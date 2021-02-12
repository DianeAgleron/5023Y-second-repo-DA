# 5023Y-second-repo-DA
## Introduction
In this exercise, our skills of Rmarkdown will be revised and combined with new found knowledge of GitHub . 

```{r setup, include=FALSE}
library(tidyverse)
library(palmerpenguins)
library(plotly)
```

## Palmer Penguins
```{r, echo=FALSE}
penguin_graph <- ggplot(data = penguins, aes(x = bill_length_mm, y = bill_depth_mm)) +
  geom_point(aes(size = body_mass_g, 
                 color = species),
             alpha = 0.4) +
  scale_color_manual(values = c("purple","orange","black")) +
  theme_minimal() +
  labs(x = "bill length (mm)",
       y = "bill depth mm",
       title = "Penguin measurements")
penguin_graph
ggplotly(penguin_graph, tooltip = c("species"))
```
