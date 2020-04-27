# Отчёт о тестировании установки OpenJDK11 и приложение KeyValidator

## Краткое описание

27.04.2020 - <Дата окончания> было проведено тестирование установки , запуска по инструкции приложения OpenJDK11 и проверки в нем приложение KeyValidator.

На тестирование затрачено: 2 час

В результате тестирования выявлены следующие дефекты:
* в инструкции показан пример с валидным и невалидным ключом, оба ключа невалидны 
* в валидных ключах для проверки - есть невалидные 
* в невалидных ключах для проверки - есть валидные

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* в [легенде](https://github.com/netology-code/javaqa-homeworks/tree/master/intro) дается тест план;
* Два тест-кейса: проверка валидных ключей, проверка невалидных ключей.
* баг-репорт


В качестве тестовых данных использовались данные:
* [инструкция](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md) по установке OpenJDK11 

Ожидаемый результат:

После установки отурываем терминал и вводим:
```shell script
java -version
```
Терминал на покажет:
```
openjdk version "11.0.5" 2019-10-15
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.5+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.5+10, mixed mode)
```
* [Руководство использования KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md)  в нем содержится приложение [KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/artifacts/KeyValidator.class)

Ожидаемый результат: 

После ввода ключей для валидацивывод приложения будет выглядеть следующим образом:
```shell script
Result for 00000000-0000-0000-0000-000000000000: OK
Result for 00000000-0000-0000-0000-000000000001: FAIL
```



Тестирование производилось в следующем окружении:
* windows 7 x64
* Java 11
* git version 2.26.0.windows.1