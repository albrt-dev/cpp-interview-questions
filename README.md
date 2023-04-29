# Вопросы к собеседованию C++

## Вопросы

| № | ВОПРОС |
| - | -------- |
| 1 | [С vs С++](https://github.com/albrt-dev/cpp-interview-questions#c-vs-c) |
| 2 | [В чем разница между структурой [struct] и классом [class]](https://github.com/albrt-dev/cpp-interview-questions#в-чем-разница-между-структурой-struct-и-классом-class) |
| 3 | [Отличие static_cast от приведения типов в стиле языка C](https://github.com/albrt-dev/cpp-interview-questions#отличие-static_cast-от-приведения-типов-в-стиле-языка-c) |

## Ответы
1. ### C vs C++
   https://www.geeksforgeeks.org/difference-between-c-and-c
2. ### В чем разница между структурой [struct] и классом [class]
   В C++ структуры формально отличаются от классов лишь тем, что по умолчанию уровень доступа к членам класса и тип наследования у структуры публичные, а у класса — приватные.
   Источник: [Википедия](https://ru.wikipedia.org/wiki/C%2B%2B#%D0%98%D0%BD%D0%BA%D0%B0%D0%BF%D1%81%D1%83%D0%BB%D1%8F%D1%86%D0%B8%D1%8F).
3. ### Отличие static_cast от приведения типов в стиле языка C
   Оператор приведения static_cast применяется для неполиморфного приведения типов на этапе компиляции программы. Отличие static_cast от приведения типов в стиле языка C состоит в том, что данный оператор приведения может отслеживать недопустимые преобразования, такие как приведение указателя к значению или наоборот (unsigned int к указателю на double не приведет), а также приведение указателей и ссылок разных типов считается корректным только, если это приведение вверх или вниз по одной иерархии наследования классов, либо это указатель на void. В случае фиксации отклонения от данных ограничений будет выдана ошибка при компиляции программы. При множественном наследовании static_cast может вернуть указатель не на исходный объект, а на его подобъект.
   Источник: [Хабр](https://habr.com/ru/articles/266747/).
   
