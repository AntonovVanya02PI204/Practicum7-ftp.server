FTP сервер


Цель работы - Научиться программно работать с файлами и файловой системой, читать, создавать, перемещать и передавать файлы по сети
Задания для выполнения
Создать сервер, который предоставляет клиенту базовые возможности файлового менеджера по сети. Клиент после подключения к серверу должен иметь возможности просматривать список файлов и папок в рабочей директории сервера (рабочая директория - это специальная папка, к которой имеет доступ процесс сервера, но она отделена от парки с кодом сервера и от любых системных файлов), создавать и удалять в ней папки, создавать, копировать и переименовывать файлы. Также клиент может передать на сервер название и содержимое файла и сервер должен создать соответствующий файл в текущей директории. Кроме того, клиент может запросить содержимое любого файла и сервер должен передать его в ответ.
Дополнительные задания:
Ограничьте возможности пользователя рамками одной определенной директории. Внутри нее он может делать все, что хочет: создавать и удалять любые файлы и папки. Нужно проследить, чтобы пользователь не мог совершить никаких действий вне пределов этой директории. Пользователь, в идеале, вообще не должен догадываться, что за пределами этой директории что-то есть.
Добавьте логирование всех действий сервера в файл. Можете использовать разные файлы для разных действий, например: подключения, авторизации, операции с файлами.
Добавьте возможность авторизации пользователя на сервере.
Добавьте возможность регистрации новых пользователей на сервере. При регистрации для пользователя создается новая рабочая папка (проще всего для ее имени использовать логин пользователя) и сфера деятельности этого пользователя ограничивается этой папкой.
Реализуете квотирование дискового пространства для каждого пользователя.
Реализуйте учётную запись администратора сервера.
Напишите отладочный клиент. Клиент должен подключаться к серверу и в автоматическом режиме тестировать корректность его работы. Используйте подход, аналогичный написанию модульных тестов. Клиент должен вывести предупреждающее сообщение, если сервер работает некорректно.

Скриншоты проделанной работы: 
Работа в командной строке:  - подключение клиента и сервера: 

