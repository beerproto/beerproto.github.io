# Inferred Values
 
You can use the the following pseudocode (JSONPath) methods to calculate the inferred values.

### Pre-Boil Volume

```javascript
kettle = $.Recipe.equipments.equipment_items[?(@.form == 'BREW_KETTLE')]
```

```javascript
pre-boil_volume = $.RecipeType.batch_size.value + kettle.boil_rate_per_hour.value
```

### Pre-Boil Gravity
```javascript
pre-boil_gravity = ($.RecipeType.batch_size.value * $.RecipeType.original_gravity.value) / pre-boil_volume
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
