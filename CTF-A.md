# Кружок CTF для старших классов

## Эпик

Прочувствовать компьютерную безопасность со всех ее сторон - как с позиции защищающегося, так и с позиции атакующего.

## Путь

Создание серверов с уязвимостями, их эксплуатация а затем устранение.

## Сторис

__Общее ТЗ:__

Веб-страничка с возможностью ввода пользоовательских данных, например, логина и пароля для авторизации. На сервере на базе пользовательских данных формируется запрос и возвращается информация о том, существует ли пользователь с таким логином и паролем, и, если существует, то вернуть его данные - имя, фамилию, дату рождения в формате ``дд.мм.гггг`` логин и захешированный пароль.

### Беззащитная база данных

__ТЗ атаки:__

Достать из базы данных всех пользователей с их именами, фамилиями, датами рождения в формате ``дд.мм.гггг``, логинами и хешами паролей.

### Радужные таблицы

__ТЗ атаки:__

Имея базу данных из [стори 1](#беззащитная-база-данных) создать радужную таблицу всех возможных паролей длины 6 (в пароле могут быть использованы только строчные буквы английского алфавита и цифры).

Используя эту таблицу найти совпадения с паролями из базы данных  из [стори 1](#беззащитная-база-данных) и состаивть список пользователей, состоящий из логинов и "чистых" паролей.

### Психология паролей

__ТЗ атаки:__

Имея базу данных из [стори 1](#беззащитная-база-данных) сформировать радужную таблицу из паролей, основанных на личных данных пользователей (см. ТЗ). На основе одной единицы пользовательских данных, должно быть сформировано ``>= n!`` паролей, где ``n`` - количество единиц пользовательских данных (логин, фамилия, имя, дата рождения). 

На основе сформированной таблицы найти совпадения с паролями из базы данных  из [стори 1](#беззащитная-база-данных) и состаивть список пользователей, состоящий из логинов и "чистых" паролей. Объединить этот список из [стори 2](#радужные-таблицы)

### Дополнительная стори

Защитить сервер от атак из стори 2-3.
