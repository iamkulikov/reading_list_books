# Трилогия «Квантовый вор», Ханну Райаниеми

[<< Все книги](../README.md)

## Рецензия

Пр

## Находки

1. Plot = data + mapping (from data to aesthetic components)

Mapping: a. Layers - what you actually see in the plot: points, lines, polygons, etc. Statistical transformations, summarise the data: for example, binning and counting observations to create a histogram, or fitting a linear model.
b.  Scales - map values in the data space to values in the aesthetic space. This includes the use of colour, shape or size. Scales also draw the legend and axes, which make it possible to read the original data values from the plot (an inverse mapping).
c. Coordinate system, describes how data coordinates are mapped to the plane of the graphic. It also provides axes and gridlines to help read the graph.
d. Facet specifies how to break up and display subsets of data as small multiples
e. Theme controls the finer points of display, like the font size and background colour.

2. geom_smooth(method = "rlm") из пакета MASS - это robust linear squares, можно заменить на него
   geom_smooth(method = "rlm", formula = y ~ s(x)) из пакета mgcv - это generalized linear model

3. geom_jitter(), чтобы немного размотать точки, которые строятся одна поверх другой

4. Обрезание границ графика с помощью xlim и ylim меняет все точки за пределами на NA, причем это происходит до вычисления summary statistics, что повлияет на сглаженные линии, средние и т.д. Обрезать без потери информации о них надо с помощью

5. Можно группировать по нескольки переменным aes(group = interaction(school_id, student_id)). Если мы хотим саммари по несгруппированным данным, то группировку нпдо прописывать внутри конкретного слоя, а не внутри aes верхнего уровня.

6. 

7.

8.


## Мои идеи

1. 

2. 


## Теги



## Жанр/тема

Руководство

## Оценка внутри жанра

10

## Когда прочел

2024
