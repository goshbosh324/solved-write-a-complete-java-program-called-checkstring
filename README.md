Download Link: https://assignmentchef.com/product/solved-write-a-complete-java-program-called-checkstring
<br>
<ol>

 <li>Write a complete Java program called CheckString according to the following guidelines.</li>

</ol>

** Each method below, including main, should handle (catch) any Exceptions that are thrown. **




** If an Exception is thrown and caught, print the Exception’s message to the command line. **

You main method should do the following in the order specified, where the methods referred to are further described below:




<ol>

 <li>Call the getWord method and print the result to the command line.</li>

 <li>Create an array of Strings called testInputData and populate it with at least three elements.</li>

 <li>Call the writeTextFile method above, passing the array you created in exercise step 2 above and the String “data.txt”.</li>

 <li>Call the readTextFile method to read the file you wrote in step 3 above. Assign the result of readTextFile to an ArrayList variable in main called fileContents.</li>

 <li>Write a loop to print the contents of the fileContents ArrayList to the command line.</li>

</ol>

The getWord method takes no parameters and returns a String. This method prompts the user for a word, and then calls the checkWord method (see below), passing as a parameter the word the user provided as input. Make sure the getWord method handles the Exception that may be thrown by the checkWord method.

The checkWord method takes a String parameter named word, returns nothing, and is declared to throw an Exception of type Exception. In the method, check if the first character of the parameter is a letter. If it is not a letter, the method throws an Exception of type Exception with the message of: “This is an invalid word entry.”

The writeTextFile method takes two parameters: an array of Strings (named arrayToWrite) and a String (named inputFilename). The method writes the Strings in the arrayToWrite array to a text file named filename (the parameter), with each String on a separate line.

The readTextFile method takes a String as a parameter (filename) and returns an ArrayList of Strings (fileContents). The method reads the text file identified by the filename parameter and populates the ArrayList with an element for each line in the text file.







<ol start="2">

 <li>Write a complete Java program called CalcWeightedAvgDropLowest according to the following guidelines.</li>

</ol>

For this program, instead of getting the data from the user via System.in, get only input and output file names from the user. See Horstmann’s program Total.java in Section 7.1, pp. 319, 320, on which this assignment is based.

Also note that the methods for getting input and writing output will need to handle exceptions, whereas in Horstmann’s Total.java example, only the main needs to handle exceptions. The simplest (and recommended) way to handle exceptions in this program is to have the two methods that read and write data each throw a FileNotFoundException. We’ll see in a later program how to handle exceptions differently.

Input File

The input file – which you need to create and prompt the user for the name of – should be called ‘data.txt’, and it should be created according to the instructions below.

The input file should contain (in order): the weight (greater than 0 and less than or equal to 1), the number, n, of lowest numbers to drop, and the numbers to be averaged after dropping the lowest n values.

For example, you might have these values in your input file (data.txt):

0.5 3 10 70 90 80 20

Creating the Input file

To create the input file, while in NetBeans with your project open, click to highlight the top-level folder of your project in the projects tab at the upper left. Then starting with the NetBeans File menu, do

File-&gt;New File




Keep the Project name at the top; keep Filter blank




For Categories choose Other (at the bottom of the categories list)

For File Types choose Empty File (at the bottom of the files list)




Next




FileName: data.txt




Folder: this should be blank; if it’s not, delete whatever’s there.




Finish

In the empty file data.txt that you just created, add a single line of data like the one in the example above, where the weight is a double (greater than 0.0 and less than or equal to 1.0) and the other numbers are the number, n, of lowest values to drop, and then the numbers to be averaged after dropping the lowest n values. Then save this data.txt input file.

<em>It’s important that your input file is where NetBeans will look to find it.</em> The above instructions should make sure that that happens.

Main method

Your main method should contain just three lines like these:

ArrayList inputValues = getData();

double weightedAvg = calcWeightedAvg(inputValues);

printResults(inputValues, weightedAvg);

where the printResults method should prompt the user for the name of the output file and print to that output file.

Output

Given the sample values above in the data.txt input file, the output file should contain something very much like the following:

The weighted average of the numbers is 42.5, when using the data 10.0, 70.0, 90.0, 80.0, 20.0, where 0.5 is the weight used, and the average is computed after dropping the lowest 3 values.

Prompting for names of input file and output file

Make sure you prompt the user for the name of the input file (even though we know what it is). You can use a prompt like: “Enter “data.txt” (no quotes) for the name of the input file: ”

Also prompt the user for the name of the output file. If you use code like that in Horstmann’s Total.java program to create the output file, the output file should be located at the same place as the input file. Check the NetBeans Files tab (next to the Project tab in the upper left) to see both the input and output files.




<ol start="3">

 <li>Create a program called CalcWeightedAvgWithExceptions, according to the following guidelines and<em>using try-catch-finally blocks in your methods that read from a file and write to a file</em>, as in the examples in the lesson notes for reading and writing text files.</li>

</ol>

<h2>Input File</h2>

The input file – which you need to create and prompt the user for the name of – should be called ‘data.txt’, and it should be created according to the instructions below.

The input file should contain (in order): the weight (greater than 0 and less than or equal to 1), the number, n, of lowest numbers to drop, and the numbers to be averaged after dropping the lowest n values.

For example, you might have these values in your input file (data.txt):

0.5 3 10 70 90 80 20

<h3>Creating the Input file</h3>

To create the input file, while in NetBeans with your project open, click to highlight the top-level folder of your project in the projects tab at the upper left. Then starting with the NetBeans File menu, do

File-&gt;New File Keep the Project name at the top; keep Filter blank For Categories choose Other (at the bottom of the categories list)For File Types choose Empty File (at the bottom of the files list) Next FileName: data.txt Folder: this should be blank; if it’s not, delete whatever’s there. Finish

In the empty file data.txt that you just created, add a single line of data like the one in the example above, where the weight is a double (greater than 0.0 and less than or equal to 1.0) and the other numbers are the number, n, of lowest values to drop, and then the numbers to be averaged after dropping the lowest n values. Then save this data.txt input file.

<em>It’s important that your input file is where NetBeans will look to find it.</em> The above instructions should make sure that that happens.

<h2>main method</h2>

Your main method should contain just three lines like these:

ArrayList inputValues = getData();

double weightedAvg = calcWeightedAvg(inputValues);

printResults(inputValues, weightedAvg);

where the printResults method should prompt the user for the name of the output file and print to that output file.

<h2>Output</h2>

Given the sample values above in the data.txt input file, the output file should contain something very much like the following:

The weighted average of the numbers is 42.5, when using the data 10.0, 70.0, 90.0, 80.0, 20.0, where 0.5 is the weight used, and the average is computed after dropping the lowest 3 values.

<h2>Prompting for names of input file and output file</h2>

Make sure you prompt the user for the name of the input file (even though we know what it is). You can use a prompt like: “Enter “data.txt” (no quotes) for the name of the input file: ”

Also prompt the user for the name of the output file. If you use code like that in Horstmann’s Total.java program to create the output file, the output file should be located at the same place as the input file. Check the NetBeans Files tab (next to the Project tab in the upper left) to see both the input and output files.


