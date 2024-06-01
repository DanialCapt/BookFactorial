# КнигаФакториал!

Это сайт для ознакомления с книгами. Здесь пользователи смогут зарегистрироваться, а затем войти в систему, используя свои имя пользователя и пароль. Как только они войдут в систему, они смогут искать книги, оставлять отзывы об отдельных книгах и просматривать отзывы других людей. Также здесь используется сторонний API Goodreads, еще одного веб-сайта, посвященного обзорам книг, для получения оценок от более широкой аудитории. Наконец, пользователи смогут запрашивать информацию о книге и отзывы о ней программным способом через API этого веб-сайта.

Я попытался сделать это приложение модульным. Основное приложение находится в папке application, которая содержит 3 модуля.

 1. Auth: Этот модуль содержит логику, связанную с аутентификацией пользователя.
 2. Основной: Этот модуль содержит в основном логику поиска книг и просмотра результатов.
 3. API: Как следует из названия, этот модуль содержит всю логику API.
 
Два из этих модулей имеют свой собственный каталог шаблонов, хотя каждый модуль использует некоторые общие шаблоны и статические файлы.
- Внутри нашего приложения есть файл __init__.py, который играет жизненно важную роль. Он объединяет все модули и создает замечательную комбинацию, которая очень перспективна, но пока не работает. 
- Вне приложения есть конфигурационный файл, который содержит важные параметры конфигурации, необходимые для бесперебойной работы этого приложения.
- Что делает import.py, так это считывает данные из books.csv и импортирует их в нашу базу данных PostgreSQL.
- Pipenv нужен для виртуальной среды, так что, Pipfile и Pipfilefile.требуется блокировка.
- Wsgi.py это файл, который помещает наше приложение в трек, запускает движок и вуаля, оно работает!