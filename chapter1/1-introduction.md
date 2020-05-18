# Introduction

Over the past few decades, the computing industry has seen lots of graphics technology rise, thrive, and decline to make
way for better graphics technology. Needless to say, the weird & wonderful world of graphics development is always
changing, and at times it's hard to keep up. The best example of this has been the recent debut of Vulkan.

OpenGL has been the leading graphics API for nearly 30 years now, however along the way there seems to be
a common consensus among developers: OpenGL doesn't give them enough control. Now, that's not to say that OpenGL hasn't
seen its fair share of changes to accomodate developers, because it certainly has changed since its original inception in
'92. In 2008, OpenGL 3 released, bringing with it a whole new API for making performant and effective applications using
hardware graphics and for a while this was enough.

Then in 2013, everything changed when AMD released their Mantle API to the world, popularizing a whole other level of control. Mantle popularised the verbose style of APIs we're used to see pop up thes days, such as Microsoft's Direct3D 12, Sony's GNM, Nintendo/NVIDIA's NVN, Apple's Metal, and Khronos' Vulkan, to name a few.

Vulkan is the spiritual successor to Mantle, which struggled to gain traction, being primarily only available on AMD hardware. Vulkan is an open standard and is open for implementation on any platform by any hardware manufacturer and, while some companies prefer to stick to their own exclusive APIs, Vulkan is pretty universally supported.

This book aims to teach you about Vulkan and the fundamental concepts behind it. We decided to write this book because there
wasn't a good way to grasp Vulkan without being well-versed in one of the higher-level APIs such as OpenGL, which isn't very productive if you have to learn another API just to learn Vulkan, and the only other alternative was paying a hefty premium
for the few books out there that are geared towards beginners.

Our hope is that anyone can pick up this book and delve into the world of Vulkan graphics development from little prior knowledge of graphics. Having personally struggled with grasping Vulkan (even with a fair amount of prior experience with OpenGL between us), we hope that we can save other aspiring Vulkan developers from going down the rocky path we went down in learning Vulkan with only a few good learning resources.
