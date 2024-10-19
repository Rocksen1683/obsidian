
## Windowing System 
Operating system layer to share screen space and user input among applications

### Canvas Abstraction 
Windowing system uses a *drawing canvas abstraction*
- local drawing area within window 
- co-ordinate system starts from $[0, 0]$ from top-left 
- drawing area implemented as a graphics buffer 

Windowing system renders the buffer at window position 
- using fast method called **bitblt** (*bit bl*ock *t*ransfer)

### Window Manager 
Windowing system also has a **window manager** to render the window and provide a Window UI 
- buttons for closing, maximizing 
- draggable areas for resizing 
### UI Toolkit 
Provides a level of abstraction to programmers and translates a programmers concepts of UI Elements into a rendering of them 
![[Pasted image 20240228122306.png]]

### Three Conceptual Models of Drawing Primitives 
1. **Pixel**: changing pixel color, pixel images
2. **Stroke**: lines, shape outlines 
3. **Region**: filled shapes, text 

## Graphics Context 
Graphics Context acts as a way to manage the state of drawing style options. Allows you to set the stroke color, fill color, width etc and allows you to keep changing it as it manages state.

### CanvasRenderingContext2D 
Getting the context for HTML Canvas 
`const gc = canvas.getContext("2d");`
#### Drawing Commands 
- rectangles 
- paths 
- text 
- images 
#### Drawing styles 
- fill and stroke color
- line thickness 
- font, text alignment 

## SimpleKit 
### Rectangle Demo 
```TypeScript 
gc.fillStyle = "red";
gc.fillRect(70, 10, 50, 50); 
gc.strokeStyle = "blue"; 
gc.strokeRect(80, 20, 50, 50); 

// stacking to make more complex shapes 
gc.lineWidth = 3; 
gc.fillRect(150, 20, 50, 50); 
gc.strokeRect(150, 20, 50, 50); 
// has no effect 
gc.strokeStyle = "green";
```

![[Pasted image 20240228123248.png]]

### Text Demo 
```TypeScript 
const x = 150; const y = 75; 
gc.font = "32pt sans-serif"; 

// standard alignment 
gc.fillStyle = "blue"; 
gc.fillText("Hello", x, y); 

// fully centred alignment 
gc.textAlign = "center"; 
gc.textBaseline = "middle"; 
gc.fillStyle = "green"; 
gc.fillText("Hello", x, y); 

// dot to show x,y location 
gc.fillStyle = "red"; 
gc.fillRect(x - 2, y - 2, 4, 4);
```

![[Pasted image 20240228123711.png]]

## Painter's Algorithm 
To draw complex shapes: 
- Combine drawing primitives 
- Draw *back-to-front* 
- Layer the image 
![[Pasted image 20240228125012.png]]

## Display List 
Keep an ordered *display list* of `Drawable` objects 
- Add all objects to array from back to front 
- Iterate through list and draw each object 

