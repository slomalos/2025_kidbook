# Отчет по лабораторной работе

## Состав команды

| ФИО         | Что делал                                                                                                    | Оценка |
| ----------- | ------------------------------------------------------------------------------------------------------------ | ------ |
| Юсуфов Р.Г. | Сбор информации, 7 терминов, редактирование, проставление ссылок, создание онтологии, написание отчёта       |        |
| Васин. Г.А. | Сбор информации, 8 терминов, работа с генерацией Gigachat, валидация результатов генерации, написание отчёта |        |


## ## Концептуализация предметной области

В процессе работы над созданием вики по мультипликации и анимации для детей была проведена концептуализация предметной области. Основная цель этого этапа заключалась в структурировании знаний, выделении ключевых понятий и установлении их взаимосвязей для последующего наполнения базы данных.

#### **Методы и инструменты**

Для концептуализации использовались следующие методы и инструменты:

- **Анализ существующих источников**: изучение открытых образовательных ресурсов, детских энциклопедий и специализированной литературы по мультипликации и анимации в т.ч. WikiData.
- **Генерация информации с помощью нейросети Gigachat**: использование ИИ для быстрого сбора и структурирования данных по тематике.
- **Создание онтологии**: формирование системы понятий и их связей, что позволило организовать информацию логично и последовательно.
- **Графическое представление**: построение диаграмм взаимосвязей с помощью инструментов типа Obsidian и Miro для наглядного отображения структуры знаний.

В ходе концептуализации была сформирована базовая структура знаний, включающая ключевые понятия, которая легла в основу наполнения вики.
## Написание текстов

Для написания текстов использовался **программный метод с помощью API нейросети Gigachat**. Это позволило автоматизировать процесс генерации контента, обеспечив единый стиль подачи информации и структурированность статей.
#### **Автоматизация генерации контента**
Мы написали скрипт на Python, который:

1. **Определял список ключевых понятий** из мира анимации.
2. **Формировал промпт**, адаптированный для детской аудитории.
3. **Запрашивал текст через API Gigachat**.
4. **Сохранял результат в формате Markdown**, создавая отдельные файлы для каждого понятия.
#### **Структура промпта**

Промпт был разработан так, чтобы тексты получались интересными, увлекательными и адаптированными для детей 10-12 лет. В него входили:
- **Простые и яркие объяснения** (сравнения, метафоры).
- **Примеры из известных мультфильмов** (Disney, Pixar, DreamWorks).
- **Интерактивные элементы** (воображаемые эксперименты, задания).
- **Практические советы** (как попробовать создать анимацию самому).
- **Перекрёстные ссылки** на другие понятия для удобной навигации.
Пример промпта:

> **"Ты – эксперт по анимации с талантом объяснять сложное детям 10-12 лет..."**  
> **"Создай увлекательное объяснение понятия, используя..."**  
> **"Обязательно добавь разделы: Определение, Как это работает?, Пример из мультфильма, Попробуй сам!"**

Дополнительно, для некоторых понятий добавлялись **специальные указания**:
- Для **"Мультфильм"** — пояснить разницу между 2D и 3D анимацией.
- Для **"Скелетная анимация"** — использовать аналогию с марионеткой.
#### **Проставление ссылок**

Перекрёстные ссылки формировались автоматически:
- В каждом тексте указывались **связанные термины**, которые связывали статьи между собой.
- Например, статья о **"Раскадровке"** содержала ссылки на **"Фреймрейт"** и **"Аниматик"**.
- Markdown-разметка позволяла легко интегрировать эти ссылки в вики.
Конечно же эти ссылки были сырыми, содержали ошибки и в целом были неудобными. Поэтому пришлось редактировать и рефакторить ручным трудом.
## Выводы

В ходе выполнения работы мы столкнулись со следующими трудностями:
**1. Качество текстов от нейросети**  
_Проблема:_ Gigachat не всегда генерировал идеально адаптированные для детей тексты. Иногда получались слишком сложные формулировки или, наоборот, слишком упрощённые.
_Решение:_
- Добавили кастомные инструкции для сложных терминов (например, «Скелетная анимация» — объяснять через аналогию с марионеткой).
- При необходимости вручную редактировали тексты перед финальной загрузкой.

**2. Автоматическая генерация ссылок**  
_Проблема:_ Не всегда удавалось корректно вставить ссылки на связанные понятия. Иногда термины пересекались неочевидным образом.

_Решение:_
- Создали список понятий и заранее прописали, какие термины логично связывать между собой.
- В коде настроили автоматическое исключение текущего термина из списка связанных, чтобы избежать дублирования.
- В дальнейшем можно улучшить логику, добавив более гибкий алгоритм связи статей.

**3. Баланс между увлекательностью и информативностью**  
_Проблема:_ Часть статей была либо слишком технической, либо слишком «развлекательной», не давая достаточного объяснения.
_Решение:_
- Ввели обязательные разделы: «Как это работает?», «Пример из мультфильма», «Попробуй сам!».
- Использовали эмодзи и игровые элементы, но не в ущерб смыслу.
- В некоторых случаях добавляли интерактивные элементы («Представь, что ты аниматор…»).
#### **Что получилось хорошо?**

**Чёткая структура вики** – статьи логично связаны, легко навигировать.  
**Понятные объяснения** – тексты адаптированы для детей, без перегрузки сложными терминами.  
**Автоматизация** – использование API Gigachat позволило ускорить процесс написания.  
**Интерактивность** – игровые элементы делают материал более вовлекающим.

#### **Что можно улучшить?**

🔹 **Добавить иллюстрации** – визуальные примеры помогут детям лучше усвоить информацию.  
🔹 **Уточнить связи между терминами** – использовать более продвинутые методы онтологической разметки.  
🔹 **Тестирование на аудитории** – проверить, насколько детям понятны тексты, и скорректировать стиль.  
🔹 **Дополнить раздел «Попробуй сам!»** – добавить больше практических заданий, например, пошаговые инструкции по созданию анимации.

Проект получился успешным – мы создали **структурированную и доступную вики по анимации**, использовав комбинацию нейросети и ручного редактирования. Автоматизация через API Gigachat значительно ускорила работу, но потребовала тщательной настройки промптов и доработки контента. В дальнейшем можно развивать проект, добавляя иллюстрации, интерактивные элементы и расширяя тематические связи между статьями.