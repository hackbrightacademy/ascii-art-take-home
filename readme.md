# Take Home Challenge: ASCII Graphics Library

```
╦ ╦┌─┐┌─┐┬┌─┌┐ ┬─┐┬┌─┐┬ ┬┌┬┐  ┬─┐┬ ┬┬  ┌─┐┌─┐┬
╠═╣├─┤│  ├┴┐├┴┐├┬┘││ ┬├─┤ │   ├┬┘│ ││  ├┤ └─┐│
╩ ╩┴ ┴└─┘┴ ┴└─┘┴└─┴└─┘┴ ┴ ┴   ┴└─└─┘┴─┘└─┘└─┘o
```

ASCII art is a term used to describe images that are made of text instead of pixels. It became a popular genre of art in the 70s-80s, back when computers could only handle displaying text on the screen. For example:

```
                   ,%%%,
                 ,%%%` %
                ,%%`( '|
               ,%%@ /\_/
     ,%.-"""--%%% "@@__
    %%/             |__`\
   .%'\     |   \   /  //
   ,%' >   .'----\ |  [/
      < <<`       ||
       `\\\       ||
         )\\      )\
 ^^^^^^^^"""^^^^^^""^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
```

In this take home challenge, you'll implement a library in the language
of your choice for drawing ASCII graphics.

## Specifications

You'll be in charge of implementing the API for drawing **rectangles** (and
squares). The API must be able to:

- Render canvas with a specified height and width
  - Print the canvas and any shapes to standard output
- Add a shape to a canvas
  - **_shape_** the shape to add. For now, assume you only have to deal
    with rectangles
- Clear all shapes from a canvas
- Create a rectangle
  - **_start_x_** is the X coordinate of the upper-left-hand corner of the
    rectangle
  - **_start_y_** is the Y coordinate of the upper-left-hand corner of the
    rectangle
  - **_end_x_** is the X coordinate of the lower-right-hand corner of the
    rectangle
  - **_end_y_** is the Y coordinate of the lower-right-hand corner of the
    rectangle
  - **_fill_char_** is the character that should be used to draw the
    rectangle
- Change a rectangle's fill character
  - **_char_** the character to use in order to draw a pre-existing
    rectangle
- Translate (move left, right, up, or down)
  - **_axis_** which axis (`'x'` or `'y'`) should we translate the rectangle on?
    Translating on the X-axis will cause the rectangle to move left
    and right. Translating on the Y-axis will cause the rectangle to
    move up and down.
  - **_num_** is how much to move the rectangle. Negative numbers will
    cause the rectangle to shift left or down. Positive numbers will cause
    the rectangle to shift right or up.

## Notes

Rectangles can overlap with one another. The most recently added rectangle
should appear on top of other rectangles. For example:

```
 ++++
 ++.....
 ++.....
   .....




```

Make sure you do not render any characters that are out of bounds.

Feel free to make decisions/assumptions about things you have questions about and please document these decisions (using comments in your solution is fine).
