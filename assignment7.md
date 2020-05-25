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
* After running the code I realize that it was actually creating three (3) smooth lines, not just one. Everything else was correct!

3.) What does show.legend = FALSE do? What happens if you remove it? Why do you think I used it earlier in the chapter?
* Show legend removes the legend on the side of the chart. If you don't include the `show.legend = FALSE` bit of code a key describing what each color appears alongside the graph. The legend was removed earlier in the chapter to save space in side-by-side comparisons. Additionally, the graphs were not complicated enough to warrent a key. 

4.) What does the se argument to geom_smooth() do?
* The `se` argument in `geom_smooth` visualizes the margin of error associated with the line being graphed. 

5.) Will these two graphs look different? Why/why not?
```
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_point() + 
  geom_smooth()
  
ggplot() + 
  geom_point(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_smooth(data = mpg, mapping = aes(x = displ, y = hwy))
```
* These graphs will look the same. The `+ geom_point() + geom_smooth()` code in the first graph simply adopts the already established parameters. Whereas in the second graph we define them twice. You'll get the same result, the second graph is simply more work.

6.) Recreate the R code necessary to generate the following graphs. (From left to right, top to bottom)
* Graph 1: 
```
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + 
  geom_smooth(se = FALSE) +
  geom_point()
```
