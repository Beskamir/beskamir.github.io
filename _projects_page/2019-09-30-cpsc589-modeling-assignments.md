---
layout: article
title: Computer Graphics Modeling Assignments
key: 20190930
permalink: /projects/modeling-assignments
cover: https://cdnb.artstation.com/p/assets/images/images/021/205/191/large/sebastian-kopacz-2019-10-10-23-57-51.jpg?1570773878
aside:
  toc: true
article_header:
  type: cover
  image:
    src: https://cdna.artstation.com/p/assets/images/images/021/494/878/large/sebastian-kopacz-eyeclean.jpg?1571893582
---

Collection of assignments I did well on for the _modeling_ course (Computer Science 589 at the University of Calgary) I am taking in fall 2019.

<!--more-->

##### Links to additional pictures on my ArtStation
- [Hypocycloid](https://www.artstation.com/artwork/A9n3lo)
- [B-Spline Curve](https://www.artstation.com/artwork/XBvAJR)

##### Links to source code and compiled versions
- Hypocycloid
  - [Source code](https://github.com/Beskamir/Hypocycloid)
  - [Compiled for 64 bit Windows 10](https://github.com/Beskamir/Hypocycloid/releases/tag/1.0)
- B-Spline Curve
  - [Source code](https://github.com/Beskamir/Bsplines)
  - [Compiled for 64 bit Windows 10](https://github.com/Beskamir/Bsplines/releases/tag/1.0)

# Hypocycloid

## Features
- Draws [hypocycloids](https://en.wikipedia.org/wiki/Hypocycloid) of any inner and outer circle radii.
- User can change:
   - Inner and outer circle radii.
   - Resolution of the resulting curve.
   - Speed at the curve is drawn. (How many vertices are generated before showing the curve to the user)
   - Number of complete rotations of the curve.
   - Color of the curve with the alpha value alpha value defining how much of the user defined rgb values should be interpolated with colors based on the coordinates of the curve's vertices.
   - Enable/disable:
      - Outer circle outline.
      - Inner circle outline.
      - Dot indicating where the curve is being drawn.
   - Option to draw a coordinate dependent polynomial curve $$(Q(u)=P_0 + P_1u + P_2u^2, 0 \le u \le 1 )$$ which demonstrates what happens when the weights of a curve do not sum to one.

### Screenshots
<img src="https://cdnb.artstation.com/p/assets/images/images/021/205/187/large/sebastian-kopacz-hypocycloid-2019-10-10-23-46-44.jpg?1570773876" width="100%" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/205/433/large/sebastian-kopacz-hypocycloid-2019-10-11-00-27-14.jpg?1570775402" width="100%" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/205/199/large/sebastian-kopacz-2019-10-10-23-56-30.jpg?1570773886" width="100%" /> 
<img src="https://cdnb.artstation.com/p/assets/images/images/021/204/693/large/sebastian-kopacz-hypocycloid-2019-09-28-18-40-20.jpg?1570771411" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/205/188/large/sebastian-kopacz-hypocycloid-2019-10-10-23-57-30.jpg?1570773875" width="100%" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/205/191/large/sebastian-kopacz-2019-10-10-23-57-51.jpg?1570773878" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/205/194/large/sebastian-kopacz-2019-10-10-23-58-13.jpg?1570774287" width="100%" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/205/437/large/sebastian-kopacz-hypocycloid-2019-10-11-00-29-36.jpg?1570775412" width="100%" />

### Videos
<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/embed/580C-mxMfKY"  frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>

<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/embed/kY9ezw0RxmU"  frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>
<div style="position:relative;padding-top:56.25%;">
  <iframe src="https://www.youtube.com/embed/kPbaJXxvwCQ"  frameborder="0" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;"></iframe>
</div>


## Credits
- [OpenGL Template](https://pages.cpsc.ucalgary.ca/~mmactavi/589/) provided to us by Mia MacTavish (the TA for the course)

---

# B-Spline Curve

## Features
- Based on my assignment 1 code except I replaced the hypocycloid with B-splines.
- Supports modeling:
  - B-splines of any order.
  - Nonuniform standard knot sequences.
  - NURBS (Non-uniform rational basis spline).
- Add/move/delete control points.
- Individually show/hide any element. 
- Edit knots and NURBS from the UI.
- Show de Boor's algorithm as it computes the curve. 

### Screenshots
<img src="https://cdna.artstation.com/p/assets/images/images/021/494/878/large/sebastian-kopacz-eyeclean.jpg?1571893582" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/494/710/large/sebastian-kopacz-bsplines-2019-10-23-22-50-57.jpg?1571892787" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/494/720/large/sebastian-kopacz-bsplines-2019-10-23-22-01-11.jpg?1571892730" width="100%" /> 
<img src="https://cdna.artstation.com/p/assets/images/images/021/494/716/large/sebastian-kopacz-bsplines-2019-10-23-22-03-56.jpg?1571892726" width="100%" />
<img src="https://cdna.artstation.com/p/assets/images/images/021/494/712/large/sebastian-kopacz-bsplines-2019-10-23-22-01-30.jpg?1571892722" width="100%" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/494/715/large/sebastian-kopacz-2019-10-23-21-53-13.jpg?1571892724" width="100%" />
<img src="https://cdnb.artstation.com/p/assets/images/images/021/494/717/large/sebastian-kopacz-2019-10-23-21-53-46.jpg?1571892726" width="100%" />

## Credits
- [OpenGL Template](https://pages.cpsc.ucalgary.ca/~mmactavi/589/) provided to us by Mia MacTavish (the TA for the course)

--- 