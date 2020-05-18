# Chapter 3: Mathematics

For almost any non-trivial graphical program, geometry will need to be moved across the screen. The simplest way to do that would be to update the geometry's vertices to the new position, but constantly sending new data to the graphics card is very slow, and not feasable for a large-scale program.

In addition, Normalized Device Coordinates are too abstract for most graphical work. For example, drawing an image at the proper size is nearly impossible when all you have are NDC. Wouldn't it be easier to use a different coordinates system?

The answer to both problems comes in the form of linear algebra. This chapter will be a **brief** introduction to the concept, and how it relates to graphics programming. If you find the topic interesting and want to know more, it is heavily recommended that you continue studying outside of this book. Several potentially-useful things (such as quaternions) are omitted here for brevity.

With that said, let's begin!

## OpenGL Mathematics Library (GLM)

This tutorial is provided in C++, a language that does not include built-in linear algebra. Instead, we will use an external library: OpenGL Mathematics Library, or GLM for short. Despite the name, it will work for Vulkan just fine, as the mathematics required are the same. Download from here:

https://glm.g-truc.net/0.9.8/index.html

At the time of writing, version 0.9.9.8 is the current stable release. If you encounter problems, be certain that you use the same version as we do.

GLM is a header-only library, so no compiling or linking are necessary. Just download and copy the header folder into your includes folder.

To ensure that it works, try running the following code:

```c++
#include <cstdio>
#include "glm/glm.hpp"

int main() {
	glm::vec4 vec(1.0f, 0.0f, 0.0f, 1.0f);
	glm::vec4 vec2(0.0f, 1.0f, 0.0f, 1.0f);

	vec += vec2;

	std::printf("{%f, %f, %f, %f}", vec.x, vec.y, vec.z, vec.w);
}
```

If no errors have occurred, the program should output vector {1.0, 1.0, 0.0, 2.0}.
