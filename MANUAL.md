** MANUAL
* Настроить зависимости в проекте gradle (Logging.log4j)
![image](https://github.com/user-attachments/assets/eea53a8e-8524-4e73-95b4-112298398af5)
* добавить файл в папку resources файл log4j (см. код в репо)
* поднять контейнер командой docker compose up
* зайти в учетку report portal под аккаунтом администратора ( superadmin\erebus)
* перехожу в report portal http://localhost:8080/
* далее необходимо создать проект, приглосить пользователя default (default\1q2w3e)
* зайти в аккаунт пользователя default в раздел профиль > параметры конфигурации
* скопировать содержимое REQUIRED в файл reportportal.properties ( нужно сгенерировать api ключ и встать в файл)
  ![image](https://github.com/user-attachments/assets/3d348737-1e73-40ab-b45b-b7d5664c6658)

* файл поместить в папку resources)
* Есть два варианта, как вы можете включить расширение ReportPortal в своих тестах: Путем указания @ExtendWith аннотации и по расположению службы (я выбрал 2й вариант)
* для подключения по аннотации нужно создать папку /META-INF/services и положить туда файл org.junit.jupiter.api.extension.Extension с содержимым ( com.epam.reportportal.junit5.ReportPortalExtension )
![image](https://github.com/user-attachments/assets/efd3fdd8-fd68-4ab7-8129-010b88b6014d)
* после чего,заускаю SUT и запустить тесты 
* в вкладке launches мы увидим логи
  ![image](https://github.com/user-attachments/assets/b056eb62-b2f2-4bcd-992d-ef6caf5932f3)
  ![image](https://github.com/user-attachments/assets/5ebcbe07-881a-48e5-8016-0288683d18c0)


