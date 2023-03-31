OS can be stuctured in layers. These layers are completely contained in all outer layers. The farer out the layer the higher the level of abstraction. These layers communicate with adjacent layers through well defined interfaces. A layer can only access routines of the adjacent inner layer and exposes functions to the adjacent outer layers. Functions that a layer exposes are called *services* and functions which operate in the same layer are called *protocols*.
Minimum are 3 layers:
1. the inner layers contain the hardware dependent components of the OS
2. the middle layers contain basic libraries and interfaces for devices and data
3. the outer layers contain user application and the user interface
