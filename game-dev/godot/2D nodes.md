

**Node2D**
keeps track of position, rotation, and scale
all other nodes may inherit from this node

**Camera2D**
specifies the point from which the scene is viewed
contains params for rotation and position
takes care of camera drag and smoothing

AnimatedSprite2D and Sprite2D
used to render 2D textures

CollisionShape2D
cannot be used as a standalone
serves as base class for all 2D objects that has collisions

PhysicsBody2D
cannot be used as a standalone
serves as a base class for all 2D objects affected by physics

RigidBody2Dqwe\
- physics body that is affected by other physics bodies and gravity
- used for all physics items than can be moved and are not directly controlled by the player

CharacterBody2D
- specialized physics body that is meant to be controlled by the body
- it contains built-in functionality for precise movement controlling with code with physics simulation

Area2D
- detection field that checks whether collision objects leave or enter it
- an area of space with its own physics and audio settings
- you can change wind, gravity, audio channels


CanvasModulate

