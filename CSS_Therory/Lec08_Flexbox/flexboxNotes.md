# flex - box properties
display:flex
makes the element flexible-box and its immediate children flex-items

flex-direction 
used to decide the direction in which the new content will be added
    values :
        1. row (default) -> content flows left to right and main-axis is vertical
        2. row-reverse -> content flow right to left and main-axis is vertical
        3. column -> content flow top to bottom and main-axis is horizontal
        4. column-reverse -> content flow bottom to top and main-axis is horizontal

flex-wrap
used to define the behavior when there is no space available, and it shirking 
        1. no-wrap (default)
        2. wrap


flex-flow 
is a shorthand property that combines the functionalities of flex-direction and flex-wrap.

justify-content: 
used to align content on main axis
    values : 
        1. start (default)
        2. end
        3. center
        4. space-between
        5. space-around
        6. space-evenly

align-items : 
in flex-box, controls the alignment of items on the cross axis.
    values : 
        1. stretch : takes full height
        2. center 
        3. start
        4. end
align-content
controls the spacing between 2 rows
    values
        1. start
        2. center
        3. space-between
        4. space-around

# flex - items properties

order
decides sequence based on index given of element using order property element are sequenced from 0 to infinity and its value is in int

flex-shrink and flex-grow
when the elements are shrink or grow with increasing and decreasing window size, the property decide its speed  to shoring and grow and its value is in int


flex-basis
controls the initial size of element and its value is in px

flex: {flex-grow} {flex-shrink} {flex-basis}

align-self
overrides the grid or flex item's  align-item property values with alignment the cross axis
    values 
        1. stretch
        2. center
        3. start
        4. end
