# CSDR порядок

[ русский язык | <a href="https://translate.google.com/translate?sl=ru&tl=zh-CN&u=https%3A%2F%2Fgithub.com%2Fit-architector%2Fprojecting.csdr%2Fblob%2Fmaster%2FREADME.md&result=%D0%9F%D0%BE%D0%BB%D1%83%D1%87%D0%B8%D1%82%D1%8C+%D0%BF%D0%B5%D1%80%D0%B5%D0%B2%D0%BE%D0%B4">用中文（表达</a> ]

<h3>Предисловие</h3>

Применяя CSDR порядок (**Conditions, Space, Distribution и Realization**) можно быть уверенным, что код проекта будет конструктивным и применим в любом языке программирования.

![](./Картинки/Энтузиазм-2.jpg)

<h3>Навигация</h3>

Следует учесть несинхронность практики и теории, так как теория иногда писалась из практики, а практика из теории, и что то в итоге оставалось позади. В случае синхрона теории и практики получится стабильный порядок, отчего и будут убраны разделы "теория/практика".

> Теория:

1. <a href="#Проект">Проект</a>

    1.1. <a href="#Замысел">Замысел</a>
    
    1.2. <a href="#Потенциалы">Потенциалы</a>
    
    1.3. <a href="#Компоненты">Компоненты</a>
    
    1.4. <a href="#Стимул">Стимул</a>
    
    1.5. <a href="#Ранжировка">Ранжировка</a>
    
    1.6. <a href="#Содержание">Содержание</a>

2. <a href="#Процессор">Процессор</a>

    2.1. <a href="#Цикл">Цикл</a>
    
    2.2. <a href="#Функционал">Функционал</a>
    
    2.3. <a href="#Роли">Роли</a>

> Практика:


3. <a href="#Код">Код</a>

    3.1. <a href="#Язык-программирования">Язык программирования</a>

    3.2. <a href="#Массив">Массив</a>
    
    3.3. <a href="#Проект">Проект</a>
    
    3.4. <a href="#Конструкции">Конструкции</a>
    
    3.5. <a href="#Рефлексы">Рефлексы</a>
    
    3.6. <a href="#Места">Места</a>
    
    3.7. <a href="#Связи">Связи</a>
    
    3.8. <a href="#Реакции">Реакции</a>
    
    3.9. <a href="#Ресурсы">Ресурсы</a>
    
    3.10. <a href="#Выполнение">Выполнение</a>
    
4. <a href="#Прототип-кода-на-PHP">Прототип кода на PHP</a>
    
    4.1. <a href="#Взаимодействие">Взаимодействие</a>
    
    4.2. <a href="#Многопоточность">Многопоточность</a>
    
    4.3. <a href="#Вариантность">Вариантность</a>
    
5. <a href="#Прототип-кода-на-JS">Прототип кода на JS</a>
    
    5.1. <a href="#Контроль">Контроль</a>
    
    5.2. <a href="#Многопоточность-1">Многопоточность</a>
    
    5.3. <a href="#Вариантность-1">Вариантность</a>
    
    5.4. <a href="#Навигация">Навигация</a>
    
    5.5. <a href="#реакция-pagespeed">Реакция pagespeed</a>
    
6. <a href="#ссылки">Ссылки</a>

![---------------------](./Картинки/hr.png)

<h2>Проект</h2>

<h3>Замысел</h3>

Проект начинается с обозначения необходимых в нём конструкций (вам это знакомо из MVC как model). Для этого нужно обозначить назначение конструкции (например: форум, магазин, анимация при загрузке страницы) и предпочтения к конструкции. Так будет делаться у конструкций проекта: флажок начала работы (назначение) и флажок завершения работы (предпочтение). Собственно это всё, что нужно ожидать от заказчика.

<h3>Потенциалы</h3>

