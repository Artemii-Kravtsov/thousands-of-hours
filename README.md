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
|1|[Исследование надёжности заёмщиков](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/1.%20%D0%98%D1%81%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BD%D0%B0%D0%B4%D1%91%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D0%B8%20%D0%B7%D0%B0%D1%91%D0%BC%D1%89%D0%B8%D0%BA%D0%BE%D0%B2/1_credit_scoring_leads.ipynb)|Изучение данных в столбцах; анализ пропусков; лемматизация; создание сводных таблиц<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">По кредитам тяжелее расплачиваться тем, у кого есть дети. Лучше, когда у клиентов нет детей. Но если дети есть, то по большому счёту, уже не важно, сколько их - процент проблемных кредитов для клиентов с детьми держится на одном уровне. Нужно отметить, что данных о клиентах с тремя и более детьми недостаточно, что рассуждать об их кредитной истории с уверенностью.</p></li><li><p align="justify">Не важно, одинок человек или не одинок и узаконены ли его отношения. Не столько семейное положение влияет на благонадёжность заёмщика, сколько его возраст.</p></li><li><p align="justify">Казалось, что клиенты с очень малым заработком будут очень часто иметь задолженности. Оказалось наоборот - у таких клиентов хорошие показатели. У клиентов с высоким уровнем дохода, ожидаемо, трудности с выплатой задолженности возникают реже. Наименее надёжны клиенты со средним заработком. Но явной взаимосвязи между доходами заёмщика и его надёжностью, судя по имеющимся данным, нет. Лучше ориентироваться на тип занятости, там закономерности налицо.</p></li><li><p align="justify">Можно ли говорить, что существует взаимосвязь между целью, на которую взят кредит, и вероятностью его выплаты? Да, именно об этом говорят данные, хотя интерпретировать их можно по-разному.</p></li></ol></details>| `pandas` `pymystem3` `nltk` |
|2|[Исследование объявлений о продаже квартир](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/2.%20%D0%98%D1%81%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BE%D0%B1%D1%8A%D1%8F%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B9%20%D0%BE%20%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%B6%D0%B5%20%D0%BA%D0%B2%D0%B0%D1%80%D1%82%D0%B8%D1%80/2_prices_on_real_estate_market.ipynb)|Масштабная предобработка данных; поиск корреляций между стоимостью объектов недвижимости и их характеристиками<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Насчёт пропусков: Публикации, относящиеся к целой группе пригородных населённых пунктов (среди них Мурино), содержат пропуски в столбцах с картографическими данными. Для квартир из других населённых пунктов расстояния, напротив, подсчитываются без проблем (исключая небольшое число объявлений из Санкт-Петербурга). Столбцы с расстоянием до парка и до пруда служат для уточнения данных в столбцах, где записано количество парков и прудов в радиусе трёх километров. Если в радиусеё трёх километров нет парка или пруда, в столбце с расстоянием появляется пропуск. Квартиры-студии и квартиры со свободной планировкой в столбце, содержащим площадь кухни, имеют пропуск. Если объявление актуально и до сих пор не закрыто, появляется пропуск в столбце с датой снятия с публикации. Пропуск в столбце с количеством балконов говорит о том, что, автор объявления просто не стал заполнять то поле, где ответом являлось бы \'ноль\', или \'нет балкона\'.</p></li><li><p align="justify">В пятиэтажных домах в Санкт-Петербурге квартиры на последних этажах выставляют на продажу на 15% чаще, чем квартиры с других этажей.</p></li><li><p align="justify">Объявления, относящиеся к недвижимости премиум-класса, как правило, сопровождаются большим числом фотографий. Значения некоторых переменных у этих объявлений являются выбросами в контексте всей базы данных (в случае когда все сегменты рынка недвижимости рассматриваются вместе). Для более предметного анализа следовало бы провести кластеризацию</p></li><li><p align="justify">Большая площади кухни однозначно ассоциируется с недвижимостью премиум класса. В Санкт-Петербурге каждые дополнительные несколько процентов в пользу площади кухни относительно общей площади находят отражение в цене (цена растёт). В других населённых пунктах площадь кухни не имеет такого влияния. По влиянию площади кухни на стоимость квадратного метра можно судить о том, насколько разнообразно предложение на данном рынке недвижимости.</p></li><li><p align="justify">Граница между центром и окраиной прослеживается ясно. Стоит объекту недвижимости пересечь отметку в 8500 метров до центра, как его рыночная возрастает на 15.000 за квадратный метр.</p></li><li><p align="justify">Каждый дополнительный метр площади в центре оценивается выше, чем в других областях - цена за квадратный метр в центре вырастает на сумму до 60 тысяч за каждый дополнительный квадратный метр площади, когда площадь превышает медианную. В то же время, скажем, в пригородах дополнительные метры площади никакой \'добавочной\' стоимостью не облагаются, и цена за квадратный метр остаётся более-менее на уровне медианной даже при большой общей площади квартиры. В окраинах и пригородах вы заплатите за один квадратный метр больше, если, напротив, покупаете слишком маленькую по площади квартиру.</p></li><li><p align="justify">Стоимость квадратного метра не сказывается на том, как быстро недвижимость будет продана.</p></li><li><p align="justify">Высота потолков наиболее ценится в городских окраинах. Там, если высота потолков превышает 270 сантиметров, то платить за квадратный метр вы будете почти столько же, как если бы покупали квартиру в центре. В центре города высокие потолки обычно идут \'в комплекте\' с большой общей площадью и соответствующе высокой стоимостью квадратного метра.</p></li></ol></details>| `pandas` `matplotlib` |
|3|[Поиск наиболее перспективного пользовательского тарифа](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/3.%20%D0%9F%D0%BE%D0%B8%D1%81%D0%BA%20%D0%BD%D0%B0%D0%B8%D0%B1%D0%BE%D0%BB%D0%B5%D0%B5%20%D0%BF%D0%B5%D1%80%D1%81%D0%BF%D0%B5%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%BE%D0%B3%D0%BE%20%D1%82%D0%B0%D1%80%D0%B8%D1%84%D0%B0/3_comparison_of_two_pricing_plans.ipynb)|Объединение данных из пяти таблиц в одну таблицу с мультииндексами; изучение предполагаемых аномалий; сравнение двух тарифов по нескольким критериям и вывод о том, который из них может быть наиболее выгодным<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Отсутствие данных по использованию клиентами некоторой услуги говорит о том, что клиенты этой услугой не пользовались.</p></li><li><p align="justify">В строчках с нулевой продолжительностью нет аномалии - имели место и звонки, и выходы в интернет - при рассчёте стоимости оператор, скорее всего, занёс в базу данных округлённые значения, в том числе округлённые до нуля.</p></li><li><p align="justify">Все клиенты, представленные в выборке, присоединились к оператору в течение года.</p></li><li><p align="justify">Несмотря на большую дисперсию израсходованных минут, мегабайтов и сообщений (по сравнению с клиентами на тарифе \'смарт\'), не похоже, чтобы тарифом \'ультра\' пользовались люди, испытывающие острую необходимость в большом тарифном пакете.</p></li><li><p align="justify">Клиенты на тарифе \'ультра\' не выбирают включённый в тарифную плату пакет (за исключением интернета - в ~15% случаев). А клиентам на тарифе \'смарт\' их пакета недостаточно: средняя выручка с клиента на \'смарт\'е в два с половиной раза превышает стоимость самого пакета.</p></li><li><p align="justify">На одного клиента \'ультра\', приносящего в среднем 2072 рубля в месяц, приходится 2.35 клиента \'смарт\', приносящие в сумме 3062 рубля в месяц. Поэтому, если доверять соотношению клиентов на разных тарифах в выборке, то следует, что тариф \'смарт\' при прочих равных оператору выгоднее.</p></li><li><p align="justify">Любопытно, что нулевое значение в минутах разговора встречается чаще, чем нулевое значение в мегабайтах трафика. Мобильный интернет - более востребованная услуга, чем телефония.</p></li><li><p align="justify">В среднем москвичам требуется примерно на один гигабайт трафика в месяц больше, чем жителям других городов. По остальным показателям, включая выручку, статистически значимой разницы между москвичами и не-москвичами нет.</p></li></ol></details>| `pandas` `matplotlib` `scipy.stats` |
|4|[Исследование рынка видеоигр](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/4.%20%D0%98%D1%81%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D1%80%D1%8B%D0%BD%D0%BA%D0%B0%20%D0%B2%D0%B8%D0%B4%D0%B5%D0%BE%D0%B8%D0%B3%D1%80/4_computer_games_market_over_time.ipynb)|Определение наиболее популярных игровых жанров и игровых платформ в исторической перспективе и в разрезе регионов; выявление актуальных параметров, влияющих на успешность игры<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Тренд на падение продаж как в абсолютных цифрах, так и в усреднённых, начавшийся в 2009 году, продолжается до сих пор.</p></li><li><p align="justify">Если текущее состояние рынка компьютерных игр нужно заключить в исторические рамки, то наиболее обоснованно было бы начать отсчёт актуального периода с 2013 года.</p></li><li><p align="justify">В Европе и Северной Америке ожидаем падение популярности жанра Action, рост популярности Shooter, в течение нескольких лет вероятно падение популярности Sports в Европе</p></li><li><p align="justify">В Европе положительным фактором к прибыльности будет, если игра - жанра Racing или Shooter, в японии - жанра Misc или Role-Playing, в Северной Америке - жанра Sports или Shooter. Нужно иметь в виду, что мода в Европе и Северной Америке на жанры более изменчива, чем в Японии.</p></li><li><p align="justify">В Европе и Северной Америке жанр Action может быть недооценён из-за большого кол-ва выпущенных игр. Конкуренция большая, однако если есть уверенность в том, что игра хорошая и выделяется на фоне остальных - то она может иметь коммерческий успех, так как средние показатели, несмотря на большое количество игр, находятся на относительно высоком уровне.</p></li><li><p align="justify">То же самое можно сказать про игры жанра Shooter, большинство из которых имеет рейтинг M. Игры с рейтингом M становятся в разы более перспективными как только пересекают медиану рейтинга по продажам. Поэтому если заранее известно, что игра жанра Shooter достаточно хороша и наверняка будет продана в тираже не меньше 150 тысяч копий, то есть смысл в неё вложиться.</p></li><li><p align="justify">Оценки критиков более совпадают с рыночной оценкой игры, особенно в Северной Америке. В Европе для предсказания коммерческой успешности игры можно отталкиваться от оценки критиков, но только если она выше 80 пунктов.</p></li><li><p align="justify">При прогнозировании оценок для новых игр не стоит слишком полагаться на жанр. Но если всё-таки делать прогноз, то на более благосклонный приём со стороны игроков могут рассчитывать игры жанра Adventure, Puzzle, Role-Playing, Misc и Action, а строгий суд, скорее всего, ожидает игры жанров Sports, Simulation, Racing, Strategy, Shooter.</p></li><li><p align="justify">Непопулярным и камерным играм ограниченное число их фанатов зачастую создаёт высокий пользовательский рейтинг, что видно на примере среднего рейтинга игр жанра Puzzle.</p></li><li><p align="justify">Оценки критиков более совпадают с рыночной оценкой игры, особенно в Северной Америке. В Европе для предсказания коммерческой успешности игры можно отталкиваться от оценки критиков, но только если она выше 80 пунктов.</p></li><li><p align="justify">Никаких гарантий балл от 70 до 100 не даёт - игр, которые получили высокую оценку, а много продаж, тем ни менее, не набрали, много, особенно когда речь о пользовательской оценке.</p></li><li><p align="justify">В Японии можно ориентироваться как на оценку критиков, так и на оценку пользователей, однако лишь для предсказания успешности игр, выпущенных в Японии. У зарубежных игр на японском рынке прогнозы плохие.</p></li><li><p align="justify">То, что платформа популярна у разработчиков, не означает, что она популярна у игроков. Например, за актуальный период 16% от всех игр вышли на платформе PSV (в этом отношении она занимает второе место после PS4). Но по числу проданных копий PSV занимает лишь восьмое место (из одиннадцати).</p></li><li><p align="justify">Платформа - региональный фактор. В Европе выгоднее всего выходить на PS4, в Северной Америке на XOne, в Японии на 3DS.</p></li><li><p align="justify">Пользовательская оценка игры не зависит от игровой платформы.</p></li></ol></details>|`pandas` `matplotlib` `scipy.stats`|
|5|[Обзор данных авиакомпании](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/5.%20%D0%9E%D0%B1%D0%B7%D0%BE%D1%80%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85%20%D0%B0%D0%B2%D0%B8%D0%B0%D0%BA%D0%BE%D0%BC%D0%BF%D0%B0%D0%BD%D0%B8%D0%B8/5_airlines_data_review.ipynb)|Попытка описать авиакомпанию, имея в распоряжении лишь информацию об основных маршрутах и авиапарке<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Данные не нуждаются в предобработке</p></li><li><p align="justify">Число рейсов распределено ассиметрично, есть выбросы</p></li><li><p align="justify">Авиакомпания активно действует на юге России, на Урале и в Приволжье</p></li><li><p align="justify">Флот авиакомпании рассчитан на региональные перевозки</p></li></ol></details>| `pandas` `matplotlib` `beautifulSoup` `Basemap` `futures` |
|6|[Оценка источников трафика](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/6.%20%D0%9E%D1%86%D0%B5%D0%BD%D0%BA%D0%B0%20%D0%B8%D1%81%D1%82%D0%BE%D1%87%D0%BD%D0%B8%D0%BA%D0%BE%D0%B2%20%D1%82%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0/6_web_analytics_of_ticket_service.ipynb)|Расчет экономических показателей (метрики юнит-экономики); оценка окупаемости инвестиций в маркетинг; поиск "узкого места" в экономической модели; когортный анализ<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Взятый год принёс валовой убыток в размере 77 тысяч у.е. Компания заработала с одного пользователя 1.10 у.е., потратив на его привлечение 1.44 у.е. Конверсия в первую покупку высокая - 16%. Низкое среднее количество покупок - 1.38 и низкая конверсия в повторную покупку - 17%.</p></li><li><p align="justify">Метрики роста начали стремительно расти в сентябре, а после ноября начали постепенно падать. Заметна некоторая корреляций объёмов инвестиций с метриками роста (больше вложений - больше трафик, больше покупок, больше длительность), но за год совсем не было корреляции между метриками роста и коммерческими метриками - рост первых не обеспечил роста вторых.</p></li><li><p align="justify">Не удалось найти закономерности, связывающие объём и время инвестиций с их эффективностью. Данных может быть недостаточно, но судя по тому, что есть, с объёмом и периодичностью инвестиций можно экспериментировать.</p></li><li><p align="justify">Сессий с устройств desktop на протяжении всего года примерно в три раза больше, чем с touch (соотношение ощутимо не изменяется). У клиентов, пользующихся устройствами desktop, средняя сессия значимо дольше, а средняя выручка с них значимо выше. Разница выборочных средних - 1.5 у.е, а разница истинных средних при уровне значимости 0.05 будет не меньше 0.86 у.е.</p></li><li><p align="justify">Подавляющее большинство клиентов \'живёт\' меньше месяца и ограничивается одной покупкой. Даже среди клиентов, совершивших две и более покупок, 78.3% пользуются сервисом нерегулярно, от случая к случаю. Больше половины первых покупок севершаются в срок менее двадцати минут. Больше 65% - в срок до двух часов. Конверсия во вторую покупку на данный момент является \'узким\' местом, то есть создаёт возможности для кратного роста. Представим, что конверсию во вторую покупку удалось поднять, благодаря чему среднее число покупок на клиента увеличилось с 1.38 до 2 (реалистичная задача - в некоторых когортах уже удавалось достичь этой цифры), и тогда за год, при всей убыточности инвестиций в третий и четвёртый источники (на которые приходилось более 60% всего маркетингового бюджета), вложения бы полностью окупились и принесли валовую прибыль.</p></li><li><p align="justify">Сформулировали образ идеального \'целевого\' клиента. Целевые клиенты совершают покупки и пользуются сервисом больше двух месяцев, и остаются с компанией неопределённо долго. Для удобства было предложено считать, что в месяц они совершают не меньше 0.6 покупок (чтобы отделять от тех, кого с большими промежутками удаётся повторно привлечь за счёт вложений в маркетинг). За один день целевые клиенты заходят на сайт в среднем 1.5 раз, проводит на сайте в среднем 21 минуту в день (или 12 минут, если судить по медиане).</p></li><li><p align="justify">Сервис сталкивается с новой проблемой - со временем становится всё больше клиентов, для которых сервис представляет ценность \'на один раз\'. Когорты всё хуже окупают вложения. Следует разобраться в причинах - к примеру, некоторые действия в январе привели к стремительному снижению Retention среди клиентов, а в марте и мае - к небольшому повышению. Возможно, сайт становится скучным, и следует поработать над тем, чтобы сайт, помимо агрегатора билетов, был успешен ещё и как портал о культурной жизни. Вызывал привыкание как чтение газет.</p></li><li><p align="justify">Рекомендуется вкладывать в 1 и 2 источники. Первый источник окупается за первый месяц благодаря 30%-ой конверсии в первую покупку, а 2 источник - за три месяца благодаря высокому среднему чеку и высокому среднему числу покупок. Если получится понять, что случилось в ноябре 2017 с пользователями, привлечёнными из 5 и 9 источников, то в них тоже (но в 9 - с большим риском). Вложения в 3 и 4 источники не окупаются.</p></li><li><p align="justify">Если компания планирует окупать вложения в течение года, то цена за посетителя не должна превышать его годового LTV. За пользователя из канала №2 можно заплатить не больше 2.66 у.е. Из канала №1 - не больше 3.28 у.е. Из канала №5 - не больше 1.06 у.е. Из канала №9 - не больше 0.89 у.е.</p></li></ol></details>| `pandas` `matplotlib` `seaborn` `scipy.stats` `statsmodels` |
|7|[Изучение результатов одного эксперимента](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/7.%20%D0%98%D0%B7%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%20%D1%80%D0%B5%D0%B7%D1%83%D0%BB%D1%8C%D1%82%D0%B0%D1%82%D0%BE%D0%B2%20%D0%BE%D0%B4%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%8D%D0%BA%D1%81%D0%BF%D0%B5%D1%80%D0%B8%D0%BC%D0%B5%D0%BD%D1%82%D0%B0/7_typical_ab_test.ipynb)|	Приоритизация гипотез; подготовка переменных; приятие решения о том, выполнены ли все условия для проведения корректного A/B-теста; сравнение двух групп по нескольким признакам<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Если окажется. что 58 пользователей, записанных в обе группы, были непоровну распределены между группами, то результатами теста нужно заниматься заново.</p></li><li><p align="justify">Стоит обратить внимание на долю очень дорогих покупок в группе B. Они были исключены из анализа, поскольку их появление в одной из групп в подавляющем большинстве случаев не не связано с тестируемым нововведением и мешает расчёту показателей, однако разница в долях очень дорогих покупок близка к 5%-уровню значимости (с преимуществом у группы В).</p></li><li><p align="justify">Пришлось находить накопительную конверсию, усредняя показатели конверсии за каждый день. Так происходит из-за того, что неизвестно накопительное значение уникальных пользователей, а лишь ежедневное. Есть как минимум четыре дня, конверсия за которые должна была бы быть посчитана с \'меньшим\' весом. С другой стороны, эта проблема затрагивает обе группы в равной степени, поэтому погрешность в подсчёте конверсии некритична при тестировании гипотезы.</p></li><li><p align="justify">Нет статистически значимого различия по среднему чеку между группами, независимо от того, очищены ли данные от выбросов и какой критерий мы используем для проверки гипотезы, T-критерий Стьюдента или U-критерий Манна-Уитни.</p></li><li><p align="justify">Между группами есть статистически значимое различие в конверсии. Конверсия в группе B лучше, чем у группы A на +0.0047% (процентных пункта). Ошибка подглядывания исключена, поскольку кривая разницы групп не растёт и не падает на протяжении длительного времени.</p></li><li><p align="justify">Выборки набирают достаточный размер, чтобы утверждать о статистически значимом различии конверсий ко 22 дню эксперимента (с вероятностью ошибки первого рода - 0.05). Если продолжить эксперимент, то на тридцать третий день можно будет заключить об увеличении коверсии во второй группе с вероятностью ошибки первого рода не больше 0.01.</p></li></ol></details>|`pandas` `matplotlib` `scipy.stats` `statsmodels`|
|8|[Рынок заведений общественного питания Москвы](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/8.%20%D0%A0%D1%8B%D0%BD%D0%BE%D0%BA%20%D0%B7%D0%B0%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B9%20%D0%BE%D0%B1%D1%89%D0%B5%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BF%D0%B8%D1%82%D0%B0%D0%BD%D0%B8%D1%8F%20%D0%9C%D0%BE%D1%81%D0%BA%D0%B2%D1%8B/8_restaurants_in_moscow.ipynb)|Масштабная предобработка данных; подготовка парсера; создание интерактивной карты; подбор оптимальных параметров для открывающегося кафе<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Не рекомендуется в таком объёме брать информацию из открытых источников, приходится тратить немало времени на предобработку.</p></li><li><p align="justify">Внутри третьего транспортного кольца (центр города) и за МКАДом - самая высокая доля ресторанов в Москве. За МКАД, скорее всего, из-за относительной невостребованности кофеен и сетевых ПБО, а в центре - из-за благоприятных условий для ресторанов.</p></li><li><p align="justify">Сетевые заведения чаще встречаются на окраинах, нежели в центре - на окраинах их доля выше примерно на 5-10%.</p></li><li><p align="justify">В популярных и непопулярных районах, на популярных и непопулярных улицах распределение посадочных мест идентично.</p></li><li><p align="justify">К сетевому распространению склонны, в первую очередь, предприятия быстро обслуживания и, во вторую, кафе и рестораны. Несетевые рестораны наиболее активно располагаются в центре города. Самые популярные улицы для них: \'Пресненская набережная\', \'проспект Мира\' и \'Ленинградский проспект\'.</p></li><li><p align="justify">В заведениях нашего формата по медиане 40 посадочных мест.</p></li><li><p align="justify">По мере роста сетей количество мест в ресторанах увеличивается примерно до 90, после чего сети продолжают расти только \'в ширину\'</p></li><li><p align="justify">Вопросы, поставленные в этом проекте перед аналитиком данных, лучше адресовать аналитику бизнес-идей.</p></li></ol></details>|`pandas` `matplotlib` `re` `OSM` `plotly`|
|9|[Событийная аналитика мобильного приложения](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/9.%20%D0%A1%D0%BE%D0%B1%D1%8B%D1%82%D0%B8%D0%B9%D0%BD%D0%B0%D1%8F%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D1%82%D0%B8%D0%BA%D0%B0%20%D0%BC%D0%BE%D0%B1%D0%B8%D0%BB%D1%8C%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/9_analysing_events_logs.ipynb)|Описание воронки событий (от первого запуска до покупки); поиск разницы между клиентской и пользовательской сессиями; когортный анализ; сравнение конверсий в группах по принципу A/B-теста<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Есть множество таких записей, когда показ экранов "Корзина" и "Оплачено" происходит в одну и ту же секунду, притом эти события составляют больше 1/3 от всех показов корзины и больше 1/2 от всех успешных оплат. Это похоже на сбой либо в записи логов, либо в работе приложения. Из-за этого в проекте сравниваются по неким общим чертам уникальные пользователи, их сессии, но их действия подробно не анализируются.</p></li><li><p align="justify">Кроме обучения, все рассматриваемые события образуют типичную последовательность действий: Главный экран --> Каталог --> Корзина --> Оплата. Именно в таком порядке события выстраиваются в воронку. Наибольшее число пользователей (до сорока процентов) теряется на переходе с главного экрана в каталог. Среди ничего не купивших пользователей проникновение в каталог - всего 10%, и лишь около процента хоть раз заходят в корзину.</p></li><li><p align="justify">Большинство первых покупок совершается в первую и вторую сессии - похоже, что пользователи скачивают приложение целенаправленно, заранее нацеливаясь на покупки. Чем выше номер некоторой сессии, тем больше по своему содержанию она похожа на клиентскую, а не пользовательскую. К двадцатой сессии не остаётся никого, кто ничего ни разу не купил.</p></li><li><p align="justify">Прошедшие обучение пользователи доходят до покупкок на 10% чаще, и почти на 20% чаще - до каталога. Среди ничего не купивших пользователей доля прошедших обучение не больше 2%, остальные проигнорировали обучение. Обучение в большинстве случаев проходят в первую сессию.</p></li><li><p align="justify">Клиентский retention, равно как содержание клиентской сессии незменны и постоянны. Коэффициент удержания - 60%, и одинаковый, независимо от активности клиента в приложении. Даже среди тех, кто пользуется приложением ежедневно и иногда по нескольку раз, доля что-либо купивших - 60% для каждой сессии. Не меняется и типичное содержание клиентской сессии: на протяжении семи сессий клиенты с неизменной активностью изучуют каталог и добавляют товары в корзину, а вот посещения главного экрана постепенно падают.</p></li><li><p align="justify">Статистически значимых различий в конверсиях нет (ни в одной из тридцати, что были проверены). Выборочные (фактические) различия в конверсиях - в пределах полутора-двух процентных пунктов. Размеров выборок было бы недостсаточно для того, чтобы зафиксировать даже самое значительное из этих различий с уровнем значимости 0.05 - даже для двухпроцентого различия нужны выборки размером не меньше 5000 уникальных пользователей на группу. А в этом датасете в группах по 2500 уникальных пользователей.</p></li></ol></details>|`pandas` `matplotlib` `seaborn` `scipy.stats` `plotly` `statsmodels`|
|10|[Создание дашборда](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/10.%20%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%B4%D0%B0%D1%88%D0%B1%D0%BE%D1%80%D0%B4%D0%B0/10_two_dashboards.ipynb)|Выгрузка данных из БД в файл формата csv; создание дашборда по согласованному макету несколькими способами; рекомендании насчёт построения дашборда<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Ссылка на дашборд, построенный в dash: https://sources-and-topics.herokuapp.com/</p></li><li><p align="justify">Cсылка на дашборд, построенный в Tableau: https://public.tableau.com/views/item_topics_fixedsize/sheet4</p></li><li><p align="justify">Одна запись в датасете - это не один просмотр (так как \'visits\' - это количество просмотров) и не одна карточка (так как \'age_segment\' - это переменная, описываюшая читателя, а не карточку. Судя по тому, что в конце взятого часа виден резкий всплекс активности, а для половины от всего времени наблюдения вообще нет записей, в базу данных с какой-то переодичностью заносятся уже агрегированные данные: результат выполнения какой-то функции. Поэтому в детализации до минут (на которой настояли при согласовании макета) может не быть никакого смысла. Если в базу заносятся агрегированные данные за час, то в дашборде нужна почасовая детализация.</p></li><li><p align="justify">С нормализованной stacked area chart (второй график) удобно следить за постепенным и взаимным изменением значений на временном ряду (когда изменения взаимосвязаны). При этом желательно, чтобы выполнялись несколько условий: во-первых, должно быть заранее известно, за какими значениями следить (потому что график \'шумный\' - любое колебание в одном значении двигает вверх/вниз весь график, и если не знать, куда смотреть, то ничего не будет понятно), а во-вторых, когда имеется достаточный промежуток времени, чтобы проследить за трендом (менеджерам виднее, но я бы начинал от одной недели). Для текущих целей больше подошёл бы гантельный график (dumbbell chart) с нормализованными значениями - долями каждой темы от общего числа просмотров - за выбранный промежуток времени.</p></li><li><p align="justify">Для сравнения тем по охвату аудитории отлично подходит круговая диаграмма. А тепловая таблица отлично иллюстрирует, какие сочетания тем и источников наиболее популярны, какие категории подобраны удачно и встречаются во многих сочетаниях, а какие - неудачно.</p></li><li><p align="justify">Tableau быстрее реагирует на фильтры, а dash даёт больше возможностей в вёрстке и в графиках. В этом проекте много фильтров и несложные, стандартные вычисления, поэтому лучше выбрать Tableau.</p></li></ol></details>| `pandas` `dash` `plotly` `sqlalchemy` `Tableau` |
|11|[Прогнозирование оттока в тренажёрном зале](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/11.%20%D0%9F%D1%80%D0%BE%D0%B3%D0%BD%D0%BE%D0%B7%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BE%D1%82%D1%82%D0%BE%D0%BA%D0%B0%20%D0%B2%20%D1%82%D1%80%D0%B5%D0%BD%D0%B0%D0%B6%D1%91%D1%80%D0%BD%D0%BE%D0%BC%20%D0%B7%D0%B0%D0%BB%D0%B5/11_predictive_models_for_churn.ipynb)|Разведывательный анализ данных, кластеризация клиентов; прогноз оттока посетителей с помощью моделей машинного обучения; снижение размерности выборки, настройка параметров машинного обучения, визуализация ошибок в предсказаниях<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">EDA: созданы новые поля \'trend_pct\', \'trend_pct_abs\', \'first_time_client\', \'15%_vi_fr_decrease\', \'vi_fr_decrease\', \'elapsed_time\' и \'cluster\' (в результате кластеризации). Из этих полей четыре оказались в той или иной степени полезны. Удалены около 80 записей, показавшиеся странными. Выбивающихся из общей массы значений нет, пропусков нет. Из всех имеющихся переменных лишь две никак не характеризуют отток, остальные характеризуют, притом для каждой из них разница между оттоком и удержанием уходит далеко за порог статистической значимости. Благодаря этому даже ненастроенные модели отлично справляются с предсказаниями.</p></li><li><p align="justify">Признаки, влияющие на отток: если клиент получил корпоративную скидку на абонемент (\'from_partner\') или приглашение от друга (\'promo_friends\'), то он будет посещать спортзал с большей вероятностью, чем тот, кто этих скидкок не получил. Клиенты, которые ходят на групповые занятия (\'group_visits\'), выбывают реже тех, кто тренируется самостоятельно. Проживание вдалеке от спортзала (\'lives_close\') - фактор, негативно влияющий на вероятность оттока. Чаще всего заканчивается оттоком резкое увеличение или резкое уменьшение частоты посещений (переменная \'trend_pct\'). Большая часть оттока приходится на клиентов, пришедших в спортзал совсем недавно (переменная \'lifetime\') - практиески все тренируются не больше трёх месяцев. Также выбывшие клиенты в средне тратят меньшие суммы денег на дополнительные услуги, моложе на два года и тренируются в два раза реже тех, кто не выбывает. Около 90% выбывших - владельцы месячных абонементов.</p></li><li><p align="justify">Кластеризация: шесть кластеров - самое лучшее. Стоит отметить, что для всех варинтов кластеризации silhouette низкое - кластеризация не очень естественно ложится на полный набор признаков.</p></li><li><p align="justify">Машинное обучение: для компании приоритетной метрикой является полнота, то есть способность угадать как можно больше клиентов, которые в скором времени уйдут в отток (минимизация False Negative). Модель случайного леса даёт лучшие показатели: если при вероятности оттока большей или равной 0.3406 мы будем предсказывать отток, то будем угадывать 97 из 100 клиентов, которые в скором времени перестанут посещать спортзал. Примерно 15 из 100 таких предсказаний будут ошибочными - в этих случаях не будет оттока там, где мы его предсказали. Модель логистической регрессии несколько хуже: с ней мы сможем угадывать 94-95 из 100 клиентов, совершая 17-18 ошибок на каждые сто предсказаний оттока. Одно решающее дерево можно настроить так, чтобы угадывать 85 из 100 клиентов, ошибаясь в 21 случае, зато предсказания будут делаться за три шага.</p></li><li><p align="justify">Рекоммендации для борьбы с оттоком: сопровождать новых посетителей (низкий lifetime), или хотя бы тех из них, кто пользуется своим первым абонементом. Сопровождать тех, кто за последнее время стал тренироваться намного чаще, чем раньше. Продавать абонементы на пол года и на год, вовлекать клиентов в приятные коммуникациии. Нацелить маркетинговые компании на людей постарше и на корпоративных клиентов </p></li></ol></details>| `pandas` `matplotlib` `seaborn` `scipy` `plotly` `sklearn` |
|12|[Диагностика ошибок в эксперименте](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/12.%20%D0%9A%D1%80%D0%B8%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F%20%D0%BE%D1%86%D0%B5%D0%BD%D0%BA%D0%B0%20%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D0%B4%D1%91%D0%BD%D0%BD%D0%BE%D0%B3%D0%BE%20%D1%8D%D0%BA%D1%81%D0%BF%D0%B5%D1%80%D0%B8%D0%BC%D0%B5%D0%BD%D1%82%D0%B0/12_sbermarket_ab_test.ipynb)|Поиск и интерпретация проблем, из-за которых может возникнуть недоверие к результатам A/B-теста. Выбор метрик и способа подсчёта, A/B-тест.<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><p align="justify">В сжатом виде результаты работы представлены в презентации в формате pfd:<br>https://disk.yandex.ru/i/gpIkyClLwA8i_A</p></ol></details>| `pandas` `matplotlib` `scipy.stats` `statsmodels` |
|13|[Анализ товарного ассортимента](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/13.%20%D0%90%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%82%D0%BE%D0%B2%D0%B0%D1%80%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%B0%D1%81%D1%81%D0%BE%D1%80%D1%82%D0%B8%D0%BC%D0%B5%D0%BD%D1%82%D0%B0/13_merchandise_planning.ipynb)|Предобработка; разбиение товарного ассортимента на категории; подбор товарных метрик для анализа категорий; кластеризация товаров по значениям метрик<details><summary><strong>Открыть выводы</strong></summary><ol style="padding-left: 0px;"><li><p align="justify">Ссылка на презентацию: https://disk.yandex.ru/i/7_s0t0Mhvt3Apw</p></li><li><p align="justify">Дашборд в Tableau Public: https://public.tableau.com/views/merch_project/Dashboard1</p></li><li><p align="justify">Выделили 9 категорий товаров, чуть больше 8% товаров остались неразмеченными. В основном, цветы с причудливыми названиями.</p></li><li><p align="justify">Тележки и товары из категории \'Стирка и уход за одеждой\' - основная группа товаров, от которых зависит выручка магазина. Товары из этих категорий редко берут по нескольку штук, редко берут вместе с товарами из других категорий и даже из своей категории.</p></li><li><p align="justify">Рекомендую расширять ассортимент предметов интерьера. Расширение ассортимента будет отлично воспринято покупателями и может привести к росту числа продаж: как основных товаров в корзине, так и дополнительных.</p></li><li><p align="justify">В целом, покупательские корзины в магазине не отличаются разнообразием, и основная выручка делается с единичных продаж, а не с корзин. Самая частая дополнительная покупка - товар из той же категории, что и самый дорогой товар в корзине.</p></li><li><p align="justify">Категория \'Чистота и гигиена\' - универсальные дополнительные товары и очень редко - основные товары в корзине (в корзине, где больше одного товара)</p></li><li><p align="justify">\'Цветы\' и \'Рассада\' стоят мало и вряд ли приносят большую прибыль, зато генерируют больше всего заказов и уникальных покупателей. Пик спроса приходится на весну.</p></li><li><p align="justify">Магазин не использует потенциал в лице клиентов, покупающих в магазине цветы и рассады. Среди них есть лояльная база, которая не конвертируется в покупки из более прибыльных категорий. Парадоксальным образом лояльная база не приносит столько прибыли, сколько клиенты с одноразовыми покупками.</p></li><li><p align="justify">Дополнительной покупкой к цветам обязательно стоит предлагать цветы и рассаду, и наоборот. Конверсия между этими двумя категориями отличная, как и конверсия внутри этих категорий в покупку других товаров той же категории.</p></li><li><p align="justify">Какова будет структура спроса на отдельный товар, нельзя предугадать, ориентируясь только на категорию.</p></li></ol></details>| `pandas` `matplotlib` `scipy.stats` `plotly` |

<br>
<span align="center">
  
[E-mail](mailto:artemiy.kravtsov@internet.ru) 🔹 [Telegram](https://t.me/Artemy_Kravtsov) 🔹 [NBViewer](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/tree/master/)

</span>

