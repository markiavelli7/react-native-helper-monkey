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