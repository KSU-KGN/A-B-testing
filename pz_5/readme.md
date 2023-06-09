# A-B-testing
## A/B-тестирование 

Папка "pz_5": Урок 5. Применение математической статистики для проверки гипотез в реальной жизни для популярных метрик (Практическое задание)
___________________________
### Выполнение практического задания № 5
### Урок 5. Применение математической статистики для проверки гипотез в реальной жизни для популярных метрик

#### Задание
1. Вы провели эксперимент c упрощением формы заказа в магазине Утконос и получили результаты по метрике конверсий в покупку.<br>
Выберите метод оценки и оцените есть ли стат. значимые различия между конверсиями в двух группах при alpha = 5%.<br>
Дайте краткие рекомендации команде.<br>
Результаты:<br>

        *	Число юзеров в группах, которые заходили на сайт в период эксперимента: n1 = 15550 и n2 = 15550. 
        *	Число юзеров в группах, которые совершили хотя бы одну покупку за период эксперимента: n1 = 164 и n2 = 228 
        *	Конверсии: conv1 = 1.05% conv2 = 1.47%<br>

2. Сравниваем метрику конверсия в покупку.<br> 
Размер выборки - 10000 элементов в каждой группе. <br>
Какой статистический критерий тут лучше всего подойдёт и почему?
#### Решение.
#### Задание 1. 
Метрика конверсий в покупку – это метрика долей (качественные данные).<br>
Эксперимент проходил среди пользователей, которые заходили на сайт в период эксперимента – это независимые группы.<br>
Число групп – 2 группы.<br>
Нам известны значения конверсий в каждой группе.<br>
Выбираем Z-критерий долей:<br>
![Notifications](https://github.com/KSU-KGN/A-B-testing/raw/main/pz_5/pz_5_1_z.jpg)        
Обнаружены статистически значимые различия между конверсиями в двух группах при alpha = 5%:<br> 
p-value < alpha (0.0011 < 0.05).<br>
Результат теста: Вы можете быть на 95 % уверены, что этот результат является следствием внесенных вами изменений, а не результатом случайности.<br>
<br>
Чтобы дать рекомендации команде воспользуемся критерием Хи-квадрат на однородность:<br>
![Notifications](https://github.com/KSU-KGN/A-B-testing/raw/main/pz_5/pz_5_1_x.jpg)   
Как видим из теста здесь также p-value < alpha, а показатели во 2-й группе более успешные.<br>
Рекомендации команде: выкатывать в продакш на всех пользователей 2-й вариант эксперимента.<br>
#### Задание 2. 
Известно: 
* Используется Метрика конверсий в покупку
* Размер выборки - 10000 элементов в каждой группе. 

Метрика конверсий в покупку – это метрика долей (качественные данные).<br>
Мы не знаем, среди каких групп производился эксперимент: зависимых или независимых.<br>
Число групп также неизвестно.<br>
<br>
Предположим, что у нас независимые группы, тогда:
1. 2 группы: необходимо использовать критерий Хи-квадрат Пирсона
2. 3 и более групп: необходимо использовать критерий Хи-квадрат Пирсона с поправкой на правдоподобие

Предположим, что у нас зависимые группы, тогда:
1. 2 группы: необходимо использовать критерий Мак-Нимара
2. 3 и более групп: необходимо использовать О-критерий Кокрена

Если мы будем сравнивать с заданным значение, то воспользуемся Z-критерием.<br>
<br>
Но перед этим, стоит проверить размер тестовой группы для желаемого минимального статистически значимого изменения.<br> 
Чем меньше alpha и больше статистическая мощность, тем больше участников эксперимента потребуется.<br> 
Чтобы посчитать конкретную минимальную цифру необходимо знать базовый уровень конверсии, минимальное значение для обнаружения изменения, значение alpha (процент, когда разница будет обнаружена при условии, что ее нет) и уровень мощности (процент, когда будет обнаружено минимальное значение изменения, если оно существует).
