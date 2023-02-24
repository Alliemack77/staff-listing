# Staff Listing 

## Some Notes to Consider:

- the listing is using [container queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Container_Queries)
    - layout is based on the width of the container (.listing-container)
    - single col at width < 600px
    - two col at widths > 600px

- the listing is using [Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) 
    - first column is using 1/4 available space
    - second column is using 3/4 available space

- you can use "grid-template-columns: auto 3fr;" to set up columns, however:
    - auto means the column will only be as wide as its contents
    - that may not be a huge deal, especailly since we should be making sure images sizes are consisitent through out the page
    - column collapses for cells without images
    - cols with smaller images will mis-align the text
    - instead I am using "minmax(200px, 1fr)" - this ensures the first col will always be a min of 200px, which is handy on pages that have different size images as using just "1fr 3fr" gives different col sizes 

- toggle the "justify-content" property to center images horizontally in their grid cell
    - this will give extra space to the left - this was something we wanted to avoid
    - we can always center the smaller images only on the pages that need it 

- to avoid column collapse I used :after psudo-element and Generated Content 
    - checkout [Rachel Andrews article *Styling Empty Cells With Generated Content And CSS Grid Layout*](https://www.smashingmagazine.com/2018/02/generated-content-grid-layout/) on Smashing Magazine