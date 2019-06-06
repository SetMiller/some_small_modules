# Proxy

Цели и задачи:
-
* Практика применения

Интересные моменты:
-  
* В данном примере рассматривается работа с функцией, которая принимает функцию обратного вызова и возвращает Proxy
* При обращении к элементу добавляем проверку передаваемых запросов
  - В случае, если это объект, то обрабатывает запрос рекурсивно:
    ```javascript
      return watchObj(target[name], callback)
    ```
  - В случае, если это функция, обрабатывает запрос, в контексте выбранного элемента:
    ```javascript
      return target[name].bind(target)
    ```
