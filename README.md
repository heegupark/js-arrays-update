# js-arrays-update
> - Maintained by: `Heegu Park`

## Adding
- const array = [1, 2, 3, 4, 5];
- const index = array.indexOf(3);
- const addedArray = [...array.slice(0, index), 30, ...array.slice(index)];
- result: [1, 2, 30, 3, 4, 5]

## Removing
- const array = [1, 2, 3, 4, 5];
- const index = array.filter(n => n !== 3);
- result: [1, 2, 4, 5]

## Updating
- const array = [1, 2, 3, 4, 5];
- const index = array.map(n => n === 3 ? 30 : n );
- result: [1, 2, 30, 4, 5]

## Flattening
```
const biDimensionalArr = [11, [22, 33], [44, 55], [66, 77], 88, 99];
const flattenArr = [].concat(...biDimensionalArr); // [11, 22, 33, 44, 55, 66, 77, 88, 99]
```

```
function flattenMultiArray(arr) {
    const flattened = [].concat(...arr);
    return flattened.some(item => Array.isArray(item)) ? flattenMultiArray(flattened) : flattened;
 }
const multiDimensionalArr = [11, [22, 33], [44, [55, 66, [77, [88]], 99]]];
const flatArr = flattenMultiArray(multiDimensionalArr); // [11, 22, 33, 44, 55, 66, 77, 88, 99]
```
