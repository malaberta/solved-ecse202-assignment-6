Download Link: https://assignmentchef.com/product/solved-ecse202-assignment-6
<br>
The attached file, dbReader.c, contains most of the code for a simple program that builds a database of student records from data stored in two input files: NamesIDs.txt and marks.txt.  Once the database is built, a simple command interpreter is started that responds to the following list of commands:




LN List all the records in the database ordered by last name.

LI List all the records in the database ordered by student ID. FN Prompts for a name and lists the record of the student with the corresponding name.

FI Prompts for a name and lists the record of the student with the

Corresponding ID.

HELP Prints this list.

? Prints this list. Q Exits the program.




The input is case insensitive, e.g., ln, lN, and Ln will all be interpreted as LN.




<h1>Examples</h1>




This program needs to be run from the command line (CMR, Terminal, Bourne shell, etc.).  Assume that the program resides in your eclipse workspace:




cd c:UsersferrieeclipseA6Debug

C:UsersferrieA6Debug&gt;




Before running the program you need to copy NamesIDs.txt and marks.txt into this directory! To check, do a direectory listing:




C:UsersferrieA6Debug&gt;dir




Directory of C:UsersferrieA6Debug&gt;




2019-11-15  03:23 PM             1,064 NamesIDs.txt

2019-11-16  02:14 PM               392 sources.mk

2019-11-16  02:14 PM             1,009 makefile

2019-11-16  02:14 PM            14,444 A6-Fall-2019-Dev

2019-11-15  12:55 PM               231 objects.mk

2019-11-15  03:23 PM               150 marks.txt

2019-11-16  02:14 PM    &lt;DIR&gt;          src

6 File(s)         17,290 bytes

1 Dir(s)  261,675,446,272 bytes free




To start the program:




C:UsersferrieA6Debug&gt;A6-Fall-2019-Dev NamesIDs.txt marks.txt

Building database…

Finished…




sdb:




sdb: LN




Student Record Database sorted by Last Name




<table width="308">

 <tbody>

  <tr>

   <td width="144">Dorethea Benes</td>

   <td width="48"> </td>

   <td width="96">2583</td>

   <td width="20">97</td>

  </tr>

  <tr>

   <td width="144">Teisha Britto</td>

   <td width="48"> </td>

   <td width="96">2871</td>

   <td width="20">68</td>

  </tr>

  <tr>

   <td width="144">Cristobal Butcher</td>

   <td width="48"> </td>

   <td width="96">2969</td>

   <td width="20">77</td>

  </tr>

  <tr>

   <td width="144">Billy Ennals</td>

   <td width="48"> </td>

   <td width="96">2191</td>

   <td width="20">82</td>

  </tr>

  <tr>

   <td width="144">Clarisa Freeze</td>

   <td width="48"> </td>

   <td width="96">2135</td>

   <td width="20">70</td>

  </tr>

  <tr>

   <td width="144">Dante Galentine</td>

   <td width="48"> </td>

   <td width="96">1194</td>

   <td width="20">89</td>

  </tr>

  <tr>

   <td width="144">Nia Stutes</td>

   <td width="48"> </td>

   <td width="96">2872</td>

   <td width="20">97</td>

  </tr>

  <tr>

   <td width="144">Suzi Tait</td>

   <td width="48"> </td>

   <td width="96">2519</td>

   <td width="20">82</td>

  </tr>

  <tr>

   <td width="144">Ciera Woolery</td>

   <td width="48"> </td>

   <td width="96">1531</td>

   <td width="20">81</td>

  </tr>

 </tbody>

</table>




sdb: LI




Student Record Database sorted by Student ID




<table width="308">

 <tbody>

  <tr>

   <td width="144">Dante Galentine</td>

   <td width="48"> </td>

   <td width="96">1194</td>

   <td width="20">89</td>

  </tr>

  <tr>

   <td width="144">Ciera Woolery</td>

   <td width="48"> </td>

   <td width="96">1531</td>

   <td width="20">81</td>

  </tr>

  <tr>

   <td width="144">Clarisa Freeze</td>

   <td width="48"> </td>

   <td width="96">2135</td>

   <td width="20">70</td>

  </tr>

  <tr>

   <td width="144">Billy Ennals</td>

   <td width="48"> </td>

   <td width="96">2191</td>

   <td width="20">82</td>

  </tr>

  <tr>

   <td width="144">Suzi Tait</td>

   <td width="48"> </td>

   <td width="96">2519</td>

   <td width="20">82</td>

  </tr>

  <tr>

   <td width="144">Dorethea Benes</td>

   <td width="48"> </td>

   <td width="96">2583</td>

   <td width="20">97</td>

  </tr>

  <tr>

   <td width="144">Teisha Britto</td>

   <td width="48"> </td>

   <td width="96">2871</td>

   <td width="20">68</td>

  </tr>

  <tr>

   <td width="144">Nia Stutes</td>

   <td width="48"> </td>

   <td width="96">2872</td>

   <td width="20">97</td>

  </tr>

  <tr>

   <td width="144">Cristobal Butcher</td>

   <td width="48"> </td>

   <td width="96">2969</td>

   <td width="20">77</td>

  </tr>

 </tbody>

