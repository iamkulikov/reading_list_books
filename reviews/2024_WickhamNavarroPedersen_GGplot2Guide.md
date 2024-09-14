# "ggplot2: Elegant Graphics for Data Analysis (3e)", H. Wickham, D. Navarro, T. Pedersen

[<< Все книги](../README.md)

[Ссылка на книгу](https://ggplot2-book.org/)

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

4. Обрезание границ графика с помощью xlim и ylim меняет все точки за пределами на NA, причем это происходит до вычисления summary statistics, что повлияет на сглаженные линии, средние и т.д. Обрезать без потери информации о них надо с помощью coord_cartesian(ylim = c(10, 35))

5. Можно группировать по нескольки переменным aes(group = interaction(school_id, student_id)). Если мы хотим саммари по несгруппированным данным, то группировку нпдо прописывать внутри конкретного слоя, а не внутри aes верхнего уровня.

6. Взвешивание точек облака рассеяния для усреднения: 
ggplot(midwest, aes(percwhite, percbelowpoverty)) + geom_point(aes(size = poptotal / 1e6)) + geom_smooth(aes(weight = poptotal), method = lm, linewidth = 1)

7. Можно во всех аннотациях писать формулы, оборачивая их в quote: ... + labs(y = quote(f(x) == x^3))

8. С помощью ggtext можно использовать оформление в текстах лейблов но нужно тогда добавить к нужному элементу 
+ theme(axis.title.x = ggtext::element_markdown())

9. Если нужно, чтобы пустой лейбл не занимал место, делаем его NULL, а не ""

10. Пакеты, чтобы сделать независимые от устройства надписи на графиках:  https://github.com/yixuan/showtext и https://github.com/wch/extrafont

11. Оси немного торчат за пределы, определенные xlim - нужно, чтобы точки данных не ложились прямо на оси. Чтобы этого избежать, можно scale_y_continuous(expand = expansion(0)). Их конечно 

12. Хороший способ залейбелить месячные или девные данные: scale_x_date(limits = lim, labels = scales::label_date_short()) - число года будет отмечены только на первой отсечке года, а обозначение месяца будет трехбуквенное.

13. Ручной поворот надписей на оси, если они перекрываются: guides(x = guide_axis(angle = 90)). Или их расположение на нескольких строчках: guides(x = guide_axis(n.dodge = 3))

14.



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
