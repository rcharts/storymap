## StoryMap

This is an [rCharts](http://rcharts.io) wrapper for [StoryMapJS](http://storymap.knightlab.com/)

### Example

Make sure that you have the `dev` branch of `rCharts` installed before trying this out. Download or Clone this repo from github and run the code below from the root directory of your download.


```S
require(rCharts)
r1 <- rCharts$new()
r1$setLib('storymap')
r1$set(
  data = 'demo.json', 
  width = 1200, 
  height = 700
)
r1$save('mystorymap.html', cdn = T)
```

To view the chart you will need to open a server. You can do this from R using the `servr` package.


```S
servr::httd()
```

You can view the storymap by navigating to 'http://localhost:4321/mystorymap.html'

### To Do

While JSON is a great format for data-interchange, it is not-so-great for authoring. On my agenda is writing a simple function that will take a slidify formatted markdown file as an input, and convert it into a storymap on the fly. Watch this space for further updates!



