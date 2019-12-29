# Flexbox

## flex property

The flex property is applied to child elements that are inside of a parent flex container:

```javascript
flex: 1;
```

By setting the flex property, the child components no longer shrink to take the minimum amount of space that they need to display their child components. They grow to take up as much space as they can get along the main axis.

**For setting the space on the cross axis, if we want the child components to take all of the available space, we have to set alignItems to 'stretch' on the PARENT component.**

## justify-content

Sets the spacing/alignment along the main axis (vertical in column and horizontal if flex-direction is set to row).

## align-items

Sets the spacing/alignment of the children along the cross axis.

## flex-direction

### Available Settings:
- **column**: This is the default setting
- **row**
- **row-reverse**
- **column-reverse**

## Sizing Child Elements

If we leave off height and width properties, each box will shrink to be as small as it can be while displaying the child elements.

## Default Child Alignment

By default child elements align themselves along the parents cross-axis

## flex-grow

Just like *flex*, **flex-grow** also makes sure that the item to which we add the property to will grow to take up as much space as it can. The difference is that **flex-grow** works a little bit differently internally, it is more flexible.

**flex** takes all of the available space in all of the directions that it can.

**flex-grow** gives the container the ability to grow to take as much space as it can get, but it will keep the other behavior of its container. For example if **flex-grow:1** is applied to a **ScrollView**, it will keep the content scrollable and will not exceed the boundaries of the screen.