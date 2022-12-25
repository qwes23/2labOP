# **Лабораторная работа №2** 

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.001.png)

# **1. Цель работы:**

Разработать и реализовать клиент-серверную информационную систему, реализующую механизм CRUD.

# **2. Основное задание:**

Спроектировать и разработать систему для анонимного общения в сети интернет. 

Интерфейс системы должен представлять собой веб-страницу с лентой заметок, отсортированных в обратном хронологическом порядке и форму добавления новой заметки. В ленте отображается последние 100 заметок. 

Возможности: 

1. Добавление текстовых заметок в общую ленту; 
1. Реагирование на чужие заметки (лайки, дизлайки); 
1. Добавление комментариев к заметкам;
1. Удаление комментариев.



















# **1. Создание пользовательского интерфейса:**



![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.002.png)




На сайте пользователю доступны следующие возможности: 

1. Добавление заметок, которые будут видны на сайте; 
1. Лайк/Дизлайк существующих заметок;
1. Добавление комментариев к каждой заметке;
1. Удаление заметок;










# **4.   Описание API сервера и хореографии:**


```Пример запроса при создании новой заметки в ленте:

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.003.jpeg)

Пример запроса при удалении заметки:

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.004.png)

```


















Пример запросов при добавлении лайка/дизлайка:

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.005.png) 

# **5. Описание структуры базы данных:**

Для хранения данных в БД используется sqlite3. Имеются 2 таблицы: в первой таблице хранятся сами заметки, а также количество лайков и дизлайков:

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.006.png)





Во второй таблице хранятся комментарии к заметкам. В каждой записи хранится содержание комментария и id поста, с которым он связан:

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.007.png)









# **6. Описание алгоритмов** 

` `Алгоритм действий пользователя:

![](im/Aspose.Words.f6850a1c-9195-497b-9ca4-cd01b1129a25.008.png)










