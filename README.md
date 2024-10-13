# WebProg

Здесь будет вся инфа по лабораторным работам по дисциплине "Веб-программирование"
Инфа для супер пользователя 
Url - http://127.0.0.1:8000/admin/
login - root
password - qwerty312

14.10.2024
За сегодня был с нуля создан проект на Django, с требованиями 1 лабораторной

# создаем новый проект
- django-admin startproject

# создаем само приложение
- python manage.py startapp Yurii

# пишим наши представления по пути Yurii/views.py

def index(request):
    return HttpResponse("Стандартная Страница")

def name(request):
    return render(request, "name.html")

def age(request):
    return render(request, "age.html")

def groupe(request):
    return render(request, "groupe.html")

def common(request):
    return render(request, "common.html")

В фунцию мы возвращаем html файл к которому мы хотим обратится 

# Добавляем путь 
Создаем список urlpatterns в файле Toloknov/urls где каждый элемент представляет собой маршрут в нашем Django приложении с определенным представлением 

Похожую операцию проделываем в файле Yurii/urls

# Работаем с настройками
В файле settings.py в списке INSTALED_APPS добавляем строку Yurii
"Забыл зачем, но без этого у меня не хотят грузиться html страницы, которые я создал

# Работа с шаблонами 
В папке приложения создаем еще одну папку templates, в которой создаем наши html файлы
У меня получилось 4 файла age, common, groupe, name.html В которые я записал Имя/Фамилию, группу, возраст и все данные в купе.

# Создание суперпользователя
python manage.py createsuperuser

Вводим логин и пароль которые я указал в начале

На этом пока все, дальше буду вспоминать как прикрутить фронт, мб что-то из этого да выйдет.
