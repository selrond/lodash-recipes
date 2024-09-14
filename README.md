# lodash-recipes
A couple of handy ways to utilize lodash for common data transformations.

> [!NOTE]  
> Recipes listed here aim for clarity by utilizing various lodash functions, rather than the most optimal solution.  
Having a clear, readable code using standardized patterns is almost always more valuable than having it perfectly optimized.

> [!IMPORTANT]  
> All of the recipes assume lodash to be imported like this:
>
> ```tsx
> import _ from 'lodash'
>  ```

## Create an object from an array and customize the keys & the values

```tsx
const source = ['one', 'two', 'three']

_.mapValues(
  _.keyBy(source, (key) => key), // second argument here can be ommitted, as it’s an identity function by default
  (value) => value.toUpperCase()
) 

// { one: 'ONE', two: 'TWO', three: 'THREE' }
```
