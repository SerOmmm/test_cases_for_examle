**Примеры тест-кейсов для сайта сети зоомагазинов "Ле'Муррр"**

<details>
<summary>TK-001: Проверка функционала фильтрации списка адресов зоомагазинов.</summary>

***

**Цель:**
Проверить работу функционала фильтрации адресов на примере отображения всех актуальных магазинов "Ле'Муррр" в г. Санкт-Петербург на станции метро "Старая Деревня"

**Предусловие**:
1.	Открыть сайт https://lemurrr.ru без авторизации пользователя.
2. Выбрать город Санкт-Петербург.
3. Перейти на вкладку "Магазины" (короткая ссылка: https://lemurrr.ru/shops/spb)

**Шаги**:
1.	Раскрыть меню фильтрации «Станция метро».
2.	В строке поиска ввести тестовые данные «Старая Деревня».
3.	В результатах поиска выбрать чек-бокс «Старая Деревня».
4.	Закрыть меню фильтрации.

**ОР**: 
1. Отображена страница МАГАЗИНЫ В Г. САНКТ-ПЕТЕРБУРГ;
2. В заголовке таблицы отображен ключ "Старая Деревня"
3. В таблице отображен список актуальных магазинов в соответствии со скриншотом:

![Адреса](https://github.com/SerOmmm/test_cases_for_examle/blob/main/Screenshot_1.png)

**Окружение**: Google Chrome не ниже версии 120

***

</details>

<details>
<summary>TK-002: Проверка структуры POST-запроса и ответа сервера при выполнении опции "Восстановление пароля".</summary>

***

**Цель:**
Проверить структуру запроса и ответ сервера при выполнении опции "Восстановление пароля".

**Предусловие**:
1.	Открыть сайт https://lemurrr.ru без авторизации пользователя.
2. Выбрать город Санкт-Петербург.

**Шаги**:
1.	На главной странице нажать кнопку "Войти".
2.	В окне авторизации нажать "Забыл пароль?"
3.	В поле ввести валидный номер телефона, например +7(901)121-15-15.
4.	Нажать "Выслать пароль".

**ОР**: 
1. Запрос отправлен на сервер методом POST на URI: https://lemurrr.ru/recovery/password
2. Запрос отправлен в Body в формате Text, структура запроса совпадает со структурой в требованиях. Пример структуры запроса:
```   
   phone=%2B7+(901)+121-15-15&CSRFToken=af60b302-2f52-4c33-b3e1-b3a2d39c9724
```   
3. Статус ответа сервера 200 ОК.

**Окружение**: Google Chrome не ниже версии 120,
               Chrome DevTools.

***

</details>
