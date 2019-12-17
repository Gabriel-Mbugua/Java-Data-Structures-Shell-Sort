# Java-Data-Structures-Shell-Sort
An example of how to improve the efficiency of the insertion sort algorithm using the shell sort algorithm.

Normal insertion sort shifts elements within an array with their immediate neighbour in order to sort the array in ascending order. 
The problem with this is that alot of shifting may need to be done if for example the smallest element in the array is at the complete end
of the array and alot of shifting would be required to shift this element all the way to the beginning.

Shell sort shifts elements in an array with a gap between them that is often calculated using either (3^k + 1), where k = array.length, and 
array.length/2. In this case we use the second option. So the element[newElement] we begin with will depend on the number of our gap. So newElement 
will be compared with the element that is newElement - gap spaces away. If [newElement - gap] > newElement then we shift [newElement -gap] to
the position of newElement. Then we check again if from newElement's new position there is an element that is [newElement - gap] spaces away.
If so then repeat the abbove process otherwise we increment to the gap to move to the next element. 

After completing the iteration we go back and get our new gap which is gap/2. Repeat this process for as many iterations needed however the last 
iteration must always have a gap of 1. This will return the algorithm back to a regular insertion algorithm however it will only shift a few times
because some values are already in their correct positions. That is how shell algorithm can increase the efficiency of the insertion algorithm!

