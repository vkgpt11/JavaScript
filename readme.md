## How does javascript, HTML and CSS get to web browser?
https://www.youtube.com/watch?v=XQpZIEejKDY

## Which one is faster JavaScript or TypeScrip?

## When do you need functional programming vs object oriented programming vs reactive programming?

## What is the need to JavaScript when we can create web pages using HTML and CSS?

## What is diffrence between JavaScript and TypeScript?

## Which HTTP verb will you use to filter items with 20 parameters? GET or POST?


https://github.com/Pau1fitz/react-interview#how-does-react-work
https://github.com/sudheerj/reactjs-interview-questions


## How do you call an API in java script?
https://stackoverflow.com/questions/36975619/how-to-call-a-rest-web-service-api-from-javascript

## what is promis in javascript?
https://www.geeksforgeeks.org/javascript-promises/

## HTML5 questions on canvas and svg?
There's a difference in what they are, and what they do for you.

    > SVG is a document format for scalable vector graphics.
    > Canvas is a javascript API for drawing vector graphics to a bitmap of a specific size.
> To elaborate a bit, on format versus API:
    > With svg you can view, save and edit the file in many different tools. With canvas you just draw, and nothing is retained about what you just did apart from the resulting image on the screen. You can animate both, SVG handles the redrawing for you by just looking at the elements and attributes specified, while with canvas you have to redraw each frame yourself using the API. You can scale both, but SVG does it automatically, while with canvas again, you have to re-issue the drawing commands for the given size.


Two things that hit me the most for SVG and Canvas were,

      > Ability to use Canvas without the DOM, where as SVG depends heavily on DOM and as the complexity increases the performance slows down. Like in game design.

      > Advantage of using SVG would be that resolution remains the same across platforms which lacks in Canvas.
