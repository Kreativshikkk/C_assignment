# Assignment description (hard, option 5)

The source file has 4 implemented functions to work with .bmp files. Files should have 24 bits per color and be without compression. All functions take some input file and make an output file with changes. Implemented functions make the following changes: 

1. **Inverting** colors in a given circle. The circle can be determined in 2 ways: either coordinates of left upper corner and right lower corner of the square in which the circle is inscribed, or coordinates of the center of the circle and its radius.
2. **Cropping** the image to a specified area. Area is rectangular and determined by coordinates of its upper left corner and coordinates of its lower right corner.
3. **Drawing a triangle**. The operation is determined by: coordinates of triangle's vertices, line thickness, line color, whether to fill the triangle or not, and the color with which it is filled, if the user selects filled.
4. **Drawing a segment**. The operation is determined by: segment's origin coordinates, segment's end coordinates, line color, line thickness.

Program also has Command Line Interface, that is, all functions can be called using console and compiled source file. Further there will be description of parsed arguments to functions, and arguments' flags. In total, program can process 13 different commands:
1. **--function / -f**: Takes as argument written after **--function / -f** string. The argument specifies the function, that will be launched. According to assignment description, you can write (and get some result) the following 4 commands: "invert", "crop", "draw_triangle", "draw_segment", calling 1, 2, 3, 4 functions respectively.
2. **--start / -s**: Takes as argument written after **--start / -s** 2 strings, convertes them to integers. These are coordinates of upper left corner for functions, which can process them (1, 2) or coordinates of the origin of the segment (function 4). Note, that coordinates should be parsed relatively to the lower left corner of the image, and firstly horizontal coordinate should be parsed, then vertical.
3. **--end / -e**: Takes as argument written after **--end / -e** 2 strings, convertes them to integers. These are coordinates of lower right corner for functions, which can process them (1, 2) or coordinates of the end of the segment (function 4). Note, that coordinates should be parsed relatively to the lower left corner of the image, and firstly horizontal coordinate should be parsed, then vertical.
4. **--thickness / -t**: Takes as argument written after **--thickness / -t** integer. Means thickness of the line for functions 3 and 4.
5. **--color_line / -c**: Takes as argument written after **--color / -c** string, specifying the color. Can be used in functions 3 and 4 for line color. There are 10 supported colors: \
5.1: red \
5.2: orange \
5.3: yellow \
5.4: green \
5.5: light-blue \
5.6: blue \
5.7: purple \
5.8: black \
5.9: white \
5.10: gray
6. **--input_file / -i**: Takes as argument written after **--input_file / -i** string, which should specify the name of an input file (for all functions).
7. **--output_file / -o**: Takes as argument written after **--output_file / -o** string, which should specify the name of an output file (for all functions).
8. **--help / -h**: This command allows to print help (description of source code). Does not take any arguments.
9. **--radius / -r**: Takes as argument written after **--radius / -r** integer. Specifies the radius of the circle for function 1.
10. **--center / -c**: Takes asa argument written after **--center / -c** 2 strings, convertes them to integers. These are coordinates of the center of the circle for function 1. Note, that coordinates should be parsed relatively to the lower left corner of the image, and firstly horizontal coordinate should be parsed, then vertical.
11. **--color_fill / -a**: Takes as argument written after **--color / -a** string, specifying the color. Can be used in function 3 to specify the color to fill the triangle. There are 10 supported colors: \
11.1: red \
11.2: orange \
11.3: yellow \
11.4: green \
11.5: light-blue \
11.6: blue \
11.7: purple \
11.8: black \
11.9: white \
11.10: gray
12. **--fill / -b**: Takes as argument written after **--fill / -b** integer. 1 if the triangle should be filled, 0 otherwise.
13. **--vertices / -v**: Takes as argument written after **--vertices / -v** 6 strings, convertes them to integers. These are coordinates of vertices of a triangle in function 3. Note, that coordinates should be parsed relatively to the lower left corner of the image, and firstly horizontal coordinate should be parsed, then vertical. \
\
Finally, the proper command (if run from root assignment directory) looks like this: \
\
./app/solution -f "specified function" "all necessary arguments for the function" -i "name of an input file" -o "name of an output file"
