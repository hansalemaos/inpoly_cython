<h2>inpoly-cython / Original: https://github.com/dengwirda/inpoly-python</h2>

```python

$pip install inpoly-cython

Project from: https://github.com/dengwirda/inpoly-python
I only added the automatic compilation of the fast kernels: https://github.com/dengwirda/inpoly-python#fast-kernels


License Terms (from https://github.com/dengwirda/inpoly-python)
This program may be freely redistributed under the condition that the copyright notices (including this entire header) are not removed, and no compensation is received through use of the software. Private, research, and institutional use is free. You may distribute modified versions of this code UNDER THE CONDITION THAT THIS CODE AND ANY MODIFICATIONS MADE TO IT IN THE SAME FILE REMAIN UNDER COPYRIGHT OF THE ORIGINAL AUTHOR, BOTH SOURCE AND OBJECT CODE ARE MADE FREELY AVAILABLE WITHOUT CHARGE, AND CLEAR NOTICE IS GIVEN OF THE MODIFICATIONS. Distribution of this code as part of a commercial system is permissible ONLY BY DIRECT ARRANGEMENT WITH THE AUTHOR. (If you are not directly supplying this code to a customer, and you are instead telling them how they can obtain it for free, then you are not required to make any arrangement with me.)

DISCLAIMER: Neither I nor the University of Sydney warrant this code in any way whatsoever. This code is provided "as-is" to be used at your own risk.

Example: 

from inpoly_cython import inpoly2
import numpy as np
    
xmin, xmax, ymin, ymax = 0, 1, 0, 1
x0, y0, x1, y1 = 0.5, 0.5, 0, 1

#define any n-sided polygon
p = np.array([[xmin, ymin],
              [xmax, ymin],
              [xmax, ymax],
              [xmin, ymax],
              [xmin, ymin]])

#define some coords
coords = np.array([[x0, y0],
                   [x1, y1]])

#get boolean mask for points if in or on polygon perimeter
isin, ison = inpoly2(coords, p)


```


