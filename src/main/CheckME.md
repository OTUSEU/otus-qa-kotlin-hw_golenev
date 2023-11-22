## Научиться работать с основными конструкциями языка и применять их на практике.
* Резюме:
* Задание принимается.
задача курса применять Kotlin вместо Java
* Поэтому предлагаю Ваш код Java преобразовать в котлин: 
1. выделить в дереве пак6ет java
2. выбрать в меню Code/Convert Java file to Kotlin file
3. согласиться что спрашивает - перепишет Java в Kotlin, Java убъет
4. buidl проект и запустить main из пакета Java
5. Должно работать
6. Сверить преобразованный код с Java(удален), с кодом в пакете Kotlin b с кодом в пакете Example
7. По процессу конвертации Java ->  Kotlin есть раздел документации и CodeLab

* Для автоТестера очень примитивный ТестCase

Все таки надо бы разобрать Example из Check или Check2 и выполнить рекомендации внизу
по переводу Вашего решения на DSL - это одна из целей этой работы.

### Описание/Пошаговая инструкция выполнения домашнего задания:
ОК Дан интерфейс interface TestRunner { fun  runTest(steps: T, test: () -> Unit) }. Класс, передаваемый в steps,
содержит методы before*/after*, которые задают предусловия/чистят данные перед/после теста.
Напишите свою реализацию интерфейса TestRunner, а именно:

1. OK.Создайте класс реализующий интерфейс
2. OK.Внутри класса переопределите метод runTest
3. OK.Внутри этого метода необходимо сначала вызвать методы с before* из steps,
   далее прогнать тест (запустить передаваемую функцию test), и после вызвать методы с after* из steps.
4. OK.Вызовы before* и after* нужно обернуть в лог/печать в консоль.
5. Проверьте работоспобоность написанного кода (можно в методе main).
   Код залейте на github. Название репозитория - otus-qa-kotlin-hw, ветка hw01-testrunner.
   В ДЗ отправьте ссылку на pull request.
   Вам потребуется 90-120 минут на выполнения задания.
   Если возникнут сложности, вы всегда можете обсудить их с одногруппниками или задать вопрос преподавателю Slack

### Критерии оценки:
### Критерии приемки:

1. При вызове метода runTest сначала вызываются методы before, далее идет прогон теста, после вызываются методы after
2. Начало и конец каждого шага (пред/постусловия, тест) логируется/выводится в консоль
Оценка:

3. На лекции дан материал вызова через DSL - предлагаю применить.
4. Логирование может быть реализованно через функцию расширения (см лекцию)
5. Т.к. курс по тестированию, то созданный код стоит оттестировать на разные комбинации before, after в т.ч пустой класс
6. Предлагаю разобрать и запустить в Idea код приведенный в example
7. Предлагаю Свой пример доделать по образцу example, запустить и еще раз прислать на проверку