По моим расчётам (и подсказкам таки еврейских братьев) наш мир 4-х-мерный: прошлое (наша опора), будущее (наша среда), объединяющее (таки да, торговля и подарки важны) и настоящее (наши дела). Основавшись на таких знаниях, и признав, что лучшего целостного проектирования, согласованного с ходом нашего времени, для моих устремлений не найти, я вычислил, что разрабатываемый проект (ядро, интерфейс, программа, сайт) нуждается в накоплении 4-х потенциалов: 

1. Права
2. Роли
3. Возможности
4. Способности

И ничего более, или менее.

<h3>Компоненты</h3>

Для накопления потенциалов я спроектировал такие компоненты: Conditions, Space, Distribution и Realization. Зафиксируем их как международную аббревиатуру CSDR. 

![](./Картинки/Дом-2.jpg)

Для удобства изъяснений, сделаю общую картину проекта и его перевод:

1) Conditions, где создаются права проекта -> <b>Рефлексы</b>

> При просмотре всех рефлексов мы можем понять какие внешние события проект обрабатывает, по простому: для чего проект существует.


2) Space, где создаются роли проекта -> <b>Места</b>

> При просмотре мест мы можем понять какие у проекта функции, оболочки, переменные и их значения.


3) Distribution, где создаются возможности проекта -> <b>Связи</b>

> При просмотре связей мы можем понять как заполняется и куда поступают значения переменных.


4) Realization, где создаются способности проекта -> <b>Реакции</b>

> При просмотре реакций мы можем понять логику проекта.

<h3>Стимул</h3>

Для того, чтобы потенциалы накапливались введём ходовой компонент "<b>ресурс</b>".


<h3>Ранжировка</h3>

Рефлексы и места из за своих особенностей (необходимости вложенности) должны выстраиваться гомоархически (в субъекты), а вот связи, реакции и ресурсы гетерархично (в объекты) для завязки на места.

![](./Картинки/Гомоархия%20и%20гетерархия-2.jpg)

<h3>Содержание</h3>

Для каждого компонента так же было выявлено необходимое содержание, дабы каждый компонент смог раскрыть себя полностью и быть применим на любом уровне проекта.

Для <b>рефлексов</b>:
1. Ориентир, где обозначение рефлекса
2. Расчёты, где устанавливается состав задач, обеспечивающих реализацию поставленных целей; уточняется характер взаимосвязи и их основные характеристики; определяются необходимые для решения задач функции обработки данных 
3. Сценарий, где id мест для активации
4. Права, где код регуляции
5. Вложение, где подкатегории рефлексов


Для <b>мест</b>:
1. Смысл, где обозначение места
2. Роль, где обозначение места
3. Связь, где id связи
4. Реакция, где id реакции
5. Ресурс, где id ресурса
6. Вложение, где подкатегории мест


Для <b>связей</b>:
1. Возможности, где массив для импорта значений


Для <b>реакций</b>:
1. Способность, где алгоритм
2. Ресурсы, где входящие ресурсы для способности
3. Результат, где выходящие ресурсы из способности


Для <b>ресурсов</b>: 
1. Информация


![---------------------](./Картинки/hr.png)


<h2>Процессор</h2>

<h3>Цикл</h3>
Проект запускается в виде циклического процесса:

1. Рефлексы активируют места
2. Места активируют связи
3. Связи активируют реакции
4. Реакции активируют рефлексы
и т.д. с самого начала, до тех пор пока есть не активированные рефлексы.

![](./Картинки/4-х%20мерный%20проект%20в%20виде%20CSDR-2.png)

<h3>Функционал</h3>

Выполнять вышеописанный цикл будет функция процессора, в которой будет такой сценарий:

1. **[по запросу: информация о рефлексе] [входящее: {id рефлекса}]** получение {тип рефлекса}, {алгоритм права}, {сценарий ролей}, {id вложенных рефлексов} в рефлексах проекта
2. **[по запросу: проверка прав] [входящее: {алгоритм права}]** проверка успешного выполнения алгоритма права для мест проекта
3. **[по запросу: память ожидания прав] [входящее: {запрос = добавить, проверить, удалить, получить всё}, {id ожидающего рефлекса}]** добавление {id рефлекса}, {алгоритм права} / получить всё {массива ожидания прав} / проверить / удаление в массиве "ожидания прав" у процессора
4. **[по запросу: проверка прав у ожидающих рефлексов]** запрос "*память ожидания прав: получить всё*"
    1. **[есть массив ожидания прав] [цикл]** последовательный запрос "*проверка прав*" по {массива ожидания прав}
        1. **[есть права]** запрос "*активация рефлекса*" с {id ожидающего рефлекса}
