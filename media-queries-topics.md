Statement) Various topics under Media Queries:

Responsive Breakpoints:
Media queries are used to define specific CSS rules that apply only when certain conditions are met, such as screen width or device type.

Example:

@media (max-width: 768px) {
  /* CSS rules for screens with a maximum width of 768px */
}
Viewport Units:
Using viewport units (vw, vh, vmin, vmax) allows you to create responsive designs based on the viewport size.

Example:

@media (max-width: 600px) {
  font-size: 4vw; /* Font size that scales with viewport width */
}
Orientation:
Media queries can target the orientation of the device (portrait or landscape).

Example:

@media (orientation: landscape) {
  /* CSS rules for landscape orientation */
}
Device Pixel Ratio:
You can adjust styles based on the device's pixel density.

Example:

@media (min-resolution: 2dppx) {
  /* CSS rules for high-density displays */
}
Retina Images:
Loading higher resolution images for devices with high pixel density.

Example:

@media only screen and (-webkit-min-device-pixel-ratio: 2),
only screen and (min--moz-device-pixel-ratio: 2),
only screen and (-o-min-device-pixel-ratio: 2/1),
only screen and (min-device-pixel-ratio: 2) {
  /* CSS rules for high-resolution images */
}

--------------------------------------------------
SOLUTION = index.html:- <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Media Queries Demo</title>
  <link rel="stylesheet" href="media-queries-demo.css">
</head>
<body>
  <h1>Media Queries Demo</h1>
  <p>Resize the window to see the responsive changes.</p>
  <div class="container">
    <img src="image.jpg" alt="Sample Image">
    <p>This is some sample content.</p>
  </div>
</body>
</html>

 -------------------------
 style.css :- body {
  font-family: sans-serif;
}

.container {
  width: 80%;
  margin: 0 auto;
}

/* Responsive breakpoints */
@media (max-width: 768px) {
  .container {
    width: 90%;
  }
}

@media (max-width: 500px) {
  font-size: 16px; /* Adjust font size for smaller screens */
}

/* Viewport units */
h1 {
  font-size: 4vw; /* Scale heading based on viewport width */
}

/* Orientation */
@media (orientation: landscape) {
  .container {
    /* Apply specific styles for landscape orientation */
  }
}

/* Device pixel ratio */
@media (min-resolution: 2dppx) {
  img {
    width: 100%; /* Display high-resolution images at full width */
  }
}

/* Retina images */
@media only screen and (-webkit-min-device-pixel-ratio: 2),
only screen and (min--moz-device-pixel-ratio: 2),
only screen and (-o-min-device-pixel-ratio: 2/1),
only screen and (min-device-pixel-ratio: 2) {
  img {
    content: url("image-highres.jpg"); /* Load high-resolution image */
  }
}

---------------------------------------------------------
