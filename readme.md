# Css flexbox

## Display
**flex**: aligning elements as bock elements
**inline-flex**: aligning elements as inline-bock elements

## Direction
**row** (default): from left to right

**column**: from to to bottom

## Order
Order in which element inside the flex container appear.
By default, all elements have an order of 0.
That can be annoying when setting the order 1 on an element, as it would appear after all others.
Negative values are allowed. This can be useful to push something on top.

## Jusitfy content
Defines how elements inside of the flex container are distributed among the available space of the container.

**flex-start** (default): Normal behavior. From start, then one after the other.

**flex-end**: The opposite. All element will be pushed to the end.

**center**: Distributes the available space equally between before and after the elements.

**space-between**: Pushes the first element at the start and the last at the end and distributes the other elements with an equal space.

**space-around**: Divides the available space equally between element and uses half of the space between element on start and end.

## Align items
Defines if items need to be all equally wide/high (depending on the direction) or independent.
**stretch** (default): stretches the smaller items to be equally big as the container.

**flex-start**: keeps items as big as their content and aligned to the start.

**flex-end**: keeps items as big as their content aligns them to the end.

**center**: keeps items as big as their content aligns them to the center.

**baseline**: keeps items as big as their content aligns them to the baseline of the first text line of each item.

## Align self
Accepts the same values as **align-items** but has to be applied to an individual item of the flex container.

---

## Flex basis
Flex basis is the optimal dimension (depending on the direct this will be the height or the width) to use if the space is available.

## Flex grow and flex shrink
**flex-grow**: defines how items in a flex container are to be expanded when there is remaining space. The value represents a proportion of the remaining space to use to expand. Example: If there are to flex items and both of their values are 1, they will share the remaining space to 50%. If the first has 2 and the second 1, the first will grow using 2/3 of the remaining space and the second 1/3.

**flex-shrink:** defines how items in a flex container are to be shrinked under their **flex-basis** when there is not enought space. The value represents a proportion of the missing space to remove form the item's size. Example: If there are to flex items and both of their values are 1, they will share the missing space to 50%. If the first has 2 and the second 1, the first will shrink using 2/3 of the remaining space and the second 1/3.

The difference with **flex-grow** here, is that the maximum that an item can shrink is determinated by its content's minimul size. In other words, it won't crop an item. It is also possible to prevent the dismention of an item to go unter the flex basis by setting the *flex-shrink* property to 0.

---

## Shorthand
The order of the properties in the shorthand differ depending on what value is assign on it and on how many values are set in the shorthand.

Example:
```
.title-1 {
  background: #dd5f40;
  flex: 1;
    /* flex-grow: 1;
       flex-shrink: 1;
       flex-basis: 0;
    */
}

.title-2 {
  background: #3d483a;
  flex: 20px;
    /* flex-grow: 1;
       flex-shrink: 1;
       flex-basis: 20px;
    */
}

.title-3 {
  background: #468e5d;
  flex: 0 80px;
    /* flex-grow: 0;
       flex-shrink: 1;
       flex-basis: 80px;
    */
}
```

## Setting the elements the same width
**flex: 1**

---






