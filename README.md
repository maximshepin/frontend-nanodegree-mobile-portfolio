# frontend-nanodegree-mobile-portfolio
src - original repositary
dist - modified folder

Just load index.html file from dist folder in your browser.
I'll keep ngrok tunnel running for some time: http://61be9238.ngrok.io/



## PART1 - Critical Rendering Path - PageSpeed Score 90+  "index.html - optimization"
![GitHub Logo](/scrshoots/speedtest.png)

1 - Optimized_pizzeria.jpg was used instead of heavy picture in the main page.
2 - Googlefont was replaced with equalent CSS code.
3 - All CSS (Style.css file) inlined (but not Print.css file).
4 - All external JS scripts are Asynchronized.
5 - Js files minified and uglyfied
6 - index.html file itself also minified and uglified

## PART2 - Getting Rid of Jank - Frame Rate 60fps+ while scrolling - "views/pizza.html" and 5-ms while changing pizza size.
![GitHub Logo](/scrshoots/60frame.png)

1 - Refactored "changePizzaSizes" function to avoid unneccasary DOM access
2 - Replaced some jQuery selectors with lighter native JScript (example: getElementsByClassName).
3 - Calculatet base phase out of the loop.
4 - Used variable for lenght property of items to access it outside the loop
5 - "requestAnimationFrame" is used while animating
6 - Amount of moving pizzas objects redused from 100 to 22(what is good for my 2k monitor)
7 - Some CSS tricks used for mover class (transform: translateZ(0);
  will-change: transform;)