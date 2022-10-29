<template>
  <router-view />
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Overpass:wght@400;700&display=swap");
/* font-family: 'Overpass', sans-serif; */

*,
*::before,
*::after {
  box-sizing: border-box;
}
* {
  margin: 0;
}
html,
body {
  height: 100%;
}
body {
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
  font-size: 15px;
}
img,
picture,
video,
canvas,
svg {
  display: block;
  max-width: 100%;
}
input,
button,
textarea,
select {
  font: inherit;
}
p,
h1,
h2,
h3,
h4,
h5,
h6 {
  overflow-wrap: break-word;
}
#root,
#__next {
  isolation: isolate;
}

:root {
  /* primary */
  --orange: hsl(25, 97%, 53%);

  /* neutral */
  --white: hsl(0, 0%, 100%);
  --lgrey: hsl(217, 12%, 63%);
  --mgrey: hsl(216, 12%, 54%);
  --dblue: hsl(213, 19%, 18%);
  --vdblue: hsl(216, 12%, 8%);
}
</style>
