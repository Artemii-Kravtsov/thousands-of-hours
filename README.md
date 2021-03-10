<h2 style="font-weight:normal" align="center">
  &nbsp;Портфель проектов по аналитике данных&nbsp;
</h2>
<br>
<h3 style="font-weight:normal" align="center">
Учебные проекты на любые темы, связанные с аналитикой.<br>
Под номером один - первый по счёту проект, по возрастанию - всё более поздние.
</h3>

<br>

|№|Название проекта|Описание|Стек|
|:-----:|-----|:-----:|-----|
|1|[Исследование надёжности заёмщиков](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/1_credit_scoring_leads.ipynb)|Изучение данных в столбцах; анализ пропусков; лемматизация; создание сводных таблиц| Первые шаги в `Pandas` |
|2|[Исследование объявлений о продаже квартир](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/2_prices_on_real_estate_market.ipynb)|Масштабная предобработка данных; поиск корреляций между стоимостью объектов недвижимости и их характеристиками| `Pandas`, первые шаги в `Matplotlib` |
|3|[Поиск наиболее перспективного пользовательского тарифа](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/3_comparison_of_two_pricing_plans.ipynb)|Объединение данных из пяти таблиц в одну; изучение аномалий в данных; сравнение двух тарифов по нескольким критериям и вывод о том, который из них может быть наиболее выгодным| `Pandas` `Matplotlib`, первый t-тест |
|4|[Исследование рынка видеоигр](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/4_computer_games_market_over_time.ipynb)|Определение наиболее популярных игровых жанров и игровых платформ в исторической перспективе и в разрезе регионов; выявление актуальных параметров, влияющих на успешность игры|`Pandas` `Matplotlib` `SciPy.Stats`|
|5|[Обзор данных авиакомпании](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/5_airlines_data_review.ipynb)|Попытка описать авиакомпанию, имея в распоряжении лишь информацию об основных маршрутах и авиапарке|`Pandas` `Matplotlib.Basemap` `Яндекс Геокодер`|
|6|[Оценка источников трафика](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/6_web_analytics_of_ticket_service.ipynb)|Расчет экономических показателей (метрики юнит-экономики); оценка окупаемости инвестиций в маркетинг; поиск "узкого места" в экономической модели; когортный анализ| `Pandas` `Matplotlib` `Statsmodels` |
|7|[Изучение результатов одного эксперимента](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/7_typical_ab_test.ipynb)|	Приоритизация гипотез; подготовка переменных; приятие решения о том, выполнены ли все условия для проведения корректного A/B-теста; сравнение двух групп по нескольким признакам |`Pandas` `Matplotlib`|
|8|[Рынок заведений общественного питания Москвы](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/034a268e0e3aeb7efbf3917d860e1f25623a9e95/8_restaurants_in_moscow.ipynb)|Масштабная предобработка данных; подготовка парсера; создание интерактивной карты; подбор оптимальных параметров для открывающегося кафе|`Pandas` `Matplotlib` `Open Street Map` `Plotly`|
|9|[Событийная аналитика мобильного приложения](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/9_analysing_events_logs.ipynb)|Описание воронки событий (от первого запуска до покупки); поиск разницы между клиентской и пользовательской сессиями; когортный анализ; сравнение конверсий в группах по принципу A/B-теста<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="left">Есть множество таких записей, когда показ экранов "Корзина" и "Оплачено" происходит в одну и ту же секунду, притом эти события составляют больше 1/3 от всех показов корзины и больше 1/2 от всех успешных оплат. Это похоже на сбой либо в записи логов, либо в работе приложения. Из-за этого в проекте сравниваются по неким общим чертам уникальные пользователи, их сессии, но их действия подробно не анализируются.</p></li><li><p align="left">Кроме обучения, все рассматриваемые события образуют типичную последовательность действий: Главный экран --> Каталог --> Корзина --> Оплата. Именно в таком порядке события выстраиваются в воронку. Наибольшее число пользователей (до сорока процентов) теряется на переходе с главного экрана в каталог. Среди ничего не купивших пользователей проникновение в каталог - всего 10%, и лишь около процента хоть раз заходят в корзину.</p></li><li><p align="left">Большинство первых покупок совершается в первую и вторую сессии - похоже, что пользователи скачивают приложение целенаправленно, заранее нацеливаясь на покупки. Чем выше номер некоторой сессии, тем больше по своему содержанию она похожа на клиентскую, а не пользовательскую. К двадцатой сессии не остаётся никого, кто ничего ни разу не купил.</p></li><li><p align="left">Прошедшие обучение пользователи доходят до покупкок на 10% чаще, и почти на 20% чаще - до каталога. Среди ничего не купивших пользователей доля прошедших обучение не больше 2%, остальные проигнорировали обучение. Обучение в большинстве случаев проходят в первую сессию.</p></li><li><p align="left">Клиентский retention, равно как содержание клиентской сессии незменны и постоянны. Коэффициент удержания - 60%, и одинаковый, независимо от активности клиента в приложении. Даже среди тех, кто пользуется приложением ежедневно и иногда по нескольку раз, доля что-либо купивших - 60% для каждой сессии. Не меняется и типичное содержание клиентской сессии: на протяжении семи сессий клиенты с неизменной активностью изучуют каталог и добавляют товары в корзину, а вот посещения главного экрана постепенно падают.</p></li><li><p align="left">Статистически значимых различий в конверсиях нет (ни в одной из тридцати, что были проверены). Выборочные (фактические) различия в конверсиях - в пределах полутора-двух процентных пунктов. Размеров выборок было бы недостсаточно для того, чтобы зафиксировать даже самое значительное из этих различий с уровнем значимости 0.05 - даже для двухпроцентого различия нужны выборки размером не меньше 5000 уникальных пользователей на группу. А в этом датасете в группах по 2500 уникальных пользователей.</p></li></ol></details>|`Pandas` `Plotly` `Matplotlib` `SciPy.Stats`|
|10|Создание дашборда|Создание пайплайна для получения данных из БД; проведение анализа взаимодействия пользователей сервиса с карточками; создание дашборда в Tableau Public; подготовка презентации|-|
|11|Прогнозирование вероятности оттока посетителей фитнес-центра|Прогноз вероятности оттока посетителей в следующем месяце; определение основных признаков влияющих на отток; составление портрета посетителей; предложение мер по снижению оттока|-|

<br>
<span align="center">
  
[E-mail](mailto:t_e_m_a@inbox.ru) 🔹 [Telegram](https://t.me/Artemy_Kravtsov) 🔹 [NBViewer](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/tree/master/)

</span>

