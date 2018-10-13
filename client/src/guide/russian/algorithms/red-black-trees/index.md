---
title: Red Black Trees
localeTitle: Красные Черные Деревья
---
## Красные Черные Деревья

Red-Black Tree - это самобалансирующееся двоичное дерево поиска (BST), где каждый узел следует следующим правилам.

1.  У каждого узла есть двое детей, окрашенных либо красным, либо черным.
2.  Каждый узел дерева листьев всегда черный.
3.  Каждый красный узел имеет обоих своих детей, окрашенных в черный цвет.
4.  Нет двух соседних красных узлов (красный узел не может иметь красный родительский или красный ребенок).
5.  Каждый путь от корня до узла дерева имеет одинаковое количество черных узлов (называемое «черной высотой»).

Референс-стиль: ![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/a/ab/Fibonacci_Tree_as_Red-Black_Tree.svg/2000px-Fibonacci_Tree_as_Red-Black_Tree.svg.png "Пример фибоначчи из красных черных деревьев")

### Почему красно-черные деревья?

Большинство операций BST (например, поиск, макс, мин, вставка, удаление и т. Д.) Принимают O (h) время, где h - высота BST. Стоимость этих операций может стать O (n) для искаженного двоичного дерева. Если мы уверены, что высота дерева остается O (Logn) после каждой вставки и удаления, мы можем гарантировать верхнюю границу O (Logn) для всех этих операций. Высота красно-черного дерева всегда равна O (Logn), где n - количество узлов в дереве.

### Сравнение с AVL Tree

Деревья AVL более сбалансированы по сравнению с красными черными деревьями, но при вставке и удалении они могут вызывать больше поворотов. Поэтому, если ваше приложение связано с многочисленными частыми вставками и удалениями, то предпочтение следует отдавать от деревьев красного цвета. И если вставки и удаления менее часты, а поиск - более частая операция, тогда дерево AVL должно быть предпочтительнее Red Black Tree.

### Левонападение красно-черного дерева

Дерево с красным-черным деревом (LLRB) с левой стороны является типом самобалансирующегося двоичного дерева поиска. Это вариант красно-черного дерева и гарантирует такую ​​же асимптотическую сложность операций, но его проще реализовать.

### Свойства левых одетых красно-черных деревьев

Все предложенные алгоритмы красно-черного дерева характеризуются наихудшим временем поиска, ограниченным малой константой, кратной log N в дереве из N ключей, а поведение, наблюдаемое на практике, обычно такое же, что и несколько быстрее, чем наихудшая оценка, близкая к рассмотренным оптимальным логарифмическим узлам N, которые наблюдались бы в идеально сбалансированном дереве.

В частности, в левом наклоне красно-черного 2-3 дерева, построенного из N случайных клавиш: -> Случайный успешный поиск исследует log2 N - 0.5 узлов. -> Средняя высота дерева составляет около 2 log2 N

#### Дополнительная информация:

*   [Видео из алгоритмов и структур данных](https://www.youtube.com/watch?v=2Ae0D6EXBV4)