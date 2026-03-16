For a 2D dart game in Java (likely using Swing or Java2D), target a base game resolution like 800x600 or 1024x768 pixels for good compatibility across screens. Create assets at powers of 2 dimensions (e.g., 256x256, 512x512) matching their on-screen size to avoid scaling artifacts, or 2x that size (e.g., 512x512 or 1024x1024) for sharper downscaling with bilinear filtering.

Dartboard Assets
Make the main dartboard sprite 512x512 or 1024x1024 pixels to fill much of the screen as the central element (e.g., 60-80% of height in 800x600). Include separate layered sprites for details like numbers or bullseye at 256x256 if animating segments.
​

Dart Assets
Design individual darts as thin sprites: 64x256 or 128x512 pixels (width x length) for flight animations across 4-8 frames. Use 128x128 for close-up or hand-held views.

Implementation Tips
Use Graphics2D.scale() in your paintComponent for resolution-independent rendering based on window size. Power-of-2 sizes optimize texture handling; test at your target resolution to refine.
