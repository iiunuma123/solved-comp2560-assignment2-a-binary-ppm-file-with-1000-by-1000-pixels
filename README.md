Download Link: https://assignmentchef.com/product/solved-comp2560-assignment2-a-binary-ppm-file-with-1000-by-1000-pixels
<br>
Write a C program to create a binary ppm file with 1000 by 1000 pixels. It uses five input colors to draw a picture. See sample runs. The input colors can be: red, green, blue, yellow, orange, cyan, magenta, ocean, violet. The corners of the central part should use the 250<sup>th</sup> and 750<sup>th</sup> row/column.

Restrictions on the file format:

<ul>

 <li>no comment line after the file type specification</li>

 <li>width (number of columns) and height (number of rows) formatted in ASCII decimal in the second line, separated by a space</li>

 <li>maximal value of color components given in the third line</li>

</ul>

Requirements on parallel execution:

<ul>

 <li>The original process should write the header information into the image file.</li>

 <li>Use <em>fork()</em> to create 10 child processes. Each child process can use about 300KB of memory to calculate 100 rows and write the data into the image file.</li>

 <li>The original process does not work on the pixels. It creates the 10 child processes to do so. To avoid having multiple child processes simultaneously accessing the image file, the parent process simply waits for one child process to terminate before creating the next.</li>

</ul>

Other requirements:

<ul>

 <li>You are not allowed to use standard I/O library functions or graphics related libraries.</li>

 <li>The command line arguments include the following in order: (i) the name of the image file; (ii) color for center; (iii) color for top-left corner; (iv) color for top-right corner; (v) color for bottom-left corner; (vi) color for bottom-right corner.</li>

</ul>







Advanced requirements (optional):




<ul>

 <li>The numbers of rows and columns of the image are not fixed numbers. They are also command line arguments.</li>

 <li>The number of child processes is not a fixed number. It is also a command line argument.</li>

</ul>







Marking scheme:




<ul>

 <li>5 logically clear</li>

 <li>5 follow the instructions and correctly use <em>fork() </em>etc.</li>

 <li>5 successfully compile</li>

 <li>5 pass all tests</li>

</ul>

<em>60-256 System Programming                                                                                                          Dr. Chen </em>

Sample runs:




&gt;&gt;&gt;&gt;&gt; kindergarten drawing.ppm blue green red yellow magenta

&gt;&gt;&gt;&gt;&gt; gimp drawing.ppm
















&gt;&gt;&gt;&gt;&gt; kindergarten drawing.ppm orange ocean yellow violet cyan

&gt;&gt;&gt;&gt;&gt; gimp drawing.ppm


