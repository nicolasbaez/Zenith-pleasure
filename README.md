# Zenith-pleasure
They're looking at me

![buh](https://github.com/nicolasbaez/Zenith-pleasure/blob/main/xp011.gif)
```javascript
a = 500;
h = 9;
k = 0;
q = 50;
setup = (_) => createCanvas(a, a);
o = (i, j, k) => {
  noFill();
  stroke(i, j, a);
  circle(i, j, 37);
  fill(i, j, a);
  circle(h * cos(k + noise(i, j) * 2) + i, h * sin(k + noise(i, j) * 2) + j, h);
};
draw = (_) => {
  colorMode(HSB, a);
  background(0);
  for (i = q; i < a; i += q) {
    for (j = q; j < a; j += q) o(i, j, k);
  }
  k += 0.1;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp011.gif", 628, { delay: 0, units: "frames" });
  }
}