5. **[по запросу: информация о месте] [входящее: {id места}]** получение {тип места}, {команда}, {id реакции}, {id связи} в местах проекта
6. **[по запросу: информация о реакции] [входящее: {id реакции}]** получение {тип реакции}, {проект роли}, {функция реакции}, {начальные данные}, {результативные данные}
7. **[по запросу: информация о связи] [входящее: {id связи}]** получение {тип связи}, {массив возможностей} в связях проекта
8. **[по запросу: активация рефлекса] [входящее: {id рефлекса}]** запрос "*информация о рефлексе*" по {id рефлекса}
    1. запрос "*проверка прав*"
    2. **[есть тип ожидание прав единожды / множественно]** запрос "*память ожидания прав: проверить*"
       1. **[нет наличия в массиве ожидания прав]** запрос "*память ожидания прав: добавить*"
       2. **[есть наличие в массиве ожидания прав] [есть права] [есть тип ожидание прав единожды]** запрос "*память ожидания прав: удалить*"
    3. **[есть права] [цикл]** последовательный запрос "*информация о месте*" у мест из {сценарий ролей}
       1. **[ориентация  = контроль]** запрос "*информация о связи*"
            1. запрос "*активация процессора*" с {проектом роли}, {параметры = массив возможностей}
       2. **[ориентация  = хранение]** запрос "*активация процессора*" с {проектом роли}
       3. **[ориентация  = содержимое]** запрос "*активация процессора*" с {проектом роли}, {параметры = вложение места}
       4. **[ориентация  = создание]** запрос "*информация о реакции*"
            1. **[есть функция]** получение {результативные данные} с функции с {параметры = начальные данные}
            2. **[нет функции]** получение {результативные данные} с запроса "*активация процессора*" с {проектом роли}, {параметры = начальные данные}
       5. запрос "*проверка прав у ожидающих рефлексов*"
    3. **[цикл]** последовательный запрос "*активация рефлекса*" с {id рефлекса} во вложении
9. **[по запросу: активация конструкции] [входящее: {конструкция}, {параметры конструкции}] [цикл]** последовательный запрос "*активация рефлекса*"
10. **[по запросу: активация процессора] [входящее: {проект}, {запрос}, {параметры запроса}]** запрос "*активация рефлекса*" с {id рефлекса = 1}
11. запрос "*активация процессора*" с {проектом}

<h3>Роли</h3>

Роль это реализованный CSDR код, который будет дополнять функционал процессора. Обозначаются роли: {названием проекта},  {ориентировкой конструкции} и {конструкцией проекта}.

Пример применения (<a target="_blank" href="https://github.com/it-architector/code.csdr/blob/master/%D0%9A%D0%B0%D1%80%D1%82%D0%B8%D0%BD%D0%BA%D0%B8/%D0%92%D0%B7%D0%B0%D0%B8%D0%BC%D0%BE%D0%B4%D0%B5%D0%B9%D1%81%D1%82%D0%B2%D0%B8%D0%B5%20%D1%8F%D0%B4%D1%80%D0%B0.png?raw=true">открыть в отдельном окне</a>):

![---------------------](./Картинки/Взаимодействие%20ядра.png)

Для начального проектирования (проектов или новых ролей) достаточно **базовых ролей**:

1. Хранение: ролей: любых
> благодаря которой процессор сможет капсулировать роли
2. Содержание: информации: текст
> благодаря которой процессор сможет запоминать информацию
3. Создание: информации: любой
> благодаря которой процессор сможет выполнять логику
5. Контроль: создания: загрузить, передача
> благодаря которой процессор сможет взаимодействовать с реакциями
6. Контроль: процессора: получить параметры, передать ответ
> благодаря которой процессор сможет взаимодействовать с другими процессорами

