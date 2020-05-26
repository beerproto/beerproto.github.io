# Inferred Values
 
You can use the the following pseudocode (JSONPath) methods to calculate the inferred values.

### Pre-Boil Volume

```javascript
kettle = $.Recipe.equipments.equipment_items[?(@.form == 'BREW_KETTLE')]
```

```javascript
Pre-Boil Volume = $.RecipeType.batch_size.value + kettle.boil_rate_per_hour.value
```