</table>




sdb: FN

Enter name to search:  Freeze




Student Name:            Clarisa Freeze

Student ID:                  2135

Total Grade:                70




sdb: FI

Enter ID to search: 2519




<table width="206">

 <tbody>

  <tr>

   <td width="144">Student Name:</td>

   <td width="62">Suzi Tait</td>

  </tr>

  <tr>

   <td width="144">Student ID:</td>

   <td width="62">2519</td>

  </tr>

  <tr>

   <td width="144">Total Grade:</td>

   <td width="62">82</td>

  </tr>

 </tbody>

</table>




sdb: foo

Command not understood.




sdb: FN

Enter name to search: Fubar

There is no student with that name.




sdb: FI

Enter ID to search: 0

There is no student with that ID.




sdb: QUIT

Program terminated…




<strong>Approach: </strong>

<strong> </strong>

To get the program to function, you need to implement the following functions:




bNode *addNode_Name(bNode *root, SRecord *Record); bNode *addNode_ID(bNode *root, SRecord *Record); bNode *makeNode(SRecord *data); void inorder(bNode *root); void search_Name(bNode *root, char *data);

void search_ID(bNode *root, int ID);




addNode_Name and addNode_ID are almost identical, the difference being in which quantity is used to order the B-Tree.  The same holds for search_Name and search_ID which implement a binary search on the B-Tree.  The remaining functions, inorder and makeNode, are identical in function to the Java code.  From the class notes and your prior experience with Java, you should be able to create the necessary B-Tree functions.  It is strongly suggested that you code and test these separately.  Once you have this worked out, you can add them to the main code and test each of the supported functions.




The key difficulty in this assignment is understanding the function arguments and returns.  The key data structure is SRecord, which is the structure that holds the student record data.  Each time a new entry is read from the files, a new SRecord object is created and populated with data.  Looking more closely at the code, the SRecord object, Record, is a pointer to the object allocated

– exactly the same as is done in Java. Comparing the addNode functions to their Java counterparts, the root of the B-Tree is passed as an argument in the “C” version whereas it was an instance variable (global) in the Java code.  In “C” it’s usually advisable to avoid global variables is it makes the code less portable and error prone.  You will notice that addNode returns the root node.  When the B-Tree is empty, the first node allocated becomes the root node and is returned to the main program.  In all other instances, it simply returns the same value that it is called with.  In the Java makeNode, the single argument corresponds to the object being added to the tree (aBall); in the “C” version this corresponds to the second argument which is a pointer to SRecord, the structure holding the current record being added.   Aside from the function arguments and “C” pointer notation (the use of -&gt; in place or “.”), the “C” code is largely unchanged from the Java version.  The makeNode function is also similar (-&gt; in place of “.”)  and the use of malloc instead of new; inOrder is similarly straightforward – but must format the data as shown in the examples (hint: look at the printf statements in the FI and FN commands).




For this assignment you are to implement the <em>non-recursive</em> version of makeNode.




What is new here are the two search functions which <em>must</em> be implemented as binary search.  This ends up looking very similar to addNode with the exception that the matching node is returned instead of a new one added.  A few minutes with Google should provide any missing details.  There is one remaining detail, how to return a value from inside a recursion.  In Java we used an instance variable, essentially a global variable accessible from any instance of the recursion.  To avoid complications with pointer-pointers (which we will mostly avoid in this course), we define a static variable bNode *match (which is globally accessible like a Java instance variable) which is used to return a pointer to the matching record.




It is worth doing this assignment carefully, especially if this is your first time developing software.  This covers most of the key topics in Part II and is good preparation for your final exam.




<strong>Instructions: </strong>




Starting off with dbReader.c, modify this program to implement the full simple database program.  The dbReader.c file will compile (with warnings) and run, simply listing the database and starting the command interpreter – with help and quit functional.  Remember to make searches case insensitive.




To obtain full marks, your program must work correctly, avoid the use of arrays except for representing character strings, and be reasonably well commented.




Run the examples shown above and save your output to a file called database.txt.  Place all of your source code in a single file, database.c




Upload your files to myCourses as indicated.