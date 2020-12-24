### Домашнее задание №4.2 по теме «Заключительная лекция»
#### Составление плана автоматизации тестирования открытия вклада "Накопилка" 
**Тестируемая функциональность:** открытие вклада "Накопилка"
                                  

Позитивное и негативное функциональное тестирование

**Количество автоматизированных тестов:** 13


## 1 - Перечень автоматизируемых сценариев:
   
    1. Открытие страницы вклада по маршруту "Частным лицам" -> "Накопилка"
    2. Открытие страницы вклада по маршруту "Частным лицам" -> "Вклады" -> "Накопилка":
     a) Открытие страницы заполнения заявки на открытие вклада по маршруту окно "Накопительный счет «Накопилка»" -> кнопка "Заполнить заявку":
     
      1) Заполнение полей ввода "Имя" и "Мобильный телефон" корректными данными, активация чек-бокса "Я согласен(а) на обработку персональных данных", нажатие кнопки "Мы перезвоним"
     
      2) Заполнение поля ввода "Имя" корректными данными, заполнение поля ввода "Мобильный телефон" некорректными данными(одна цифра). Ожидается появление сообщения об ошибке "Проверьте, пожалуйста, номер телефона"
       
      3) Заполнение поля ввода "Имя" корректными данными, заполнение поля ввода "Мобильный телефон" некорректными данными(буква). Ожидается невозможность ввода некорректных данных.
       
      4) Заполнение поля ввода "Имя" корректными данными, заполнение поля ввода "Мобильный телефон" некорректными данными(спецсимвол). Ожидается невозможность ввода некорректных данных.
       
      5) Оставление полей ввода "Имя" и "Мобильный телефон" незаполненными, активация чек-бокса "Я согласен(а) на обработку персональных данных", нажатие кнопки "Мы перезвоним"
       
      6) Оставление полей ввода "Имя" и "Мобильный телефон" незаполненными, чек-бокса "Я согласен(а) на обработку персональных данных" неактивированным, нажатие кнопки "Мы перезвоним"
		
         b) Открытие страницы заполнения заявки на открытие вклада по маршруту окно "Как открыть счет и услугу «Копилка для сдачи»?" -> кнопка "Заполнить заявку":

         1) Нажатие на ссылку всплывающего окна "персональных данных"

         2) Заполнение поля ввода "Имя" корректными данными, оставление поля ввода "Мобильный телефон" незаполненным, активация чек-бокса "Я согласен(а) на обработку персональных данных", нажатие кнопки "Мы перезвоним"

         3) Заполнение поля ввода "Мобильный телефон" корректными данными, оставление поля ввода "Имя" незаполненным, активация чек-бокса "Я согласен(а) на обработку персональных данных", нажатие кнопки "Мы перезвоним"

         4) Заполнение поля ввода "Мобильный телефон" корректными данными, заполнение поля ввода "Имя" некорректными данными(цифра). Ожидается невозможность ввода некорректных данных.

         5) Заполнение поля ввода "Мобильный телефон" корректными данными, заполнение поля ввода "Имя" некорректными данными(спецсимвол). Ожидается невозможность ввода некорректных данных.

         6) Заполнение поля ввода "Мобильный телефон" корректными данными, заполнение поля ввода "Имя" некорректными данными(буквы латинского алфавита). Ожидается невозможность ввода некорректных данных.
		

## 2 - Перечень используемых инструментов с обоснованием выбора:
   * IntelliJ IDEA -  интегрированная среда разработки программного обеспечения.Выбрана в связи с установшейся практикой в компании.
   * Java 8 - язык написания авто-тестов. Выбран в связи с установшейся практикой в компании.
   * GitHub - система для хостинга проекта тестирования и его совместной разработки. Выбрана в связи с установшейся практикой в компании.
   * JUnit - платформа для написания автотестов и их запуска. Выбрана в связи с установшейся практикой в компании. 
   * Gradle - система управления зависимостями. Выбрана в связи с установшейся практикой в компании.
     * JavaCodeCoverage - плагин для определения степени покрытия программного кода авто-тестами. Выбрана в связи с установшейся практикой в компании.
     * Lombok - плагин для добавления дополнительных аннотаций. Выбран для сокращения временных затрат при написании авто-тестов.
   * Selenide - фреймворк для автоматизированного тестирования веб-приложений.  Выбран для сокращения временных затрат при написании авто-тестов.
   * Allure - фреймворк для составления отчетности при проведении автоматизированного тестирования. Выбран для мониторинга результатов тестирования, 
              с целью сокращения временных затрат при развертывании системы мониторинга.

## 3 - Перечень необходимых разрешений/данных/доступов от банка:
     * Предоставить сервисный доступ к SUT 

## 4 - Перечень и описание возможных рисков при автоматизации:
      * Увеличение затрачиваемого временного ресурса из-за необходимости поддерживать и актуализировать сервисный доступ 
	  * Вероятность получения сервисного доступа злоумышленниками

## 5 - Перечень необходимых специалистов для автоматизации:
      1. Инженер по автоматизированному тестированию - 1 чел.(разработка и поддержка авто-тестов)
      2. Разработчик - 1 чел.(поддержка сервисного доступа)
      3. Специалист по безопасности - 1 чел.(защита сервисного доступа)

## 6 - Интервальная оценка с учётом рисков (в часах):
      1. Подготовка тестовой среды, настройка инструментов - 5 часа
      2. Подготовка тестовых данных(написание вспомогательных классов(Datahelper и т.п.), создание PageObject и т.п. ) - 5 часа
      3. Написание авто-тестов - 1 час на 1 авто-тест, количество автотестов - 11 шт.
      4. Пилотный прогон авто-тестов - 3 часа.
      5. Повысительный коэффициент учета рисков - 1.5
	  
	  Временные затраты, требуемые для проведения автоматизации тестирования:
	  
	  t = (5+5+(1х13)+3)х1.5 = 39 часов
	  
## Примечания:
   1. Авто-тесты разделены на две половины, т.к. по информации от Заказчика маршруты "окно "Накопительный счет «Накопилка»" -> кнопка "Заполнить заявку"" и "окно "Как открыть счет и услугу «Копилка для сдачи»?" -> кнопка "Заполнить заявку"" являются равными по популярности. 
