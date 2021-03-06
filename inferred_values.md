# Values
 
You can use the the following pseudocode methods to calculate the inferred values.

## Reference

`$` a JSONPath in beerProto (the values within given structs are ignored for readability e.g. $.RecipeType.batch_size instead of $.RecipeType.batch_size.value)

`hours()` function to return the number of hours.

`points()` function to return the digits to the right of the decimal point multiplied by 1000; for example, a specific gravity of 1.048 is 48 points.

### Pre-Boil Volume

```javascript
kettle = $.Recipe.equipments.equipment_items[?(@.form == 'BREW_KETTLE')]
```


```javascript
pre-boil_volume = (($.RecipeType.batch_size / 100) * expansion) + $.RecipeType.batch_size + (hours($.RecipeType.boil.boil_time) * kettle.boil_rate_per_hour)
```

### Pre-Boil Gravity
```javascript
pre-boil_gravity = ($.RecipeType.batch_size * points($.RecipeType.original_gravity)) / pre-boil_volume
```

# Constants

### Sucrose (SG)
```javascript
sucrose = 1.04621
```
### Water expansion (%)
```javascript
expansion = 4.16
```
