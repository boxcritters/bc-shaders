# Hello World

*Based off: [https://github.com/baseten/easelbender]*

# Steps for now
Copy https://github.com/boxcritters/bc-shaders/blob/master/bc-shaders.js in to console
# Sample Usage
```js
var fs = `#version 300 es
precision mediump float;

in vec2 vPixelCoord;
out vec4 fColor;

uniform sampler2D uStageTex;
uniform float uTime;
uniform vec2 uViewportSize;
uniform vec2 vMousePos;

void main() {
	fColor = texture(uStageTex,vPixelCoord);
}`
loadShader({fs:fs})
```

# params
{
* fs:FragmentShader
* vs:VertexShader
* data:custom uniforms
* container:
}

# Built in uniforms
sampler2D uStageTex
float uTime
vec2 uViewportSize
vec2 vMousePos