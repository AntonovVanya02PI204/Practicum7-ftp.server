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

Далее запишем текстовый файл в раннее созданной папке tasks

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
















