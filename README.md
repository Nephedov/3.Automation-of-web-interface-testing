# Домашнее задание к занятию «7.3. Jest и Playwright»

## Решения
### Задание 1
* <a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/blob/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/jest/package.json">jest/package.json</a>. - Скрипт запуска.
* <a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/blob/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/jest/jest.config.js">jest/jest.config.js</a>. - Настройки покрытия.
* <a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/blob/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/jest/test/unit/sortByName.test.js">sortByName.test.js</a>. - Тесты.

<a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/tree/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/jest">Репозиторий</a> Jest проекта.

### Задание 2
* <a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/blob/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/playwright/package.json">playwright/package.json</a>. - Скрипт запуска.
* <a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/blob/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/playwright/playwright.config.js">playwright/playwright.config.js</a>. - Конфигурация Playwright.
* <a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/blob/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/playwright/tests/MyTest.spec.js">MyTest.spec.js</a>. - Тесты.
* <a href="https://github.com/netology-code/jsaqa-code/issues/3">Screenshots</a>. - Скриншоты выполнения шагов автотестов.

<a href="https://github.com/Nephedov/jsaqa-code-Nephedov93/tree/a34f0c1fac66d7ae133fba25690391c0a6d5eb35/7.3/playwright">Репозиторий</a> Playwright проекта.

## Что было сделано
* Задание 1
  * В package.json - Дописан скрипт запуска "Jest", оценки покрытия во время проогона тестов.
  * Создан jest.config.js c настройками о покрытии.
  * Дописаны unit-тесты для полного покрытия.
  * Создан .gitignore. Подключены и настроены плагины Eslint, Prettier.
* Задание 2.
  * В package.json - Дописан скрипт запуска "Playwright".
  * Создан playwright.config.js c параметрами запуска тестов.
  * Написаны функциональные автотесты формы авторизации.
  * Добавлены скриншоты для логирования шагов автотестов.
  * Создан .gitignore. Подключены и настроены плагины Eslint, Prettier.

## Задача 1. Jest. Unit-тесты и отчёты

1. Сделайте форк [проекта с лекции](https://github.com/netology-code/jsaqa-code/tree/main/7.3/jest).
2. Добавьте отчёты о покрытии.

Ваши отчёты должны создаваться во время прогона тестов с помощью скрипта. Его нужно добавить в блок со скриптами в файле `package.json`.
    
Скрипт для запуска оценки покрытия должен запускать команду `"jest --collectCoverage"`.

В нашем случае мы хотим:

- проверять покрытие кода во всех файлах с расширениями `.js` и `.jsx`;
- исключать из проверки директорию `"/node_modules/"`;
- исключать из проверки директорию `"/coverage/"`, в которой будут создаваться отчёты.

3. Добавьте желаемые параметры покрытия:
```
"coverageThreshold": {
        "branches": 100,
        "functions": 100,
        "lines": 100
  }
```

4. Запустите тесты с проверкой покрытия.

5. Допишите недостающие тесты для покрытия 100% по всем параметрам.


## Задача 2. UI-тест на Playwright

Нужно протестировать авторизацию на сайте [netology.ru](https://netology.ru/).

1. Подготовьте тестовые данные:

- создайте файл `user.js` и положите в него свой email и password как константы;
- добавьте файл `user.js` в `.gitignore`. 
**Важно.** Проследите, чтобы email и password не попали в ваш репозиторий, иначе ваш проект не пройдёт аудит безопасности, а злоумышленники получат ваши данные.

2. Создайте тест 1 «Успешная авторизация».
Проверьте ожидаемый результат:
- проверьте, что открылась страница [профиля](https://netology.ru/profile);
- удостоверьтесь, что страница профиля открыта, например, проверив элемент `h2` и текст заголовка.

4. Создайте тест 2 «Неуспешная авторизация».
Проверьте результат:
- проверьте текст об ошибке в появившемся блоке.



## Задача 3* (необязательная). Скриншоты.

Усложнённая версия второго задания: нужно добавить автоматические скриншоты для каждого экрана.
