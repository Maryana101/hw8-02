# Домашнее задание к занятию "Что такое DevOps. СI/СD" - Варфоломеева Марьяна

### Задание 1

Все задания были выполнены на виртуальной машине c CentOS 7 из предыдущего  ДЗ (Подъём инфраструктуры в Yandex Cloud).

На ВМ был установлен jenkins и проведены тесты и сборки проекта на go.

Ниже настройки проекта Freestyle Project Jenkins:

 - указана ссылка на гитхаб с проектом
![](./img/4_proj_propetries.png)

 - и команды shell
![](./img/5_proj_propetries.png)

 - в nexus был создан репозиторий:
![](./img/6_nexus_propetries.png)


**Результат выполнения теста и сборки на Jenkins:**
![](./img/1_freestyle_project_build.png)

в nexus был загружен проект с номером сборки:
![](./img/8_nexus_build_num.png)

### Задание 2

Создать pipeline project, подготовить pipeline-скрипт для выполнения теста и сборки проекта.

В настройках проекта добавлен скрипт:
![](./img/9_pipeline_script.png)

**Результат:**
![](./img/10_build_result.png)

в nexus также видно, что сборка обновилась:
![](./img/11_nexus.png)

### Задание 3

Изменить pipeline так, чтобы вместо Docker-образа собирался бинарный go-файл.

В новом pipeline проекте добавлен обновленный скрипт:
![](./img/14_pipeline_scr_raw.png)

**Результат выполнения:**

![](./img/12_jenkins_build.png)

В репозиторий nexus был загружен файл:
![](./img/13_nexus_raw_repo.png)


