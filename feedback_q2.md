# Feedback for Problem 2

## Loading Data 

* The standard csv way to read a file is to use the reader class in the csv module, but if you observe the data, it's almost like a text file, just that it's structured column-wise as well.
* So a nice way to read this (especially since it has no header, which csv files usually have) is to treat it like a text file and read it line by line into a list, and then split the string with the ',' character, and you get what you want.
* Since you haven't used both of them, I'd suggest that you also try out reading from a csv file and from a text file, even though you'll have libraries like sklearn to help you out with this in the future, you'll need to know how to load assignments from these in the future.

## Organising Data

* If you had taken the data from the csv file, the only thing you needed to do was to reshape a 1D matrix to a 2D matrix. I'm not sure what format sklearn loads the dataset in, but yeah, seems like you've done something similar also, although with some added steps for other reasons I think.
* Okay, seems like you've read from the file and organised below that, so that's fine

Also, you're loading the dataset in each cell, which is not required in jupyter/colab notebooks, once you load it once into an array, you can reuse the array for all subsequent cells. (Or maybe you just wanted to load it in many different ways? I'm not sure)

## Grouping the Data

* For this part, your idea is correct, but you should have used one for loop with 10 iterations, instead of copying the same thing and storing it in 10 different arrays, changing the number and array name in each. You could have used a dictionary or a normal Python list, to store all the images (note that you can't use a numpy array to store it because the number of images in each category would be different, and NumPy only allows homogenous data types)
* Check these two links out as well, they talk about group by using pure NumPy : https://stackoverflow.com/questions/49372918/group-numpy-into-multiple-sub-arrays-using-an-array-of-values and https://stackoverflow.com/questions/49141969/vectorized-groupby-with-numpy?noredirect=1&lq=1

## Computing Mean Images

* Similar problem here of being neater using loops, these are all just good coding practices that will save you time and make it look neater, so if you had used a for loop for the earlier part, you would have used it here as well.

Overall, nice job, you've done whatever we asked for, and hope you learnt something from the assignment and the feedback, do reach out if you have any questions.
