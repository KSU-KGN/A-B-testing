# A-B-testing
## A/B-тестирование 

Папка "pz_2": Урок 2. А/Б тестирование (Практическое задание)
___________________________
### Выполнение практического задания № 2
### Урок 2. А/Б тестирование

#### Задание 1. 
Сделайте приоритизацию гипотез из предыдущего урока с помощью ICE.<br>

#### Задание 2.
Составьте шаблон дизайна эксперимента для гипотезы, которая набрала больше всего баллов в практическом задании предыдущего урока.<br>

#### Решение.

#### Задание 1. 
<b>Приоритизация гипотез по ICE:</b><br>
<table>
  <tr>
    <th></th>
    <th></th>
 	 	<th>Impact влияние<br>(0-10)</th>
    <th>Confidence уверенность<br>(0-10)</th>
    <th>Ease лёгкость реализации<br>(0-10)</th>
    <th>ICE Score<br>(IxCxE)</th>
  </tr>
  <tr>
    <th>1</th>
    <td>Улучшение функционала на странице «Сравнения товаров»:<br>
    • ранжирование/ перетаскивание пользователем выбранных товаров<br>
    • возможность выбирать только нужные характеристики товаров для сравнения</td>
    <td align="center">6</td>	
    <td align="center">3</td>	
    <td align="center">9</td>	
    <td align="center">162</td>
  </tr>
  <tr>
    <th>2</th>
    <td><b>Баннер Регистрации в бонусной программе.<br>
    Реклама преимуществ Бонусной программы.</b></td>	
    <td align="center"><b>8</b></td>	
    <td align="center"><b>5</b></td>	
    <td align="center"><b>10</b></td>	
    <td align="center"><b>400</b></td>
  </tr>
  <tr>
    <th>3</th>
    <td>Хронология сортировки на странице в Избранном.</td>	
    <td align="center">5</td>	
    <td align="center">3</td>	
    <td align="center">10</td>	
    <td align="center">150</td>
  </tr>
  <tr>
    <th>4</th>
    <td>Новые пункты выдачи товаров.</td>	
    <td align="center">10</td>
    <td align="center">10</td>
    <td align="center">2</td>
    <td align="center">200</td>
  </tr>
</table>

#### Задание 2.
Больше всего баллов набрала Гипотеза 2:<br>
«Баннер Регистрации в бонусной программе. Реклама преимуществ Бонусной программы».<br>

<b>Шаблон дизайна эксперимента:</b>
1.	Гипотеза.
2.	Что делаем.
3.	На каких пользователях тестируем.
4.	Ключевые метрики для оценки эксперимента.
5.	Ожидаемый эффект.
6.	План действий в зависимости от результатов эксперимента.

<b>1. Гипотеза:</b><br>
Если на странице https://www.citilink.ru мы добавим Рекламный баннер с приглашением зарегистрироваться в Программе лояльности, где кратко говорится о преимуществах программы «Клуб Ситилинк» для незарегистрированных пользователей (с переходом на специальную страницу, где расписаны все преимущества и плюшки бонусной программы), то это привлечёт новых потенциальных постоянных клиентов, что увеличит конверсию на 1-2%, потому что незарегистрированные пользователи не знают о такой возможности и её трудно найти на сайте, а бонусная программа делает более привлекательными покупки именно на этом сайте, потому что некоторые конкуренты отказались от таких программ.

<b>2. Что делаем:</b><br>
**Контрольная версия:** оставляем текущий вид страницы.<br>
**Тестовая версия:** добавляем Баннер Регистрации в бонусной программе вверх главной страницы сайта в одном ряду с Лентой акций-рекомендаций справа от ленты.

<b>3. На каких пользователях тестируем:</b><br>
Только на незарегистрированных пользователях.

<b>4. Ключевые метрики для оценки эксперимента:</b><br>
*	Процент конверсий в регистрацию (после перехода по ссылке на рекламную страницу) (%CR) — primary (ключевая метрика).
*	Процент показателя отказов от регистрации (после перехода по ссылке на рекламную страницу) — secondary1 (добавочная 1).
*	Процент перехода по ссылке на рекламную страницу — secondary2 (добавочная 2).

<b>5. Ожидаемый эффект:</b><br>
Увеличение конверсии (регистрация новых пользователей) на 1-2%.

<b>6. План действий в зависимости от результатов эксперимента:</b><br>
*	Если наш эксперимент будет положительным: мы зафиксируем ожидаемое улучшение в ключевой метрике и будет приемлемый показатель в добавочной 1, будет достаточный показатель в добавочной 2, то масштабируем изменение и «выкатываем» его на всех незарегистрированных пользователей.
*	Если мы зафиксируем ожидаемое улучшение в ключевой метрике, но будет большой показатель в добавочной 1, то масштабируем изменение и «выкатываем» его на всех незарегистрированных пользователей, но продолжаем работу - улучшаем Рекламную страницу преимуществ Бонусной программы, анализируем саму Бонусную программы.
*	Если мы зафиксируем ожидаемое улучшение в ключевой метрике, но показатель в добавочной 2 будет недостаточный, то масштабируем изменение и «выкатываем» его на всех незарегистрированных пользователей, но продолжаем работу – улучшаем дизайн и содержание Баннера Регистрации в бонусной программе.
*	Если ключевая метрика упадёт, то откатываем эксперимент.
*	Если ключевая метрика вырастит недостаточно, то: 
    *	при большом показателе в добавочной 1 улучшаем Рекламную страницу преимуществ Бонусной программы, анализируем саму Бонусную программы;
    * при малом показателе в добавочной 2 улучшаем дизайн и содержание Баннера Регистрации в бонусной программе.