![---------------------](./Картинки/hr.png)


<h2>Код</h2>

<h3>Язык программирования</h3>

Язык программирования должен иметь массив для хранения данных и функционала (анонимную функцию для выполнения кода по вызову).

<h3>Массив</h3>

Код принято начинать в виде 7-и массивов:

```php
$code['Проект']      = [...];
$code['Конструкции'] = [...];
$code['Рефлексы']    = [...];
$code['Места']       = [...];
$code['Связи']       = [...];
$code['Реакции']     = [...];
$code['Ресурсы']     = [...];
```

<h3>Проект</h3>

**Проект** принято делать фиксировано:

```php
$code['Проект'] = [
    'Название' => '{Название проекта}',
    'Версия' => '{Номер корректировки проекта}'
];
```

<h3>Конструкции</h3>

**Конструкции** принято делать последовательно:

```php
$code['Конструкции'] = [
    '1' => [
        'Назначение'    => '{Назначение 1}',
        'Предпочтение'  => '{Предпочтение 1}',
        'Ориентировка'  => '{Ориентировка 1}',
        'Условия'       => ['{reflex_1}'],
    ],
    '2' => [
        'Назначение'    => '{Назначение 2}',
        'Предпочтение'  => '{Предпочтение 2}',
        'Ориентировка'  => '{Ориентировка 2}',
        'Условия'       => ['{reflex_1.1}','{reflex_1.1.1}','{reflex_1.1.2}'],
    ]
];
```

> Где, назначение это ключевое слово конструкции.
>
> При этом, id рефлексов добавляются в условия тогда, когда проектируются рефлексы.

> Где, предпочтение содержит всю информацию о необходимости конструкции.

> Где, условия это массив id рефлексов, которые созданы для конструкции.

> Где, ориентировка для концентрированного проектирования конструкции и состоит из 4-х вариантов:
1. Хранение
> форма вмещения
> 
> где, варианты вложения у сценария рефлекса: 
> 1. Нет
> 2. Есть, запуск другого рефлекса
>
> где, варианты вложения у места: 
> 1. Есть, роли (шаблон)
>
> где, варианты связи:
> 1. Нет
>
> где, варианты реакции:
> 1. Нет
2. Содержание
> значения формы
> 
> где, варианты вложения у сценария рефлекса: 
> 1. Нет
>
> где, варианты вложения у места: 
> 1. Есть, текст (шаблон)
> 2. Есть, число (шаблон)
> 3. Есть, массив (шаблон)
>
> где, варианты связи:
> 1. Нет
>
> где, варианты реакции:
> 1. Нет
3. Создание
> создание содержания
> 
> где, варианты вложения у сценария рефлекса: 
> 1. Нет
>
> где, варианты вложения у места: 
> 1. Нет
>
> где, варианты связи:
> 1. Нет
>
> где, варианты реакции:
> 1. Есть, редактируемая способность
> 2. Есть, не редактируемая способность
4. Контроль
> отдача и получение содержания
> 
> где, варианты вложения у сценария рефлекса: 
> 1. Нет
>
> где, варианты вложения у места:  
> 1. Нет
>
> где, варианты связи:
> 1. Есть
>
> где, варианты реакции:
> 1. Нет

<h3>Рефлексы</h3>

**Рефлексы** принято делать со вложением:

```php
$code['Рефлексы'] = [
    '1' => [
        'Ориентир'   => '{Рефлекс 1}',
        'Расчёты'    => '{Описание 1}',
        'Сценарий'   => ['{place_id_1.1}','{place_id_1.2}'],
        'Права'      => '{Код условия 1}',
        'Вложение'   => [
            '1.1' => [
                'Ориентир'   => '{Рефлекс 2}',
                'Расчёты'    => '{Описание 2}',
                'Сценарий'   => ['{place_id_3.2.1}','{place_id_3.2.2}'],
                'Права'      => '{Код условия 2}',
                'Вложение'   => [
                     '1.1.1' => [
                           'Ориентир'   => '{Рефлекс 3}',
                           'Расчёты'    => '{Описание 3}',
                            'Сценарий'   => ['{place_id_4}'],
                            'Права'      => false,
                            'Вложение'   => false
                     ],
                ]
            ],
        ]
    ]
];
```

