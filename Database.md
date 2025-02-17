# Домашнее задание к занятию 11.1. «Базы данных, их типы» - Александр Сомкин.

---

### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков.
СУБД должна гарантировать целостность и чёткую структуру данных.

Для задач бюджетирования проектов с формированием финансовых аналитических отчетов и прогнозирования рисков, рекомендую использовать реляционные СУБД. Такие СУБД гарантируют целостность и четкую структуру данных за счет использования таблиц и связей между ними.
Рекомендую использовать транзакционную модель СУБД. 

Если хеширование стало занимать длительное время, можно рассмотреть возможность использования параллельной обработки с помощью многопоточности.
Для этого можно воспользоваться API, поддерживающим многопоточность, такими как Java Concurrency API, C++11 Thread Support Library, .NET Parallel Library и т.д.

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к 
маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? 
СУБД должны быть гибкими и быстрыми.

Для лендингов и CRM, где требуется гибкость и быстродействие, рекомендуется использовать NoSQL СУБД.
Для лендингов, где обычно хранится относительно небольшой объем данных, часто используются NoSQL СУБД, такие как MongoDB или Cassandra.

Для CRM систем, где необходимо хранить большие объемы структурированных данных и обрабатывать сложные запросы, рекомендуется использовать реляционные СУБД, такие как Oracle Database, Microsoft SQL Server или PostgreSQL.

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу 
и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

Для создания базы данных отдела контроля качества, содержащей информацию о корпоративных нормах и правилах, обучающих материалах и т.д., рекомендуется использовать СУБД с простой и понятной структурой, которая позволяет легко организовывать и хранить данные.
Одним из примеров такой СУБД может быть реляционная СУБД, такая как MySQL, PostgreSQL или Microsoft SQL Server. 

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов 
по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать
со связями.


Для решения задач, связанных с формированием маршрутов доставки материалов по объектам и распределением курьеров по маршрутам с доставкой документов, необходимо использовать СУБД, способные эффективно работать с графовыми структурами и быстро обрабатывать запросы на поиск кратчайших путей.
Одним из примеров такой СУБД может быть графовая СУБД, такая как Neo4j или OrientDB. Они предоставляют специальные алгоритмы для работы с графами, что позволяет быстро выполнять запросы на поиск кратчайших путей и другие операции над графами.
Также возможно использование реляционной СУБД, такой как PostgreSQL



---

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы 
транзакция завершилась успешно. Ориентируйтесь на шесть действий.

1.  Проверка счета на наличие нужной суммы.
2.  Ввод номера телефона. 
3.  Подтверждение номера телефона. 
4.  Ввод суммы. 
5.  Подтверждение оплаты. 
6.  Проверка баланса телефона,необходимая сумма должна быть на счету телефона.



---

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 

1. Структурированные данные.
2. Более высокая консистентность данных.
3. Более простой язык запросов.
4. Более надежная поддержка транзакций.
5. Лучшая поддержка аналитических запросов.




---

### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу 
выделено 1000 машин. 

Для данной ситуации следует выбирать СУБД, которая поддерживает горизонтальное масштабирование (широкое распределение данных на несколько серверов). Один из основных критериев - это возможность эффективного обработки и хранения большого объема данных. При этом важно, чтобы СУБД имела высокую производительность и надежность.

Что касается модели "распределенных вычислений", то здесь лучше всего подойдет модель MapReduce. Эта модель позволяет производить параллельную обработку большого количества данных, которые разбиваются на множество блоков и распределяются по разным серверам. Затем каждый сервер выполняет свою часть работы независимо от других, а результаты объединяются для получения окончательного результата. Это уменьшает время выполнения операций и повышает скорость работы всей системы.

