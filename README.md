# mandela
drawing mandela shapes based on voronoi diagrams :art: :snowflake:

To create a simple shape:
```{r}
mandela(iter=4, points=6, radius=1.6, palette=topo.colors(5))
```
The palette can be applied by polygon area or distance from the center using the palette as supplied or as a gradient from those values.
```{r}
mandela(iter=4, points=6, radius=1.6, palette=viridis(5), distance_colouring = TRUE, gradient_colouring = TRUE)
```

To create an animation of shapes:
```{r}
mandela_save(4,c(3,6,9,12),seq(from=1.8,to=4.2,by=0.1),border_poly = TRUE, path = "images/",cm=10,res=100,palette = viridis::viridis_pal()(20))
im43<-magick::image_read(paste0("images/",dir("images/")))
ani43<-magick::image_animate(im43)
magick::image_write(ani43,"ani43.gif")
```

![mandala3-10-3](https://github.com/jrwalker-projects/mandala/blob/master/man3-10-3vir15.png)
