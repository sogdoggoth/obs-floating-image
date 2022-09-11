# obs-floating-image
HTML file for a floating image

How to use with OBS:
Step 1: Add your image to the same folder these files are located in.
Step 2: Open config.js and overwrite "./filename.filetype" (default is circle.png) with your image details
NOTE the './' is important
Step 3: Open OBS and create a new Browser source. Point it to 'floatImage.html'
Step 4: Adjust the values in config.js as necessary. You will need to refresh the page

Instructions:

Everything is controlled by the config.js file. 
Open it in any text editor to start making changes

Horizontal values will affect the x axis (left / right)
Vertical values will affect the y axis (up / down)

Distance:
    This determines the speed with which the image moves across the axis.
    A value of 1 will have the image move 30 pixels, 2 at 60 and 2.5 at 75.

Frequency:
    How often an image will 'Bounce' over 3 seconds.

Timing Offset:
    The offset by which the floating animation moves. A value of 0, 0 will have
    the image move in diagonals. A value of 0, 1 will have the image move in 
    a clockwise circle. A value of 0, 3 will have the image move in a counter
    clockwise circle.

Axis Offset:
    This adjusts where in the OBS browser source the image will orbit around.
    Positive numbers move it Up and Left, negative numbers move it Down and Right.

Here's two sets of values to get your started:
    Clockwise circle:
        vertical:{
            frequency:1,
            distance:1,
            timing_offset:1,
            axis_offset:0,
        },
        horizontal:{
            frequency: 1,
            distance: 1,
            timing_offset:0,
            axis_offset:0
        },
        image:{
            location: './circle.png'
        }
    
    Infinite / Figure 8 (change the timing offset and frequency):
         vertical:{
            frequency:2,
            distance:1,
            timing_offset:0,
            axis_offset:0,
        },
        horizontal:{
            frequency: 1,
            distance: 1,
            timing_offset:0,
            axis_offset:0
        },
        image:{
            location: './circle.png'
        }
