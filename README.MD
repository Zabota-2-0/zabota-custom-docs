# Правила ведения документации по кастомам
------------
Данный документ описывает правила ведения документация по пользовательским настройкам базы данных Zabota 2.0 отдельных клиентов.

Для каждой клиники требуется создать собственный каталог, имя которого должно соответстветствовать ID клиники. Внутри каталога обязательно необходимо создать ряд MD файлов. Каждый MD файл должен отражать отдельные сущности изменений. Например: visit_directions.MD, order_details.MD и т.д. 

Правила именования MD файлов:
- Допускаются только латинские буквы в нижнем регистре и цифры, а также тире:  a-z 0-9 -.
Например: my-changes.MD, first-patients-01.MD
- Не допускается название только из цифр
- Название должно быть осмысленным
- Слова не должны быть склеяны, для разделения используйте тире
- Не начинайте название файла с цифры
- Не используйте в названиях заглавные буквы

## 1 Правила ведения MD файлов

------------


- Каждый файл должен содержать раздел Описание, в котором описывается предназначение внесенного кастома. Этот раздел должен располагаться в начале документа
- Документ должен содержать подробное описание изменений с уточнением мест изменений. Скрипты импорта, база данных: таблицы, функции, процедуры и т.д

## 2 Правила элементов MD файла

------------


- Заголовок каждого раздела необходимо делать со стилем заголовка #H1
- Заголовок каждого подраздела необходимо делать со стилем заголовка ##H2
- Заголовок не должен содержать точки в конце
- Заголовок не должен содерджать точки после нумерации раздела
- Все элементы списков должны заканчиваться без точки в конце предложения

Ниже будут представлены элементы и их оформления для использования в документации

## 2.1 Изображения

------------

![](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png)

## 2.2 Заголовки

------------
# Заголовок H1
# Заголовок H2


## 2.3 Цитирование

> Цитата


## 2.4 Ссылки

[Ссылка](http://localhost/)

## 2.5 Блоки кода

#### SQL

```SQL
SELECT TOP 1 @ID=d.Doctor_ID
FROM messages m
INNER JOIN records r ON r.parent_id=m.Message_id
INNER JOIN doctors d ON d.FullName LIKE r.content
WHERE r.name LIKE @Key
AND m.xmid=@Xid;
```

#### Delphi

```delphi
ADataTypeConvertors:= TDictionary<TFieldType,TDataTypeToStringConverterCallback>.Create;
RegisterDataTypeToStringConvertor(ftDateTime,ConvertDateTimeToString);
RegisterDataTypeToStringConvertor(ftDate,ConvertDateToString);
RegisterDataTypeToStringConvertor(ftTime,ConvertTimeToString);
RegisterDataTypeToStringConvertor(ftFloat,ConvertFloatToString);
RegisterDataTypeToStringConvertor(ftBCD,ConvertFloatToString);
RegisterDataTypeToStringConvertor(ftFMTBcd,ConvertFloatToString);
RegisterDataTypeToStringConvertor(ftCurrency,ConvertFloatToString);

```

## 2.6 Списки

#### Ненумерованный список (-)

- Item A
- Item B
- Item C
     

#### Ненумерованный список с вложениями
                
+ Item A
+ Item B
    + Item B 1
    + Item B 2
    + Item B 3
+ Item C
    * Item C 1
    * Item C 2
    * Item C 3

#### Нумерованный список
                
1. Item A
2. Item B
3. Item C
                
----
                    
###Таблицы
                    
Первый заголовок  | Второй заголовок
------------- | -------------
Контент  | Контент
Контент  | Контент

----


## Конец