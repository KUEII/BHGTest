# BHGTest

## Feature Testing

### Basic Control

- Move - WASD
- Look around - Mouse

### Pick Up Item

- Interact(pick up) - E

### Inventory

- Open inventory UI - B
- Drag and drop - LMB
- Close - Esc/Close Button
- Inspect 3D mesh control - LMB drag

Inspection viewport is on the right side in the inventory, it is empty initially. Drop items on top of it to inspect the items.

### Dialogue Trigger

- Interact(talk) - E
- Continue dialogue - Next Button

There is a NPC on the right side that is talkable.


## Design Decision

### Interactive Module

Interaction is very common and resuble, should be better modularized.
The custom interactive module

### Item

A very bare bone Item structure with item table, only ID and appearance are included.
With the limit of time, I was focusing on functionaility and I think this should be enough for testing.

### Inventory

I also used a very bare bone inventory component, with only an array of structure and limited functionaility to finish the test. It could also be implemented in other way, for example, a global inventory system.
I instantiated an individual mesh inspector somewhere in the level, and a scene capture component to render the mesh onto a texture. The control of the mesh inspection is actually transforming the scene capture component.

### Drag and Drop

The built-in Drag and Drop functionality is used, with a custom InventoryDDO extended from the built-in DragDropOperation.

### Dialogue

Some simple dialogue data stored directly inside the NPC. could be better integrated into a dialogue component or a global dialogue system, with a dedicated data asset or formats from external plugins.
