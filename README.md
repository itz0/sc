# Программа для сравнения двух строк String compare
​

## Что делает эта программа, какой принцип работы?

эта консольная программа позволяет быстро сравнить 2 текстовые строки и получить на выходе **процент** совпадения строк

## Для кого эта программа?

для фрилансеров

## Системные требования и ограничения программы

программа гарантированно работает на ОС Windows 10 x64 

## По поводу вирусов, троянов и закрытого кода

данная программа гарантированно ***мною*** не содержит в себе вирусов, троянов и прочего малваря, кто сомневается можете запускать из песочницы, написана на чистом питоне и скомпилирована на gcc последних версий.

## Состав дистрибутива программы

в дистрибутив программы входит два файла и необходимые для работы программы:

- **string_compare-1.0-first_release.exe** - исполняемый файл программы

- **strings.xlsx** - файл пример для демонстрации работы программы и правильного оформления запросов строк для сравнения

## Руководство по использованию программы (данная инструкция предназначена только для первой версии программы 1.0.0.0):

1. Скачайте и распакуйте архив с программой из [релизов](https://github.com/itz0/sc/releases/)
2. Ознакомьтесь с форматом заполнения файла запроса **strings.xlsx**
3. Запустите исполняемый файл **string_compare-1.0-first_release.exe** дождитесь окончания работы программы, следуя сообщениям вывода консоли
4. Проверьте результат в полученном файле **string_compare.xlsx**

# Известные баги:


Если среди строк в файле **strings.xlsx** отправленных на сравнение будут найдены символы в кодировке unicode, в основном это специфичные латинские символы и другие,
программа может внезапно закрытся в таком случае рекомендуется проверить файл **strings_compare.csv** который программа генерирует в процессе своей работы, пролистать его до конца и сохранить идентификатор **goods_id** последней полученной строки, далее открыть файл **strings.xlsx** используя идентификатор goods_id найти последнюю обработанную строку и удалить последующую строку, сравнив её отдельно в ручную, так как именно из неё программа и закрылась, подобное решение рекомендуется применять всегда когда программа закрывается при сравнении строк.
