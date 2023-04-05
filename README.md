# Angular + WebGL template 
This is a quick start WebGL project template for Angular.

## Workflow

### WebGL
Rendering is done in the fragment shader located at [/src/shaders/fragment.glsl](/src/shaders/fragment.glsl), this is where the code must be changed to control rendering.

Here is a recap of the different variables:

| Variable  | Description |
| ------------- | ------------- |
| u_Width  | width of the canvas |
| u_Height  | height of the canvas |
| o_FragColor | color that will be rendered to the canvas |

By default this shader draws random colored pixels.

### Angular

Rendering is called from **scene-canvas** component located at [/src/app/scene-canvas/scene-canvas.component.ts](src/app/scene-canvas/scene-canvas.component.ts).<br>
The ``main()`` function is responsible for initializing **WebGL context**, **buffers**, **program**, **program info**, handling **window resize** and **animation loop**.<br>
The ``drawScene(gl: WebGL2RenderingContext, programInfo: any)`` function is called each animation loop. It passes info and buffers to WebGL shaders and renders to the canvas.


## How to use

*The website is an [Angular](https://angular.io/docs) application.*<br>
Install [Angular CLI](https://angular.io/cli)<br>
Clone this repository<br>
Run ``npm install`` command in the project root to install all packages<br>
Run ``ng serve`` command to start a local server

## Examples


[wavesimulator.starfree.app](https://wavesimulator.starfree.app)

https://user-images.githubusercontent.com/98308569/230017409-2630d962-d2b9-41ae-9502-a5e3ac029765.mov

<br><br>
[newtonfractal.starfree.app](https://newtonfractal.starfree.app)

<img width="1118" alt="Capture d’écran 2023-04-05 à 09 56 06" src="https://user-images.githubusercontent.com/98308569/230017614-6dcf0dd7-06cd-46d5-afc5-7edc7d6cae26.png">

<br><br>
[chargesimulation.starfree.app](https://chargesimulation.starfree.app)

https://user-images.githubusercontent.com/98308569/230018003-396b7752-fa1f-4036-80c9-3428de694549.mp4

