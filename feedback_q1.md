In the class Tester, there are following issues in the functions: 

1. def iterative_mult(w) :
* Needs to be changed to def iterative_mult(self, w), and the class variable M needs to be accessed using self.M
* A matrix is stored in a "row-major" form, and w is a row vector itself, so in the code you are multiplying two rows together. In matrix multiplication, you need to multiply row by column.
* If you want to multiply two matrices you should use np.matmul() or np.dot(). The * operator is for element-wise multiplication

2. def matrix_mult(w) :
* A self parameter needs to be added (similar to point 1). 
* w is already a numpy array, so the first statement is unnecessary. Also, the print statement is unnecessary
* np.multiply doesn't work for matrix multiplication, the functions in the last comment of point 1 work.
* You need to vectorise the sum as well. The purpose of this function is to eliminate for loops entirely.
* The expected answer was np.sum(np.matmul(self.w, self.M)). As you can see, for loops are absent here.

3. def comparison(w) :
* This function shouldn't return arrays but two scalars. I don't understand why the time printed is an array. Maybe you can google the function timeit.timeit

4. Plotting
* The plot itself should be based upon two arrays only. Since the output of 3. is wrong, I don't understand what is being plotted.
* The legend is missing
* Since the data consists of powers of 10, it is good practice to use logarithmic scale for plotting such data
