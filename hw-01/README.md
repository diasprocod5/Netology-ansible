1. Попробуйте запустить playbook на окружении из test.yml, зафиксируйте значение, которое имеет факт some_fact для указанного хоста при выполнении playbook.
![task-1](images/task-1.png)
----

2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на all default fact.
![task-2](images/task-2.png)
----
3. Воспользуйтесь подготовленным (используется docker) или создайте собственное окружение для проведения дальнейших испытаний.
![task-3](images/task-3.png)
----
4. Проведите запуск playbook на окружении из prod.yml. Зафиксируйте полученные значения some_fact для каждого из managed host.
![task-4](images/task-4.png)
----
5. Добавьте факты в group_vars каждой из групп хостов так, чтобы для some_fact получились значения: для deb — deb default fact, для el — el default fact.
![task-5](images/task-5.png)
----
6. Повторите запуск playbook на окружении prod.yml. Убедитесь, что выдаются корректные значения для всех хостов.
![task-6](images/task-6.png)
----
7. При помощи ansible-vault зашифруйте факты в group_vars/deb и group_vars/el с паролем netology.
![task-7](images/task-7.png)
----
8. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь в работоспособности.
![task-8](images/task-8.png)
----
9. Посмотрите при помощи ansible-doc список плагинов для подключения. Выберите подходящий для работы на control node.
![task-9](images/task-9.png)
----
10. В prod.yml добавьте новую группу хостов с именем local, в ней разместите localhost с необходимым типом подключения.
![task-10](images/task-10.png)
----
11. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь, что факты some_fact для каждого из хостов определены из верных group_vars.
![task-11](images/task-11.png)