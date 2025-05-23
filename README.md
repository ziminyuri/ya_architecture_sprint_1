# Задание № 1

Вам нужно разделить проект Mesto на несколько микрофронтендов. Самостоятельно решите, какой фреймворк будете использовать, — Module Federation или Single SPA.

## Функциональность Mesto:

- Загрузка фотографий
- Удаление фотографий
- Сбор и учет лайков под фото
- Создание профиля и его редактирование

## Основные компоненты:
В соответсвии с основными бизнес-функциями предлагаю разбивку на 3 микрофронтенда и хост приложение:
1. Profile - Профиль и его редактирование
2. Places - Лента фотографий (CRUD) и учет лайков
3. Auth - Авторизация/Регистрация
4. Host - Хост приложение, которое объединяет в себе микрофронтенды.

## Выбор подхода
Выбираем между:
- Single SPA (SSPA).
- Webpack Module Federation (WMF)

### Обоснование выбора WMF:
- Однородный технологический стек: Все компоненты Mesto написаны на React.
- Наличие общих модулей: Проект использует общие компоненты и утилиты.
- Преимущества WMF: WMF позволяет создавать переиспользуемые модули и эффективно разделять код между микрофронтендами, что особенно важно в данном сценарии. SSPA лучше подходит для объединения приложений, написанных на разных фреймворках.

### Обоснование архитектурного решения:
Выбранный подход позволит разработать микрофронтенды как независимо развертываемые приложения, которые будут интегрированы в общее корневое приложение (host). Благодаря использованию WMF, мы сможем переиспользовать общие компоненты и утилиты, снижая дублирование кода и упрощая поддержку. Существующая структура проекта, с одной главной страницей, идеально подходит для использования в качестве корневого приложения, объединяющего микрофронтенды для профиля, фотографий и аутентификации.

#### Метод интеграции: Run Time (объединяем микрофронтенды в момент выполнения).
#### Метод композиции: клиентская

Работа выполнена на уровнях 1-2 (планирование и проектирование изменений).

# Задание 2
Разделение монолита на микросервисы
Диаграмма arch_template_task2.drawio лежит в корне репо. 