# Staff Listing 

## Some Notes to Consider:

- the listing is using container queries
    - layout is based on the width of the container (.listing-container)
    - single col at width < 600px
    - two col at widths > 600px

- the listing is using Grid 
    - first column is using 1/4 available space
    - second column is using 3/4 available space

- you can use "grid-template-columns: auto 3fr;" to set up columns, however:
    - auto means the column will only be as wide as its contents
    - column collapses for cells without images
    - cols with smaller images will mis-align the text

- toggle the "justify-content" property to center images horizontally in their grid cell
    - this will give extra space to the left - this was something we wanted to avoid
    - we can always center the smaller images only on the pages that need it 