> Каждый вложенный рефлекс будет автоматически активан (запустится сценарий),  в зависимости от проверки прав.

> Где, в сценарии указываются id мест для последовательной активации: array({place_id_1}, {place_id_2}, {place_id_3}, ...).
>
> При этом, id мест добавляются в сценарий тогда, когда реализируются места, в нужной для этого последовательности.


> Где, в права можно добавить код условия (то что заключается в if) для активации сценария. 
> 
> Конструкция: array('вместилище'=>array('вместилище'=>['значение 1','оператор','значение 2'],'вместилище'=>['значение 1','оператор','значение 2']))
> 
> Где, вместилище: 
> 1. для обозначения условия - число
> 2. для обозначения сопоставления "OR" - 'variation'
> 3. для обозначения сопоставления "AND" - 'constant'
> 
> Где, значение 1 и 2: 
> 1. предполагаемое значение места
> 2. значение из места - '{place_id}'
> 3. текст
> 
> Где, оператор: 
> 1. равенство - '='
> 2. больше - '>'
> 3. равно либо больше - '>='
> 4. не равно - '!='
> 5. значение 1 есть в массиве значения 2 - 'in'
> 6. значения 1 нет в массиве значения 2 - 'not in'
> 7. частично равен - '=%'
> 
> При этом, вложенность может быть:
> 1. для одного условия: array('{число}'=>['{значение 1}','{оператор}','{значение 2}'])
> 2. много-вложенным: array('variation'=>array( '{число}'=>['{значение 1}','{оператор}','{значение 2}'], 'constant'=>array( '{число}'=>['{значение 1}','{оператор}','{значение 2}'], 'число'=>['{значение 1}','{оператор}','{значение 2}'] )))
> 
> 
> При этом, обозначения (variation, constant) могут содержать добавочно на конце цифру:
> 
>     'variation'=> array(
>
>     'constant_1'=>array('{число}'=>['{значение 1}','{оператор}','{значение 2}'],'{число}'=>['{значение 1}','{оператор}','{значение 2}']),
>
>     'constant_2'=>array('{число}'=>['значение 1}','{оператор}','{значение 2}'],'{число}'=>['{значение 1}','{оператор}','{значение 2}'])
>
>      )


<h3>Места</h3>

**Места** принято делать со вложением:

```php
$code['Места']    = [
    '{ID 1}' => [
        'Смысл'      => '{Описание 1}',
        'Роль'       => ['{Название роли 1}', '{Ориентировка конструкции роли 1}', '{Конструкция роли 1}'],
        'Связь'      => '{Наличие связи 1}',
        'Реакция'    => '{Наличие реакции 1}',
        'Ресурс'     => '{Наличие ресурса 1}',
        'Вложение'   => [
            '{ID 1.1}' => [
                'Смысл'      => '{Описание 2}',
                'Роль'       => ['{Название роли 1}', '{Ориентировка конструкции роли 1}', '{Конструкция роли 1}'],
                'Связь'      => '{Наличие связи 2}',
                'Реакция'    => '{Наличие реакции 2}',
                'Ресурс'     => '{Наличие ресурса 2}',
                'Вложение'   => [
                    '{ID 1.1.1}' => [
                        'Смысл'      => '{Описание 3}',
                        'Роль'       => ['{Название роли 1}', '{Ориентировка конструкции роли 1}', '{Конструкция роли 1}'],
                        'Связь'      => '{Наличие связи 3}',
                        'Реакция'    => '{Наличие реакции 3}',
                        'Ресурс'     => '{Наличие ресурса 3}',
                        'Вложение'   => false,
                     ],
                    '{ID 1.1.2}' => [
                        'Смысл'      => '{Описание 4}',
                        'Роль'       => ['{Название роли 1}', '{Ориентировка конструкции роли 1}', '{Конструкция роли 1}'],
                        'Связь'      => '{Наличие связи 4}',
                        'Реакция'    => '{Наличие реакции 4}',
                        'Ресурс'     => '{Наличие ресурса 4}',
                        'Вложение'   => false,
                     ],
                ],
            ],
        ]
    ]
];
```

