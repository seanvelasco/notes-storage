
In Godot, everything is a scene or a node.


1. Create a scene, Node2D. This is the root node. You can rename it to level. I renamed it to World.




### Creating a character
1. Create another separate scene CharacterBody2D. You can rename this to Player.
2. Under CharacterBody2D, create a Sprite2D as a child node.
3. Navigate to Sprite2D > Texture on the right-side panel. Drag the character sprites to the picker.
4. Go to the right-side panel > Navigation and adjust the Hframes and Vframes
5. Add CollisionShape2D, change Shape to RectangleShape2D 
6. Click the Shape > Rectangle and adjust the pixels accordingly
7. Drag Player or CharacterBody2D to the root node World




### Game is blurry, how to fix
1. Navigate to Project > Project Settings > Rendering > Textures
2. Set Default Texture Filter to Nearest
