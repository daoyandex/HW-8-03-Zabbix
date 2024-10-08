# Домашнее задание к занятию "`Занятие 8-03 Zabbix, часть 2`" - `Алексеев Александр`

### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1 Создайте свой шаблон, в котором будут элементы данных, мониторящие загрузку CPU и RAM хоста.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
В веб-интерфейсе Zabbix Servera в разделе Templates создайте новый шаблон
Создайте Item который будет собирать информацию об загрузке CPU в процентах
Создайте Item который будет собирать информацию об загрузке RAM в процентах
Требования к результату
Прикрепите в файл README.md скриншот страницы шаблона с названием «Задание 1»

![My Linux by Zabbix agent Template with system.cpu.util и vm.memory.size[pavailable]](img/HW-8-03_2_Zabbix_scr_My_Linux_by_Zabbix_agent_Template.png)
![My Linux by Zabbix agent Template with vm.memory.size[pavailable]](img/HW-8-03-Z-2-my-template-mem.png)
![My Linux by Zabbix agent Template with system.cpu.util](img/HW-8-03-Z-2-my-template-cpu.png)

---

### Задание 2 Добавьте в Zabbix два хоста и задайте им имена <фамилия и инициалы-1> и <фамилия и инициалы-2>. Например: ivanovii-1 и ivanovii-2.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Установите Zabbix Agent на 2 виртмашины, одной из них может быть ваш Zabbix Server
Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов
Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera
Прикрепите за каждым хостом шаблон Linux by Zabbix Agent
Проверьте что в разделе Latest Data начали появляться данные с добавленных агентов

![2 new hosts](img/HW-8-03_2-Z-2-new-hosts.png)

---

### Задание 3 Привяжите созданный шаблон к двум хостам. Также привяжите к обоим хостам шаблон Linux by Zabbix Agent.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
Зайдите в настройки каждого хоста и в разделе Templates прикрепите к этому хосту ваш шаблон
Так же к каждому хосту привяжите шаблон Linux by Zabbix Agent
Проверьте что в раздел Latest Data начали поступать необходимые данные из вашего шаблона
Требования к результату
Прикрепите в файл README.md скриншот страницы хостов, где будут видны привязки шаблонов с названиями «Задание 2-3». Хосты должны иметь зелёный статус подключения

![Latest data of "My Linux by Zabbix agent" Template onto 2 new hosts](img/HW-8-03_2-Z-Latest-data-from-2-new-hosts.png)

---

### Задание 4 Создайте свой кастомный дашборд.

Процесс выполнения
Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
В разделе Dashboards создайте новый дашборд
Разместите на нём несколько графиков на ваше усмотрение.
Требования к результату
Прикрепите в файл README.md скриншот дашборда с названием «Задание 4»

![My New Dashboard with data from 2 new hosts](img/HW-8-03_2-Z-My_New-Dashboard.png)

---

### Задание 5* со звёздочкой

Создайте карту и расположите на ней два своих хоста.
Процесс выполнения
Настройте между хостами линк.
Привяжите к линку триггер, связанный с agent.ping одного из хостов, и установите индикатором сработавшего триггера красную пунктирную линию.
Выключите хост, чей триггер добавлен в линк. Дождитесь срабатывания триггера.
Требования к результату
Прикрепите в файл README.md скриншот карты, где видно, что триггер сработал, с названием «Задание 5»

---

### Задание 6* со звёздочкой

Создайте UserParameter на bash и прикрепите его к созданному вами ранее шаблону. Он должен вызывать скрипт, который:
при получении 1 будет возвращать ваши ФИО,
при получении 2 будет возвращать текущую дату.
Требования к результату
Прикрепите в файл README.md код скрипта, а также скриншот Latest data с результатом работы скрипта на bash, чтобы был виден результат работы скрипта при отправке в него 1 и 2

---

### Задание 7* со звёздочкой

Доработайте Python-скрипт из лекции, создайте для него UserParameter и прикрепите его к созданному вами ранее шаблону. Скрипт должен:
при получении 1 возвращать ваши ФИО,
при получении 2 возвращать текущую дату,
делать всё, что делал скрипт из лекции.
Прикрепите в файл README.md код скрипта в Git. Приложите в Git скриншот Latest data с результатом работы скрипта на Python, чтобы были видны результаты работы скрипта при отправке в него 1, 2, -ping, а также -simple_print.*

---

### Задание 8* со звёздочкой

Настройте автообнаружение и прикрепление к хостам созданного вами ранее шаблона.
Требования к результату
Прикрепите в файл README.md скриншот правила обнаружения, а также скриншот страницы Discover, где видны оба хоста.*

---

### Задание 9* со звёздочкой

Доработайте скрипты Vagrant для 2-х агентов, чтобы они были готовы к автообнаружению сервером, а также имели на борту разработанные вами ранее параметры пользователей.
Приложите в GitHub файлы Vagrantfile и zabbix-agent.sh.*

---