<h3>Связи</h3>

**Связи** принято делать последовательно:

```php
$code['Связи']    = [
    '{ID 1}'  => [
        'Возможности'   => ['{Откуда 1}'=>'{Куда 1}', '{Откуда 2}'=>'{Куда 2}']
    ],
    '{ID 2}'  => [
        'Возможности'   => ['{Откуда 3}'=>'{Куда 3}']
    ],
];
```

> Где, в возможностях массив передачи информации с {откуда} в {куда}. 

<h3>Реакции</h3>

**Реакции** принято делать последовательно:

```php
$code['Реакции']    = [
    '{ID 1}'  => [
        'Ресурсы'      => null,
        'Способность'  => function($opportunities = []){

            /*получаем значения переменных*/
            $var_1 = $opportunities['key 1'];
            $var_2 = $opportunities['key 2'];
            
            /*выполняем трансмутацию*/
            
            $var_new = $var_1 + $var_2;
            
            /*результат*/
            return [
                'key 3' => $var_new,
            ];
        },
        'Результат'    => null
    ],
    '{ID 2}'  => [
        'Ресурсы'      => null,
        'Способность'  => false,
        'Результат'    => null
    ],
];
```

> Где, в ресурсы и результат заполняются по ходу работы.
> 
> Где, способность при false содержится в коде роли. 
> 
> Где, в $opportunities способности = ресурсы. 
> 
> Где, return способности = результат. 


<h3>Ресурсы</h3>

**Ресурсы** принято делать последовательно:

```php
$code['Ресурсы']    = [
    '{ID 1}'  => [
      'Информация' => '{Значение 1}'
    ],
    '{ID 2}'  => [
      'Информация' => '{Значение 2}'
    ],
];
```

<h3>Выполнение</h3>

Для выполнения кода добавим функцию процессора и активируем:

```php
$cpu = [
    'Функция' => function($in = ['{код}','{конструкция}','{параметры конструкции}']){...},
    'Роли' => [
         '{название роли}' => '{код}',
    ];

$cpu['Функция']($in = ['{код = $code}','{конструкция = "фоновый запуск"}','{параметры конструкции = ["сделать" => "оптимизацию базы"]}']);
```



> Где, роли это все применённые в проекте роли.

> Где, у ролей параметры конструкции:
> 1. категория хранения: -
> 2. категория содержания: вложение места
> 3. категория создания: вложение реакции
> 4. категория контроля: вложение связи


![---------------------](./Картинки/hr.png)

<h2>Прототип кода на PHP</h2>

Для потверждения работоспособности порядка в ядре были наскоро собраны практические прототипы на PHP.

<h3>Взаимодействие</h3>

Установим цель такую: на внешний запрос ("x" и "y") выдать результат "z", рассчитанный по формуле x + y = z.

Спланируем проект (стрелками обозначим влияние / активацию):

![](./Картинки/Планировка%20php%20проекта-2.png)

<a href="https://www.youtube.com/watch?v=SW-4kUMS27M&feature=youtu.be">Видео планировки</a>

Результат: <a href="./PHP/Взаимодействие.php">Код взаимодействия</a> (<a href="https://framework-csdr.ru/samples/PHP/Взаимодействие.php?x=2&y=6">запустить вариант 2 + 6</a>).

<h3>Многопоточность</h3>

Ход работы: На вход дадим массив из вариантов "x" и "y" и последовательно выведем результат в ответ.

