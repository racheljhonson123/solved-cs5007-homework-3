Download Link: https://assignmentchef.com/product/solved-cs5007-homework-3
<br>
<h1>1             Point</h1>

State a class Point that has two instance variables, its rational coordinates self.x and self.y.

<ul>

 <li>Implement in this class a constructor with two arguments, the values of the coordinates. Each argument should have a default value 0<em>.</em>0, allowing to call this method without arguments.</li>

 <li>Write two methods named getX and getY that respecitvely return the value of x and the value of self.y.</li>

 <li>Write a method named setX that takes a rational value as argument and modifies x so as it becomes equal to this value.</li>

 <li>Write a method named setY that takes a rational value as argument and modifies y so as it becomes equal to this value.</li>

 <li>Write a method named toString that returns a string containing the two coordinates of the point self, within parenthesis and separated by a comma.</li>

 <li>Write a method named equals that takes another object of class Point as argument and returns True if the x and y coordinates of this points are equal to the x and y coordinates of self, and returns False</li>

</ul>

Outside from the class, write the following statements: Create a point <em>p</em><sub>1 </sub>of coordinates (0<em>,</em>0) and un point <em>p</em><sub>2 </sub>of coordinates (1<em>,</em>2). Print out the coordinates of the two points on the same line, by calling toString on the two points. Print the result of applying the method equals on point <em>p</em><sub>1</sub>, using <em>p</em><sub>2 </sub>as argument. Set the x coordinate of <em>p</em><sub>2 </sub>equal to the x coordinate of <em>p</em><sub>1</sub>, using the methods setX and getX. Set the y coordinate of <em>p</em><sub>2 </sub>equal to the y coordinate of <em>p</em><sub>1</sub>, using the method setY and getY. Print again the result of applying the method equals on point <em>p</em><sub>1</sub>, using <em>p</em><sub>2 </sub>as argument. Increment by 1 the x coordinate of <em>p</em><sub>2</sub>, using the methods setX and getX . Print again the result of applying the method equals on point <em>p</em><sub>1</sub>, using <em>p</em><sub>2 </sub>as argument.

<h1>2             Rectangle</h1>

State a class Rectangle that has three instance variables: a point (an object of the class Point previously defined, corresponding to the left bottom corner), a rational width and a rational height.

<ul>

 <li>Implement in this class a constructor with three arguments, a point and two rational values, to be assigned to the three instance variables. No default values should be stated (the constructor must be called with three arguments).</li>

 <li>Write a method named perimeter that returns the perimeter of the rectangle.</li>

 <li>Write a method named area that returns the area of the rectangle.</li>

 <li>Write a method named getOrigin that returns a reference to the point representing the left bottom corner of the rectangle.</li>

 <li>Write a method named toString that returns a string containing, on the same line, the string representing the bottom left corner, followed by the rectangle width and height, formatted as follows (the values will differ depending on each object):</li>

</ul>

(0.0,0.0), L=2, H=5.5.

Outside from the class, write the following statements: Create a rectangle <em>r</em><sub>1 </sub>whose bottom left corner is <em>p</em><sub>1</sub>, width is 2 and height is 5<em>.</em>5. Create a rectangle <em>r</em><sub>2 </sub>whose bottom left corner is <em>p</em><sub>2</sub>, width is 3 and height is 6. Print out the bottom left corner of <em>r</em><sub>1 </sub>and the perimeter of <em>r</em><sub>1</sub>, by calling the appropriate methods. Print out the bottom left corner of <em>r</em><sub>2 </sub>and the area of <em>r</em><sub>2</sub>, by calling the appropriate methods. Print the result of the call to the method toString respectively applied to the two rectangles <em>r</em><sub>1 </sub>and <em>r</em><sub>2</sub>.

<h1>3             Movable rectangle</h1>

State a class MovableRectangle that inherits from class Rectangle. This class has a supplementary instance variable, assumed to be boolean, called self.move.

<ul>

 <li>Implement in this class a constructor with three arguments, a point and two rational values, to be assigned to the three instance variables. move is initially always set to False. Your code MUST call the constructor of the superclass.</li>

 <li>Write a method named unlock that sets move to True.</li>

 <li>Write a method named lock that sets move to False.</li>

 <li>Write a method named moveTo that takes an object of class Point as argument, and: If the rectangle is unlocked, moves it so as its new bottom left is the point given as argument. Otherwise, the method prints the following message: Warning: locked.</li>

 <li>Write a method named toString that returns a string containing, on the same line, the string representing the bottom left corner, followed by the rectangle width and height, followed by the current status (locked or unlocked) formatted as follows (the values will differ depending on each object):</li>

</ul>

(5,15), W=2, H=2, Movable? True

(if it is locked, the end of string should be …Movable? False).

Outside from the class, write the following statements: Create a movable rectangle <em>r</em><sub>3 </sub>whose bottom left corner is <em>p</em><sub>1</sub>, width is 2 and height is 2. Print the rectangle <em>r</em><sub>3</sub>, using toString. Create a point <em>p</em><sub>3 </sub>of coordinates (5<em>,</em>15). Call the method moveTo on rectangle <em>r</em><sub>3 </sub>in order to try moving its origin to <em>p</em><sub>3</sub>. Print again the rectangle <em>r</em><sub>3</sub>, using toString. Unlock <em>r</em><sub>3</sub>. Call again the method moveTo on rectangle <em>r</em><sub>3 </sub>in order to try moving its origin to <em>p</em><sub>3</sub>. Print again the rectangle <em>r</em><sub>3</sub>, using toString.

<h1>4             Extra-credit : Read File (5 points)</h1>

Create a class Tour with a single instance variable self.MyList that will refer to a list object. Create a constructor that takes one string parameter, the name of a file, filename. This class deals with files representing sets of cities. You will find on the course website some data files tourX.csv, where X is the number of cities in the set. If you open such a file with a <em>text </em>editor, you will see that the file states one city per row: name, <em>x </em>coordinate, <em>y </em>coordinate. The constructor must assign the instance variable self.MyList using the file whose name is given as argument (string parameter filename, assumed to be one of the files tourX.csv). When called, the argument is directly a file name, not a path. The constructor assigns to self.MyList a list of the following form (the above text is just an example used to show the expected format):

[[’Atlanta’, ’22’, ’3’], [’Augusta’, ’46’, ’28’], <em>…</em>]

<em>Note: in such a list </em>[[’Atlanta’, ’22’, ’3’], [’Augusta’, ’46’, ’28’], <em>…</em>]<em>, all elements in sublists are strings (not integers).</em>