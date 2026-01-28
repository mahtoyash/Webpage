# cursor animation

ok so this code makes your cursor have a trailing effect. when you move your mouse it leaves behind red glowing squares and a white comet tail.
it grabs the canvas and makes it fullscreen. theres this PIXEL_SIZE set to 35 which controls the square sizes.
when you move your mouse it tracks the position and figures out which grid square your in. like the screen is divided into 35x35 boxes. whenever you enter a new box it gets added to a Map with some transparency so your basically painting red squares as you move.
the trail doesnt just jump to your mouse, it smoothly chases after it by moving 15% of the distance each frame. keeps track of last 15 positions to draw the comet tail.
it draws white squares along the trail that fade out and get smaller. the red pixels also fade out each frame (alpha -= 0.05) until they disappear. when fully faded they get deleted from the map.
if you resize window it updates canvas size.
