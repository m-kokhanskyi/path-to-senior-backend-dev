# Master/Slave реплікація 

### Ціль
 Засвоїти теорії Master/Slave реплікації та синхронізації на практиці.
 Навчитися працювати з проксі для БД
### Вимоги і рекомендації
 - Docker Compose
 - MySQL/PostgresSQL
 - Будь який фреймворк(laravel, nestjs ....)
 - Siege (https://github.com/JoeDog/siege)
 - Прочитати статтю https://shopify.engineering/read-consistency-database-replicas

### Завдання
 1. Підняти три контейнера з БД для db-1, db-2, db-3 (використовуючи mysql або postgresSQL)
 2. На запущених контейнерах налаштувати кластер у вигляді: одного сервера master і двох серверів slaves
 3. Наповнити master даними і перевірити чи працює реплікація
 5. Написати API яке буде виконувати запис в master і одразу запит читання цього запису в slave та використовуючи siege подивитися як часто не буде нових даних на slave і через це буде повертатися помилка
 6. Реалізувати підхід який описаний тут https://shopify.engineering/read-consistency-database-replicas
