## 3.6.1 Exercises

1.) What geom would you use to draw a line chart? A boxplot? A histogram? An area chart?
* line chart  --> `geom_line()`
* boxplot --> `geom_boxplot()`
* histogram --> `geom_histogram()`
* Area chart --> `geom_area()`

2.) Run this code in your head and predict what the output will look like. Then, run the code in R and check your predictions.
* ``` 
  ggplot(data = mpg, mapping = aes(x = displ, y = hwy, color = drv)) + 
  geom_point() + 
  geom_smooth(se = FALSE)
  ```
* Based on this code, the graph will contain both the plots of a scatter plot and a smooth line. Highway MPG will be on the Y axis and engine size will be on the X axis. Each point in the scatter plot will be colored based on the type of car it represents. 
