**1. Перечень автоматизируемых сценариев**

*Поиск и открытие нужного курса через главную страницу портала Нетологии*
- Поиск нужного курса через меню "Каталог курсов"

  На главной странице перейти в раздел каталог курсов, далее выбрать направление "Программирование", найти среди выборки профессию "Тестировщик ПО", кликнуть по профессии.
  
- Поиск нужного курса через выборку курсов по направлениям обучения

  На главной странице, найти карточку направления обучения "Программирование", кликнуть по ней. Найти в результатах профессию "Тестировщик ПО", кликнуть на профессию.

 *Набор тест кейсов для случая: Пользователь НЕ авторизован*
 
- Заполнение и отправка формы c валидными данными (HappyPath)

    *Входными данными являются- либо полученные данные по тестовому пользователю, либо данные пользователя созданы самостоятельно*
    - Имя пользователя более 2 символов, на английской или русской раскладке, не содержащие цифровых значений (# Андрей)
    - Номер телефона соответствующий маске +9 (999) 999-99-99 (# +71234567890)
    - Адрес электронной почты соответствует маске email@domain
    
    *Ожидаемым результатом является, получение письма на электронную почту, с описанием выбранного курса и доп. информацией по методам оплаты. Сообщением, что специалист скоро свяжется по указанному в форме номеру телефона.* 
    
- Отправка формы для получения консультации по курсу

    *Входными данными являются- либо полученные данные по тестовому пользователю, либо данные пользователя созданы самостоятельно*
    - Имя пользователя более 2 символов, на английской или русской раскладке, не содержащие цифровых значений (# Андрей)
    - Номер телефона соответствующий маске +9 (999) 999-99-99 (# +71234567890)
    - Адрес электронной почты соответствует маске email@domain

    *Ожидаемым результатом является получение письма на электронную почту, с описанием выбранного курса. Сообщением, что специалист скоро свяжется по указанному в форме номеру телефона.* 

- Проверка поля ИМЯ на невалидные данные

    *Значение, не удовлетворяющию формату по количеству знаков(# менее 2 буквенных символов)*
    
    *Значение, не удовлетворяющию формату, содержащие любые цифровые значения(# 0-9)*
    
    *Значение, не удовлетворяющию формату, содержащие специальные символы(# <,./*)*


- Проверка поля ТЕЛЕФОН на невалидные данные

    *Значение, не удовлетворяющию формату по количеству знаков(# +799911)*
    
    *Значение, не удовлетворяющию формату, содержащие любые буквенные символы(# а-Я,a-Z)*
    
    *Значение, не удовлетворяющию формату, содержащие специальные символы(# <,./*)*

- Проверка поля EMAIL на невалидные данные

    *Заполненное значение, НЕ удовлетворяющие маске для эл.почты- "email@domain" (#netsobaki.com)*
    
    *Заполненное значение, содержащее недопустимые символы или пробелы в адресе (# email @domain)*

 *Набор тест кейсов для случая: Пользователь авторизован*
 
- Отправка формы

    *Входными данными являются- либо полученные данные по тестовому пользователю, либо данные пользователя созданы самостоятельно*
    
    - Имя пользователя более 2 символов, на английской или русской раскладке, не содержащие цифровых значений (# Андрей)
    - Номер телефона соответствующий маске +9 (999) 999-99-99 (# +791234567890)
    - адрес электронной почты соответствует маске email@domain

     *Ожидаемым результатом является получение сообщения, что форма отправлена. Получение письма на электронную почту, с описанием выбранного курса.* 

- Проверка автоматического заполнения формы с данными из профиля пользователя

     *Данные в форме совпадают с данными тестового зарегистрированного пользователя*

- Проверка, что курс добавлен в личном кабинете после заполнения и отправки формы

    *Фиксация появления и совпадения названия выбранного курса в ЛК тестового пользователя*


**2. Перечень используемых инструментов с обоснованием выбора**
- Язык программирования для написания кода автотестов, Java
- Среда разработки по написанию кода, IntelliJ IDEA
- Библиотека *Selenide* для автоматизации тестирования веб форм.
- Библиотека *Rest.assured* в случае если есть возможность отправка API запроса
- DBUtils для фиксации создания заявки на курс или получение консультации
- Инструмент для формирования отчетности по проведенному тестированию, Allure
- В случае наличия готовых user storys, возможное использование библиотеки cucumber, для описания тестов для отчетности
- Библиотека Jakarta Mail для проверки входящих писем

**3. Перечень необходимых разрешений/данных/доступов**
- Разрешение на автоматизированное тестирование сайта 
- User story от менеджера
- Данные для тестового зарегестрированного пользователя (email, номер телефона), если их нет можно ли его создать (профиль).  
- Как проверить факт отправки формы, доступ к БД
- Если есть возможность взаимодействия по API, данные по телу запроса, методы, адрес, формат ответа и т.д 

**4. Перечень и описание возможных рисков при автоматизации**
- Смена формы записи на курс, не актуальные локаторы для автоматизации веб формы
- Смена наименования курса, не актуальные локаторы для автоматизации веб формы
- Удаление данных тестового пользователя
- Обновление сайта, отсутсвие старых локаторов в новой верстке для навигации по порталу

**5. Перечень необходимых специалистов для автоматизации**
- QA Auto инженер

**6. Интервальная оценка с учётом рисков (в часах)**
- 8 часов, дальнейшая поддержка и рефакторинг кода в случае изменения формы или портала
