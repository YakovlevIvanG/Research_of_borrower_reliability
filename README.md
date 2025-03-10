*Проект выполнялся в качестве учебного в Яндекс-практикуме по курсу "Специалист по Data Science расширенный"*
*Дата выполнения: декабрь 2023 года.*

## Исследование надежности заемщиков
**Цель работы:**  
Проанализировать предоставленный датасет и выявить закономерности.

**Описание проекта**
Заказчик — кредитный отдел банка. Нужно разобраться, влияет ли семейное положение и количество детей клиента на факт погашения кредита в срок. Входные данные от банка — статистика о платёжеспособности клиентов.
Результаты исследования будут учтены при построении модели кредитного скоринга — специальной системы, которая оценивает способность потенциального заёмщика вернуть кредит банку.

**Описание данных**
- children — количество детей в семье
- days_employed — общий трудовой стаж в днях
- dob_years — возраст клиента в годах
- education — уровень образования клиента
- education_id — идентификатор уровня образования
- family_status — семейное положение
- family_status_id — идентификатор семейного положения
- gender — пол клиента
- income_type — тип занятости
- debt — имел ли задолженность по возврату кредитов
- total_income — ежемесячный доход
- purpose — цель получения кредита

## Общие выводы по работе
1. Представлены исходные данные в количестве 21525 строк. В 2174 строке были обнаружены пропущенные значения. Пропущенные значения были в стоблцах "days_employed" (количество дней занятости) и в "total_income" (общий доход). Пустые значения были заменены на медианные в целях повышения точности анализа.  
Также были обнаружены аномальные значения в столбце "children" (дети): 20 и -1. Указанные значения были удалены как аномальные.  
Для удобства анализа общие доходы и цели кредитов были разделены на категории.


2. В общем случае на вероятность возникновения просрочки по кредиту влияет:
- семейное положение человека. Так, среди вдовцов/вдов наблюдается наименьшая доля просрочек.
- цель кредита. Наименьшая доля просрочек у кредитов, выданных для операций с недвижимостью.
- наличие или отсутствует детей. У людей с детьми доля просрочек больше, чем у людей без детей.  
- На основе представленных данных нет возможности сделать вывод о связи между доходом человека и вероятностью возникновения задолжности.


3. В целях уточнения анализа предлагается:
- дополнить данные по доходам из других источников, к примеру, по данным различных фондов социальной поддержки.
- собрать данные по величине задержек по кредитам у людей с высоким доходом и с низким доходом. Возможно, указанные данные могут сделать выводы о зависимости доходов и вероятности просрочки по кредиту.