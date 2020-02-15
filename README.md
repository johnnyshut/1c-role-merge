# Объединение ролей в 1С

## Описание

Идея проекта: При использовании RLS часто у заказчика появляется возражение о скорости работы пользователей ограниченных по правам. Типичным решением такой ситуации является - анализ прав и их упрощение, возможно даже до уровня - роль для каждого пользователя. Такая потребность натолкнула на мысль об автоматизации труда программиста.

## Использование

1. В конфигурации создаем роль которая будет хранить результат объединения прав нескольких ролей
2. Выгружаем конфигурацию в файлы
3. Запускаем 1С предприятие в режиме управляемое приложение
4. Открываем обработку "1c-role-merge.epf"
5. В открывшемся окне выбираем путь до "Файл роли приемника" (Созданная нами роль, для версии платформы 8.3.16 пример пути ".\src\Roles\РольПриемник\Ext\Rights.xml")
6. В табличной части указываем пути до файлов прав ролей которые требуется объединить
7. Выполняем команду "Объединить"
8. Загружаем конфигурацию из файлов

[Лицензия](LICENSE.md)

[Договоренности о доработках](CONTRIBUTING.md)

[Проект EDT](.\src)

### TODO

1. Сделать на OScript, чтобы не быть привязанным к 1С предприятию
2. Добавить в обработку визуализацию прав, чтобы при пересечении ограничений на запись можно было интерактивно выбирать нужные нам настройки