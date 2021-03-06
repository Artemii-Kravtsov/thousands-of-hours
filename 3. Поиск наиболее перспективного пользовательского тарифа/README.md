# Поиск наиболее перспективного пользовательского тарифа
[Открыть проект в NBViewer](https://nbviewer.jupyter.org/github/Artemii-Kravtsov/thousands-of-hours/blob/master/3.%20%D0%9F%D0%BE%D0%B8%D1%81%D0%BA%20%D0%BD%D0%B0%D0%B8%D0%B1%D0%BE%D0%BB%D0%B5%D0%B5%20%D0%BF%D0%B5%D1%80%D1%81%D0%BF%D0%B5%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D1%81%D0%BA%D0%BE%D0%B3%D0%BE%20%D1%82%D0%B0%D1%80%D0%B8%D1%84%D0%B0/3_comparison_of_two_pricing_plans.ipynb)
<br>

## Задачи 
- Проверить гипотезу о том, что средняя выручка пользователей тарифов «Ультра» и «Смарт» различается.
- Проверить гипотезу о том, что средняя выручка пользователей из Москвы отличается от выручки пользователей из других регионов.
- Какой тариф выгоднее для компании? 


## Коротко о данных 
4 датафрейма, в которых собрана информация о пятиста уникальных пользователях. В одном - персональные данные. В остальных датафреймах по три переменных: уникальный идентификатор, временная переменная и непрерывная числовая переменная. Возникают трудности с интерпретацией данных из-за того, что о некоторых пользователях нет данных и из-за того, что непрерывная числовая переменная принимает значение '0'. 


## Библиотеки 
`pandas` `matplotlib` `scipy.stats`


## Выводы 
<ol style="padding-left: 0px;"><li><p align="justify">Отсутствие данных по использованию клиентами некоторой услуги говорит о том, что клиенты этой услугой не пользовались.</p></li><li><p align="justify">В строчках с нулевой продолжительностью нет аномалии - имели место и звонки, и выходы в интернет - при рассчёте стоимости оператор, скорее всего, занёс в базу данных округлённые значения, в том числе округлённые до нуля.</p></li><li><p align="justify">Все клиенты, представленные в выборке, присоединились к оператору в течение года.</p></li><li><p align="justify">Несмотря на большую дисперсию израсходованных минут, мегабайтов и сообщений (по сравнению с клиентами на тарифе 'смарт'), не похоже, чтобы тарифом 'ультра' пользовались люди, испытывающие острую необходимость в большом тарифном пакете.</p></li><li><p align="justify">Клиенты на тарифе 'ультра' не выбирают включённый в тарифную плату пакет (за исключением интернета - в ~15% случаев). А клиентам на тарифе 'смарт' их пакета недостаточно: средняя выручка с клиента на 'смарт'е в два с половиной раза превышает стоимость самого пакета.</p></li><li><p align="justify">На одного клиента 'ультра', приносящего в среднем 2072 рубля в месяц, приходится 2.35 клиента 'смарт', приносящие в сумме 3062 рубля в месяц. Поэтому, если доверять соотношению клиентов на разных тарифах в выборке, то следует, что тариф \'смарт\' при прочих равных оператору выгоднее.</p></li><li><p align="justify">Любопытно, что нулевое значение в минутах разговора встречается чаще, чем нулевое значение в мегабайтах трафика. Мобильный интернет - более востребованная услуга, чем телефония.</p></li><li><p align="justify">В среднем москвичам требуется примерно на один гигабайт трафика в месяц больше, чем жителям других городов. По остальным показателям, включая выручку, статистически значимой разницы между москвичами и не-москвичами нет.</p></li></ol>
