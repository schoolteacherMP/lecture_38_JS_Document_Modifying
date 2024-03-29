# lecture_38_JS_Document_Modifying  

#  [Задачи ](https://github.com/schoolteacherMP/lecture_38_JS_Document_-Modifying/blob/main/tasks.md)  

## Методы для создания узлов:  

**document.createElement(tag)** – создаёт элемент с заданным тегом,  
**document.createTextNode(value)** – создаёт текстовый узел (редко используется),  
**elem.cloneNode(deep)** – клонирует элемент, если deep==true, то со всеми дочерними элементами.  

## Вставка и удаление:  
node.**append**(...nodes or strings) – вставляет в node в конец,  
node.**prepend**(...nodes or strings) – вставляет в node в начало,  
node.**before**(...nodes or strings) – вставляет прямо перед node,  
node.**after**(...nodes or strings) – вставляет сразу после node,  
node.**replaceWith**(...nodes or strings) – заменяет node.  
node.**remove**() – удаляет node.  

## Устаревшие методы:  
parent.appendChild(node)  
parent.insertBefore(node, nextSibling)  
parent.removeChild(node)  
parent.replaceChild(newElem, node)  
Все эти методы возвращают node.  

## Если нужно вставить фрагмент HTML, то elem.insertAdjacentHTML(where, html) вставляет в зависимости от where:  

"**beforebegin**" – вставляет html прямо перед elem,  
"**afterbegin**" – вставляет html в elem в начало,  
"**beforeend**" – вставляет html в elem в конец,  
"**afterend**" – вставляет html сразу после elem.  
## Также существуют похожие методы elem.insertAdjacentText и elem.insertAdjacentElement, они вставляют текстовые строки и элементы, но они редко используются.  

## Чтобы добавить HTML на страницу до завершения её загрузки:  
**document.write(html)**  
После загрузки страницы такой вызов затирает документ. В основном встречается в старых скриптах.  

