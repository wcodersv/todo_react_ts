# ToDo на React TypeScript

### Посмотреть сайт можно справа, под разделом 'About'.


## 👩‍💻 Общее описание:

**Todos** - одностраничное приложение на `React + TypeScript`. Приложение позволяет пользователю добавлять новые задачи, отмечать их как выполненные и удалять завершенные задачи. Также доступна фильтрация задач по статусу: все задачи, активные задачи (невыполненные) и выполненные задачи. Пользователь может управлять списком задач и видеть сводку о количестве выполненных задач.


## Тестовое задание:
#### Сделайте ToDo-приложение, позволяющее управлять текущим списком дел
Что должно быть в интерфейсе:
* Поле для ввода новой задачи
* Списки всех задач, невыполненных и выполненных задач (по отдельности)

#### Требования к коду:
* Создано с исползованием React и React Hooks
* Библиотеки компонент – на ваше усмотрение
* Ключевая на ваш взгляд функциональность покрыта тестами
* Проект должен запускаться командой
   ```bash
   npm i && npm run start
   ```

## 📌 Функциональность:
Основными функциями этого кода являются создание и управление TODO-листом в веб-приложении с использованием библиотеки React. Вот основные функции, которые решает этот код:

1. Создание и отображение задач:
   - Пользователь может вводить новые задачи в поле ввода и добавлять их в список при нажатии на "Enter".

2. Отметка задач как выполненных или не выполненных:
   - Пользователь может отмечать задачи как выполненные или снова как не выполненные, кликая на соответствующий флажок.

3. Фильтрация задач:
   - Пользователь может просматривать задачи в различных режимах фильтрации: "все", "активные" и "выполненные".
   - Функции `showAllTasks`, `showActiveTasks` и `showCompletedTasks` позволяют переключаться между фильтрами.

4. Сохранение данных:
   - Состояние списка задач автоматически сохраняется в `LocalStorage` при каждом изменении.
   - При загрузке приложения из `LocalStorage` восстанавливается предыдущее состояние задач.

5. Удаление выполненных задач:
   - Пользователь может удалить все выполненные задачи с помощью кнопки "Clear completed".


## 📋 Технические детали:

- Использование `React` для создания компонентов и построения пользовательского интерфейса.

- Использование `useState` для управления состоянием приложения, включая хранение состояния `todos` (списка задач) и `currentFilter` (текущего фильтра задач).

- Использование `useEffect` для выполнения побочных эффектов, таких как сохранение состояния задач в `LocalStorage`.

- Использование `localStorage` для хранения данных задач на стороне клиента.

- Использование `useRef` для создания ссылки на элемент DOM и установки фокуса на поле ввода при загрузке страницы.

- Использование структурированного подхода к созданию компонентов с отдельными файлами для каждого компонента (например, `InputField.tsx`, `TodoItem.tsx`, `TaskSummary.tsx`, и `Button.tsx`).

- Использование стилей CSS (например, `module.css`) для стилизации компонентов и элементов интерфейса пользователя.


## 🧪 Тестирование
Функциональность покрыта тестами, команды запуска:

- запустить тесты:
   ```bash
   npm run test
   ```

- запустить тесты с созданием отчета покрытия:
   ```bash
   npm run test -- --coverage --watchAll
   ```

<details>
<summary><b> Тестовые сценарии </b></summary>

1. Добавление задачи

   - Цель: Проверить, что новая задача успешно добавляется в список после ввода и нажатия клавиши Enter.

2. Изменение статуса выполнения задачи

   - Цель: Проверить, что статус задачи изменяется правильно

3. Фильтрация задач
   - Цель: Гарантировать, что фильтры задач работают корректно и отображают задачи в соответствии с выбранным фильтром.
   - Тесты:
     - "Active" фильтр: Проверка, что только активные задачи отображаются.
     - "Completed" фильтр: Проверка, что только завершенные задачи отображаются.
     - "All" фильтр: Проверка, что все задачи отображаются.

4. Удаление завершенных задач
   - Цель: Проверить, что при нажатии на кнопку "Clear completed" все завершенные задачи удаляются из списка.
</details>
