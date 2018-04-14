###### Approximating a circular arc to Bezier Curve (approximate2circulararc.py)

This script is to approximate a circular arc to a bezier curve

    Input:
        - waypoint ids
        - left turn (0) or right turn (1)
        - two points (P1,P2) on the circle in counter-clock wise 
            (Location of the waypoints between which the circular arc is being fit)
        - center of the circle (C)
        (Angle between CP1,CP2 should not exceed 180. In this case split the arc)
    Output:
        - Control points written in a text file

**def** roateP(point)

This function is to rotate a point 90 degrees counterclockwise.

Args:
    point : a point with x and y coordinates in a list or tuple
    

Returns:
    a numpy array of size (2,1) with x and y coordinates after rotating
    the point

```python
    >>> from approximate2circulararc import *
    >>> a = [1,2]
    >>> b = rotateP(a)
```

**def** bezierControlPoints(point1, point2, center)

Args:
    point1 : a point with x and y coordinates in a list or tuple
    point2 : a point with x and y coordinates in a list or tuple
    center : a point with x and y coordinates in a list or tuple

returns:
    A list of two control points between point1 and point2

This function function accepts the two end points of the circular arc and the center as inputs and returns
the control points for a bezier curve that approximates the circular arc

```python
    >>> from approximate2circulararc import *
    >>> point1 = [0,1]
    >>> point2 = [1,0]
    >>> center = [0,0]
    >>> control_points = bezierControlPoints(point1,point2,center) 
```  
