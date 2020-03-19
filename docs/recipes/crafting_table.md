# Crafting Table

### Addition:
Note: All crafting table or crafting grid recipe additions must start with `craftingTable`. In order to make a recipe for the 2x2 grid, only add a 2x2 array. Example:
```zenscript
craftingTable.addShaped("grid_recipe_test", <item:minecraft:chest>,
[[<item:minecraft:stick>, <item:minecraft:oak_planks>]
[<item:minecraft:oak_planks>, <item:minecraft:stick>]]);
```

# Shaped
Shaped recipes mean that the recipe has to be put in an exact way to get the output, like when you craft a pickaxe.

Syntax:
```zenscript
craftingTable.addShaped(String recipeName, IItemStack output, IIngredient[][] ingredients, @ZenCodeType.Optional RecipeFunctionMatrix recipeFunction);
```

Example:
```
craftingTable.addShaped("shaped_mirror_test", <item:minecraft:arrow>,
[[<item:minecraft:diamond>, <item:minecraft:diamond>, <item:minecraft:air>],
[<item:minecraft:air>, <item:minecraft:flint>, <item:minecraft:air>],
[<item:minecraft:air>, <item:minecraft:flint>, <item:minecraft:air>]]);
```

# Shaped (Mirrored)
Mirrored recipes are recipes that give the same output even if it's flipped around, like how you can craft an axe by putting the planks on either side of the sticks.

Syntax:
```zenscript
craftingTable.addShapedMirrored(String recipeName, IItemStack output, IIngredient[][] ingredients, @ZenCodeType.Optional RecipeFunctionMatrix recipeFunction);
```

Example:
```zenscript
craftingTable.addShapedMirrored("shapeless_test", <item:minecraft:diamond>,
[[<item:minecraft:cobblestone>, <item:minecraft:air>, <item:minecraft:air>],
[<item:minecraft:air>, <item:minecraft:stick>, <item:minecraft:air>],
[<item:minecraft:air>, <item:minecraft:air>, <item:minecraft:stick>]]);
```

# Shapeless
Shapeless recipes are recipes that can be input any way in the crafting table and they will return the ouput.

Syntax:
```zenscript
addShapeless(String recipeName, IItemStack output, IIngredient[] ingredients, @ZenCodeType.Optional RecipeFunctionArray recipeFunction);
```

Example:
```zenscript
addShapeless("shapeless_test", <item:minecraft:wool>,
[[<item:minecraft:string>, <item:minecraft:string>, <item:minecraft:string>]]);
```
