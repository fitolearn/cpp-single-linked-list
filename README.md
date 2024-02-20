# Single linked list

# Описание программы
Аналог контейнера std::forward_list, обеспечивается строгая гарантия безопасности исключений. Элемент списка называется «узел». Элемент списка можно представить в виде структуры **Node**, которая содержит значение элемента и указатель на следующий узел. 

# Требования:
1. -std=c++17
2. g++ (MinG w64) 13.2.0

# Шаблонный класс односвязного списка SingleLinkedList<Type> обладает следующим функционалом:
 - Конструктор по умолчанию `SingleLinkedList`, который создаёт пустой список;
 - Конструктор копирования;
 - Метод `InsertAfter`. За время O(1) вставляет в список новое значение следом за элементом, на который ссылается переданный в InsertAfter итератор. Метод обеспечивает строгую гарантию безопасности исключений.
 - Метод `EraseAfter`. За время O(1) удаляет из списка элемент, следующий за элементом, на который ссылается переданный в `InsertAfter` итератор. Не выбрасывает исключений.
 - Метод `swap`. Обменивает содержимое списков за время O(1);
 - Метод `GetSize`. Возвращает количество элементов в списке за время O(1)
 - Метод `IsEmpty`. Сообщает, пустой ли список за время O(1)
 - Метод `PushFront` Вставляет элемент value в начало списка за время O(1)
 - Метод `Clear`. Очищает список за время O(N)
 - Метод `PopFront`. Удаляет первый элемента непустого списка за время O(1)
 - Методы `before_begin` и `cbefore_begin`. Возвращают итераторы, ссылающиеся на фиктивную позицию перед первым элементом списка. Такой итератор используется как параметр для методов `InsertAfter` и `EraseAfter`, когда нужно вставить или удалить элемент в начале списка.

# В классе односвязного списка представлен следующий функционал:
 - Операции сравнения ==, !=, <, >, <=, >=;
 - Обмен содержимого двух списков с использованием метода swap и шаблонной функции swap;
 - Конструирование односвязного списка на основе `initializer_list`.
 - Конструктор копирования и операция присваивания. Операция присваивания обеспечивает строгую гарантию безопасности исключений.
