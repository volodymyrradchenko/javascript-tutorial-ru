Основная причина -- шаблон может быть любым, даже некорректным HTML. В `DIV` доставить незакрытым тег -- и могут быть проблемы. А в скрипте может быть почти что угодно, его содержимое полностью игнорируется.

Кроме того, содержимое `DIV` браузер обрабатывает, создаёт DOM-узлы, добавляет их в документ, но там они совсем не нужны, это же шаблон.

Альтернативный вариант -- поместить шаблон в комментарий `<!-- ... -->`, его содержимое можно получить при помощи `node.data`. Но у узла-комментария не может быть `id`, так что это менее удобно.
