---
layout: post
title:  "3D Game Engine Written in C++"
author: "Steven"
img_preview_1 : "/assets/gameengine/Engine_xEhLLv1aRc.png"
img_preview_2 : "/assets/gameengine/glossy_marble.png"
img_preview_3 : "/assets/gameengine/gold_head.png"
img_preview_4 : "/assets/gameengine/Engine_Qk40NZYm1U.png"
---


[See On Github](https://github.com/tucci/game-engine/tree/imgui-editor/Engine/Engine)


# Some History

**TLDR:** I always wanted to create a game engine from scratch, but never had the time or know how. After programming for **8 years** *(at the time of writing this)* and taking numerous related game dev courses, I feel like I have built up enough knowledge and confidence to start building a game engine from the ground up.


When I started school, I told myself that I wouldn't go into game development. It seemed too far fetched and out of reach for me.
However, as I started taking more advanced classes, I found the game related courses always to be the most interesting. The first game related class I took was a computer graphics course.
We went over the graphics pipeline, modeling, animation, rendering, opengl programming, basic lighting and texturing, shader programming, ray tracing, etc.
I was very interested that I got an A+ on this course somehow. The group project was a lot of fun [*(you can see the results here)*]({% post_url 2018-05-2-Procedural-Art-Gallery %}).
I built a very basic 3d engine from scrath for my group to use. It was pretty simple, and lots of things were coded specifically for our problem. We didn't have much time, so we had to take shortcuts.


After the graphics course, I just end up taking anything related to graphics and games development.

**Related Courses:**
- Computer Graphics
- Game Development I & II (Heavy focus on Game Design and AI)
- Image Processing
- Computer Vision
- Numerical Methods
- C++
- Compilers


While C++ is not related to games specifically, it is the standard in game development. So C++ seemed like a no brainer to take. 
On the other head, both Image Processing and Computer Vision have similarities to game development.
Techniques learned in Image Processing can be used with shader programming and other graphic programming techniques.
Computer Vision has a lot of overlap with computer graphics and 3D math.
Compilers was the least related to games, but I think the class helped increase my programming proficiency.
Understanding what compilers do and don't do for you is very important for making things go fast. Knowing that the code you write has to be ran on a real machine with real constraints is important to know.
Writing a compiler from scratch makes you learn a lot about programming and performance. It was very challenging and very fun as well. 


<!--
# Why are you writing a game engine? You can just use Unity or Unreal.
Yes.
If you want to create a game, both Unity and Unreal are much better alternatives.
The time it takes to write an engine from scratch is infinite. You'll never be able to create a game in time. You'll waste a lot of time, effort, and are probably going to do everything wrong.

This is more or less the response everyone gives you when you say you are making a game engine. I agree mostly, and disagree depending on the game and context.

There are many good reasons to write your own game engine.

- Your game would be extremely difficult to implement in Unity or Unreal. *(Probably not, but try them first)*
- You have a very large team of experts and you need all the control. *(You already know all this then.)*
- You are trying to learn how game engines work *(that is my reason)*.
- For the fun of it.
- You have ambition or don't care what other people tell you to do.

I am sure there are other reasons to write your own game engine. 

My reason is that I didn't set out to make a game. I just wanted to learn how game engines work.
For me, making game engines and tools for other people to use was more interesting and fulfilling.

I always loved programming tools to support other programmers and artists to help them build cool stuff. I don't mind doing the hard work and being in the background supporting everyone else.
-->


# Philosophy for writing this engine
- No libraries such as stl and boost. (No std::vector or std::string)
- Minimize dependencies
- Try to write everything from scratch as much as possible
- Program using Data Oriented Design
- Avoid OOP 
- Program in C++, but avoid all the crazy modern C++ insanity
	- Templates are used sparingly (Only containers), also to avoid bloated compile times
	- Minimal use of operator overloading. Only used for Vectors, Matrices, and Quaternions
	- No Virtuals, Inheritance, or OOP-ness
	- No Friend declarations
	- No new/delete. Try to use custom memory allocators for everything
	- Avoid autos. Prefer fixed width int types (uint32_t/u32 over int)
	- No C++ Exceptions
	- No RTTI
	- Try to think hard about object lifetime and ownership.
- Avoid too many layers of abstraction
- Be explicit rather than implicit. Code is easier to follow in the debugger
- Think about the data and data flow
- Be wary about memory latency, memory layout, and the memory hierarchy
- Understand that you are writing code for a real machine with constraints, finite resources and not some abstract machine
	- How much memory does a system need?
	- How much time does a system need to perform its task?
	- Does this code need to be done now, or can it be done later?
- Write code that I need now and not in the future
- Write code that is easy to debug, understand, and easy to change
- Write code that can be multi-threaded easily
- Try to read the outputted assembly and try to understand what it is trying to do
- Understand what the compiler can and can't do for me

# Things I learned/Implemented
- Work Ethic, Self Discipline, and Consistency. I worked on this for at least an hour everyday.
- Physically Based Rendering with HDR [Followed the learnopengl tutorial](https://learnopengl.com/PBR/Theory)
- HDR Skybox for IBL(Image Based Lighting)
- ECS using a Data Oriented Design
- Material System (Cook Torrance) (Albedo, Normal, Metal, Roughness, AO maps)
- Software Rendering [Followed the Tiny Renderer tutorial](https://github.com/ssloy/tinyrenderer)
- Built a platform layer (win32,linux) on top of SDL2
- Implemented own math library (Vectors, Matrices, Quaternions) in SIMD
- Custom Memory Allocators
- Faster Hashmap implementation. (Linear, Open Addressed)
- Custom FBX scene importer written from scratch
- Shadowmaps using PCF
- Experimenting/Learning about Renderer Architecture.
- Experimental Multi threaded Job System
- Proper Game loop with physics untied to framerate
- Implemented an entire Asset Management system. (Asset Ids/Handles, Asset Files, Asset Loading)
- Implemented Scene Hierarchy Management
- Logging System with different levels (INFO, WARN, FATAL, VERBOSE)
- Started integrating an editor using Qt(but moved to ImGui)
- Undo/Redo system for editor
- Drag and drop support



## Some Screenshots
![]({{site.url}}/assets/gameengine/glossy_marble.png){: .col-12}
Some overly glossy marble material

![]({{site.url}}/assets/gameengine/gold_head.png){: .col-12}
Gold head, sphere, and plane to show reflections using IBL (Image Based Lighting)

![]({{site.url}}/assets/gameengine/painted_cement.png){: .col-12}
Showing a painted cemented material

![]({{site.url}}/assets/gameengine/rusted_iron.png){: .col-12}
Showing a rusted iron material

![]({{site.url}}/assets/gameengine/wood_material.png){: .col-12}
Showing a wood material

![]({{site.url}}/assets/gameengine/qt_editor_interface.png){: .col-12}
An early prototype of the editor using QT

![]({{site.url}}/assets/gameengine/imgui_editor.png){: .col-12}
Editor moved and reimplemented in ImGui. (Early ui)

![]({{site.url}}/assets/gameengine/Engine_Qk40NZYm1U.png){: .col-12}
Editor with default layout

![]({{site.url}}/assets/gameengine/Engine_xEhLLv1aRc.png){: .col-12}
Editor with a 4 panel Layout

![]({{site.url}}/assets/gameengine/ChtOkIY4wW-min.gif){: .col-12}
Basic scripting and animation of entities



