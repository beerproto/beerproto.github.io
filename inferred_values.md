# Values
 
You can use the the following pseudocode methods to calculate the inferred values.

## Reference

`$` a JSONPath in beerProto

`??` a null-coalescing operator, returns the value of its left-hand operand if it isn't null; otherwise, it evaluates the right-hand operand and returns its result.

`??=` null-coalescing assignment operator, assigns the value of its right-hand operand to its left-hand operand only if the left-hand operand evaluates to null.

### Pre-Boil Volume
A default boil time of 60 minutes when no boil_time is provided.

```javascript
kettle = $.Recipe.equipments.equipment_items[?(@.form == 'BREW_KETTLE')]
```

```javascript
pre-boil_volume = $.RecipeType.batch_size.value + (kettle.boil_rate_per_hour.value * $.RecipeType.boil.boil_time ?? 60)
```

### Pre-Boil Gravity
```javascript
pre-boil_gravity = ($.RecipeType.batch_size.value * $.RecipeType.original_gravity.value) / pre-boil_volume
```


### Density
```javascript
density =  pre-boil_volume / 
```

### Specific volume 
```javascript
specific_volum = density /
```

# Constants

### Sucrose (SG)
```javascript
sucrose = 1.04621
```
### Volumetric expansion coefficient (1/k)
```javascript
expansion = 0.0004
```