![image](https://user-images.githubusercontent.com/92279258/146115305-47e567bb-3ad1-49f8-a8e9-43ba25ce25cf.png)


![image](https://user-images.githubusercontent.com/92279258/146114989-1afcc3ab-ba4a-470a-b2f2-6799427b25dc.png)

Создание папки:

![image](https://user-images.githubusercontent.com/92279258/146251059-4e18e827-87af-42e3-b3ce-0e97af644acf.png)

![image](https://user-images.githubusercontent.com/92279258/146251102-3bb345b0-35ef-4991-b119-36ae056c711c.png)

Создаем в данной директории папку tasks с помощью команды mkdir 

![image](https://user-images.githubusercontent.com/92279258/146251179-83d63d5c-d82f-42c1-bb0b-371a08afe156.png)

Как видим, наша папка появилась 

![image](https://user-images.githubusercontent.com/92279258/146251255-40a1e259-1016-450f-bd7e-a17c874cd1ad.png)

Перейдем в нее, убедимся что она пуста 

![image](https://user-images.githubusercontent.com/92279258/146251320-1af98d37-37c2-428d-ad98-64192802292c.png)

Теперь посмотрим, как отображаются наши действия на сервере:

![image](https://user-images.githubusercontent.com/92279258/146251502-e589bcc7-0c0e-4ba1-ad2b-1fd25df60ed8.png)

Далее  с помощью команды echo создадим новый файл, запишем в него текст, ( данный файл  расположен в раннее созданной папке tasks)

![image](https://user-images.githubusercontent.com/92279258/146251703-c6ced06c-cde0-4fa5-b5f8-2530dd1c3c4d.png)

Проверим его наличие и содержимое в нем

![image](https://user-images.githubusercontent.com/92279258/146251856-38bb975d-4aa6-4128-9388-0b0cf1d38771.png)

![image](https://user-images.githubusercontent.com/92279258/146251885-9d31847a-84ef-44ee-9890-508e1be4ca48.png)

![image](https://user-images.githubusercontent.com/92279258/146251939-be02f92b-3672-44ff-8b34-a1bc321b5b01.png)

Проверим содержимое папки tasks с помощью команды ls

![image](https://user-images.githubusercontent.com/92279258/146252106-a0ed0abf-bf01-4f13-8283-00bd12713464.png)

Отображение всех действий на сервере 

![image](https://user-images.githubusercontent.com/92279258/146252191-c72fb695-d6bc-4fd0-977f-cf388b3dbfd6.png)

Проверка содержимого файла с помощью команды cat 

![image](https://user-images.githubusercontent.com/92279258/146253383-f84d953f-6944-42e1-b0fe-e065ee2b8276.png)


Отображение содержимого папки или файла, перемещение: 

![image](https://user-images.githubusercontent.com/92279258/146253485-4bb41c3a-8030-4a28-a765-39726d1818b8.png)


![image](https://user-images.githubusercontent.com/92279258/146253083-4b67af59-27f2-4184-929d-94321838ff7d.png)


![image](https://user-images.githubusercontent.com/92279258/146254290-78bb7076-c9e8-4f64-91ad-0c6d0bc73ec1.png)


![image](https://user-images.githubusercontent.com/92279258/146253552-ed7fdf4e-574d-47bf-a415-26a55b083719.png)


Удаление файла с помощью команды rm

![image](https://user-images.githubusercontent.com/92279258/146254529-ff984614-1fa6-4f98-81c5-21c4c07a59ab.png)

![image](https://user-images.githubusercontent.com/92279258/146253737-6e680665-7d27-4403-b3a0-c80e49870ac9.png)

![image](https://user-images.githubusercontent.com/92279258/146253815-02e271a8-5fa2-42ee-9abe-c4e6483b1b02.png)

![image](https://user-images.githubusercontent.com/92279258/146253843-30df9296-c4bf-46a2-84e1-af40cb291bbb.png)

Создадим новую папку tasks2, а затем удалим ее с помощью команды rmdir

![image](https://user-images.githubusercontent.com/92279258/146256662-5938a483-d312-481a-8a24-9c3e43e82950.png)

![image](https://user-images.githubusercontent.com/92279258/146256446-435ccd99-82b6-4120-b3c2-e2d55b5da616.png)

![image](https://user-images.githubusercontent.com/92279258/146256483-eab8acf8-d8a7-410d-ba8a-df1193a108c6.png)

![image](https://user-images.githubusercontent.com/92279258/146256533-a5669266-6fbd-479a-831b-127dc2bb941a.png)

Как видим, папка tasks2 удалилась 

![image](https://user-images.githubusercontent.com/92279258/146256631-ee72c23e-3d2a-411d-bbb5-129e0c033a5a.png)


![image](https://user-images.githubusercontent.com/92279258/146256767-db2dbd9d-ff5a-4e44-9735-31511d9cf276.png)

Теперь с помощью команды exit осуществим выход - отключение клиента от сервера

![image](https://user-images.githubusercontent.com/92279258/146256984-775c28c1-a309-494d-8b6c-fff4e7768716.png)

Дополнительные задания:
Ограничьте возможности пользователя рамками одной определенной директории. Внутри нее он может делать все, что хочет: создавать и удалять любые файлы и папки. Нужно проследить, чтобы пользователь не мог совершить никаких действий вне пределов этой директории. Пользователь, в идеале, вообще не должен догадываться, что за пределами этой директории что-то есть.

Убедимся в работоспособности данного действия - (файл клиента)

![image](https://user-images.githubusercontent.com/92279258/146257502-0ea22bf5-6140-4a24-a57b-45ce574bb22f.png)

Если Host и Port не указаны, они используются по умолчанию (Host=localhost, Port=9090)

![image](https://user-images.githubusercontent.com/92279258/146257961-1866d159-8908-4018-bc4d-00c2d0fe97a3.png)

![image](https://user-images.githubusercontent.com/92279258/146258012-5a1b7311-f1d7-4802-82f1-2ef120f90201.png)


Файл сервера : 

![image](https://user-images.githubusercontent.com/92279258/146257607-c89152e7-b771-42a7-934f-14401df0e86f.png)

Содержимое папки: 

![image](https://user-images.githubusercontent.com/92279258/146257873-0334c351-07bc-4b68-bf0e-f55bf2f0c3ff.png)

Добавьте логирование всех действий сервера в файл. Можете использовать разные файлы для разных действий, например: подключения, авторизации, операции с файлами.

Логи добавлены в файл log.txt

![image](https://user-images.githubusercontent.com/92279258/146258249-aca84e00-0099-4bfe-b8e2-0341a3e4c362.png)

![image](https://user-images.githubusercontent.com/92279258/146258279-f92e2c9d-8c0a-4bc7-a996-c16ae63397f6.png)

Добавьте возможность авторизации пользователя на сервере.

Если пользователь уже зарегистрирован и хочет войти под своим именем - ( авторизоваться), он должен ввести цифру 2 - ( как на скриншоте ниже - файл клиента)  

![image](https://user-images.githubusercontent.com/92279258/146258583-bc8be822-fea4-4ac0-b89b-d6f0a2448094.png)

Отображение на сервере: ( на скриншоте - файл сервера )

![image](https://user-images.githubusercontent.com/92279258/146258712-4b1ce8d5-dd55-4fc0-82e7-4c7dd046d9f2.png)

Как видим, пользователь Admin действительно существует, так как у него есть своя именная папка: 

![image](https://user-images.githubusercontent.com/92279258/146258865-271ce9c3-a632-4948-a9c5-201380167882.png)

Данные со всеми пользователями, которые зарегистрированы в нашей системе, записываем в отдельный текстовый файл Users.txt

![image](https://user-images.githubusercontent.com/92279258/146258987-68f4bf20-48ac-4458-869c-041753dc361a.png)

Добавьте возможность регистрации новых пользователей на сервере. При регистрации для пользователя создается новая рабочая папка (проще всего для ее имени использовать логин пользователя) и сфера деятельности этого пользователя ограничивается этой папкой.

Если пользователь еще не зарегистрирован в системе - он может это сделать, нажав цифру 1 ( как на скриншоте ниже ) - файл клиента 

![image](https://user-images.githubusercontent.com/92279258/146259459-93bfe4aa-4735-49ec-b8ed-19699f125b51.png)

![image](https://user-images.githubusercontent.com/92279258/146259530-42409455-a68b-4e8a-8462-3497ddb06e95.png)

Отображение на сервере: ( на скриншоте - файл сервера )

![image](https://user-images.githubusercontent.com/92279258/146259768-70745ceb-90d3-4d69-a5f3-3aa9b6d0ac3c.png)

Как видим, в файл Users.txt, где хранится вся информация о зарегистрированных пользователях, добавился пользователь Admin2 

![image](https://user-images.githubusercontent.com/92279258/146259891-791a1a8d-882b-427e-9e65-5d234e6213a9.png)

Также создалась новая папка - папка пользователя Admin2

![image](https://user-images.githubusercontent.com/92279258/146260024-b20e8abe-d3e0-47bf-802f-8513dcc27af3.png)

Реализуйте учётную запись администратора сервера.


![image](https://user-images.githubusercontent.com/92279258/146260094-635a02be-9fde-461b-b904-747c9104e22c.png)

![image](https://user-images.githubusercontent.com/92279258/146260137-c7a9756e-8592-487e-8683-1282efe7fe9c.png)













































