# Leak report

In the checkwhite.space.c, line 41 contains the calloc function that allocates a slot of every "saved" character. The memory allocated by calloc will not be retrieveable therefore causing the memory leak. To fix this problem, add the funciton free() at the end of the method to free up whatever space allocated by calloc. 
