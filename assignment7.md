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
