# Навигация WIN									
	Команда	Качество								
	1	2	3	4						
	CD									домашняя директория
	CD	 ..								перейти на одну вверх
	CD	name								перейти в директорию
	CD	name	/	name						перейти в директорию в диретории
										
	PWD									где я, сообщает положение
										
	ls									содержание текущей директории
	ls 	..								содержание родительской директории
	ls 	~								содержание домашней директории
	ls	 -a								содержание директории со скрытыми файлами
	ls	 -la	.ssh/							Проверка наличия директории, ключами SSH
										
	touch	name								создание файла
	touch	name	/	name						создание файла в директории
	touch	 ..	/	 ..	/	name				создание файла в директории на две выше
										
	mkdir	name								создание директории
	mkdir	 -p	/	name	/	name				создание директории в директории
	mkdir	~	/	name	/	name				создание директории в директории в домашней папке
	mkdir	..	/	name	/	name				создание директории в директории в родительской папке
										
		что		куда						
	cp	name		name						копирование файлов
										
										
		что		куда						
	mv	name		name						перемещение файлов
				что		что		куда		
	mv	..	/	name		name				перемещение файлов из разных директорий
										
	cat	name								чтение только текстовых файлов
										
	rm	name								удалить файл
	rmdir	name								удалить пустую директорию
	rm	 -r								удалить не пустую директорию
										
	mkdir	name1	&&	cp	name		name1			созать директорию и скопировать в неё файл
										
										
	ssh	 -keygen 	 -t	ed25519	 -C	"Email"			Генерация ключей публичного и приватного
	ssh	 -keygen 	 -t	rsa	 -b	4096	 -C	"Email"	Генерация ключей публичного и приватного зап вариант
										
	clip	<	name							Копирование содержимого файла
	clip	<	~	/	.ssh/id_rsa.pub				Копирование содержимого публичного ключа в домашней директории
						
# Основные команды Git									
					
	Команда	Качество								
	1	2	3	4						
	git init								Инициализировать Гит репозиторий
										
	git	config	 --global	user.name		name		Заполнение конфигурации имени
	git	config	 --global	user.email		email		Заполнение конфигурации Электронной почты
										
	rm	 -rf	.git							Разгитить папку, удалив Гит репозиторий
										
	 -r									рекурсивно (папки вместе с содержимым)
	f									заставить (точно, точно)
										
	git 	status								проверить состояние гит репозитория
										
	git 	add								подготовить файл к сохранению
										
	git 	add 	 --all							подготовить файлы к сохранению
										
	git 	add								подготовить текущую папку с файлами к сохранению
										
	git 	commit	 -m							сохранить историю с пояснением
										
	git 	log								Просмотреть историю коммитов
										
	git	remote	 -v							Проверить связь репозиториев локального и публичного
										
	git	push	 -u	origin	main					В первый раз пушим связывая локальный и публичный реппозитории
			 -u		master					первый раз свяжет локальную ветку с одноименной удалённой
	git	push	 --global	push.default		current		Всегда создаёт удалённую ветку, отслеживающую локальную
										
	cat	~	/.gitconfig						Убедится что инфа попала в конфигурацию
	git	config	 --list							Убедится что инфа попала в конфигурацию
										
	git	branch	 -a							Проверка удалённых ветвей


				


# Шпаргалка. Базовые команды в консоли
Чтобы вам было удобнее взаимодействовать с командной строкой, мы подготовили шпаргалку. В ней собраны все команды, о которых мы рассказали в уроках, и их полезные вариации. 
Навигация
pwd (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке;
ls (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;
ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;
cd first-project (от англ. change directory, «сменить директорию») — перейди в папку first-project;
cd first-project/html — перейди в папку html, которая находится в папке first-project;
cd .. — перейди на уровень выше, в родительскую папку;
cd ~ — перейди в домашнюю директорию (/Users/Username);
cd / — перейди в корневую директорию.
Работа с файлами и папками
Создание
touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке;
touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;
mkdir second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке.
Копирование и перемещение
cp file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место;
mv file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место.
Чтение
cat file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt.
Удаление
rm about.html (от англ. remove, «удалить») — удали файл about.html;
rmdir images (от англ. remove directory, «удалить директорию») — удали папку images;
rm -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.
Полезные возможности
Команды необязательно печатать и выполнять по очереди. Можно указать их списком — разделить двумя амперсандами (&&).
У консоли есть собственная память — буфер с несколькими последними командами. По ним можно перемещаться с помощью клавиш со стрелками вверх (↑) и вниз (↓).
Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать Tab. Если файл или папка есть в текущей директории, командная строка допишет путь сама.
Например, вы находитесь в папке dev. Начните вводить cd first и дважды нажмите Tab. Если папка first-project есть внутри dev, командная строка автоматически подставит её имя. Останется только нажать Enter.