Результат: <a href="./PHP/Многопоточность.php">Код многопоточности</a> (<a href="https://framework-csdr.ru/samples/PHP/Многопоточность.php?data_x_y[1][x]=3&data_x_y[1][y]=7&data_x_y[2][x]=12&data_x_y[2][y]=5&data_x_y[3][x]=6&data_x_y[3][y]=6">запустить вариант (3 + 7, 12 + 5, 6 + 6)</a>).

<h3>Вариантность</h3>

Ход работы: На вход дадим переменную "kill" и в зависимости от её значения дадим ответ.

Результат: <a href="./PHP/Вариантность.php">Код вариантности</a> (<a href="https://framework-csdr.ru/samples/PHP/Вариантность.php?kill=false">запустить вариант kill=false</a>, <a href="https://framework-csdr.ru/samples/PHP/Вариантность.php?kill=true">вариант kill=true</a>).

![---------------------](./Картинки/hr.png)

<h2>Прототип кода на JS</h2>

Для потверждения работоспособности порядка в интерфейсе были наскоро собраны практические прототипы на JS.

<h3>Контроль</h3>

 - развёртка html
 - наполнение содержимым
 - установка стиля
 - установка favicon
 - смена текста по нажатию на тэг
 - показ подсказки по наведению (и отведению) на тэг

Результат: <a href="./JS/Контроль.html">Код контроля</a> (<a href="https://framework-csdr.ru/samples/JS/Контроль.html">открыть на хостинге</a>).

<h3>Многопоточность</h3>

Ход работы: На вход дадим массив с вариантами "id" и "текст" и последовательно на основе полученных данных выведем ссылки в браузер.

Результат: <a href="./JS/Многопоточность.html">Код многопоточности</a> (<a href="https://framework-csdr.ru/samples/JS/Многопоточность.html">открыть на хостинге</a>).

<h3>Вариантность</h3>

Ход работы: Выведем ссылки меню и в зависимости от "id" из браузера активируем открытую ссылку из меню.

Результат: <a href="./JS/Вариантность.html">Код вариантности</a> (<a href="https://framework-csdr.ru/samples/JS/Вариантность.html">открыть на хостинге</a>).

<h3>Навигация</h3>

Ход работы: Выведем ссылки меню и в зависимости от "id" из браузера активируем открытую ссылку из меню, без перезагрузки страницы, но меняя открытую ссылку в браузере.

Результат: <a href="./JS/Навигация.html">Код навигации</a> (<a href="https://framework-csdr.ru/samples/JS/Навигация.html">открыть на хостинге</a>).

<h3>Реакция pagespeed</h3>

Для тестирования у <a href="https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fframework-csdr.ru%2F">google pagespeed</a> была создана стандартная страница, со всеми графическим наворотами: https://framework-csdr.ru/index.html

Результат проверки:

![](./Картинки/pagespeed/pagespeed_1.png)

![](./Картинки/pagespeed/pagespeed_3.png)

![](./Картинки/pagespeed/pagespeed_2.png)

![](./Картинки/pagespeed/pagespeed_4.png)

![---------------------](./Картинки/hr.png)

<h2>Ссылки</h2>

Материал по теме: 

![](./Картинки/Общение.png) <a target="_blank" href="https://www.youtube.com/watch?v=VgH-R3puQes">Ефим Гринкруг: что такое программная инженерия / проектирование</a><br>
![](./Картинки/Общение.png) <a target="_blank" href="https://www.youtube.com/watch?v=fwlNqJudtHk">Юлия Пучнина: использование компонентной архитектуры в веб-приложениях / архитектирование</a><br>
![](./Картинки/Общение.png) <a target="_blank" href="https://www.youtube.com/watch?v=mc7EMdyawBk">Игорь Алексеенко: классические приёмы программирования во фронтенде / дизайнирование</a><br>

Проект поддерживают:

![](./Картинки/поддержка/phpstorm.png) <a target="_blank" href="https://www.jetbrains.com/?from=framework+csdr">JetBrains PhpStorm</a><br>
