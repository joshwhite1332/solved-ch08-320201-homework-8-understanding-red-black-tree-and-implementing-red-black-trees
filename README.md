Download Link: https://assignmentchef.com/product/solved-ch08-320201-homework-8-understanding-red-black-tree-and-implementing-red-black-trees
<br>
<h2>Problem 1: Understanding Red Black Trees</h2>

Make sure you submit your solution in the specified format. Points will be deducted if your solution does not follow the format. For a short explanation of pre-order tree traversal, check this assignment’s last page.

FORMATFORA) ANDB): Write your solutions into the text files solutiona.txt and solutionb .txt, respectively. Each tree is to be represented using pre-order traversal. Separate individual values within trees with single spaces. Separate different trees with new lines. Each node’s value needs to be immediately followed by ’B’ or ’R’, representing the node’s color. Do not add nil nodes. Example: 17B 12R 7R. You are welcome to also upload your detailed solution (drawn trees), into solutiondetailed.pdf. Grading will be based on the .txt files that you submit, but in case they are incorrect, we can give you partial points for the detailed solution. FORMATFORC): Please submit your argumentation in the file solutionc.pdf.

<ul>

 <li>Describe all valid red-black trees that store the numbers 1,2,3,4,5.</li>

 <li>Describe the red-black trees that result after successively inserting the keys [14, 42, 35, 7, 26, 17] into an empty red-black tree. You are required to describe the tree after each insertion, as well as any additional recoloring and balancing.</li>

 <li>Consider a red-black tree formed by inserting <em>n </em>nodes with the algorithm described in class. Argue that if <em>n&gt;</em>1, the tree contains at least one red node.</li>

</ul>

<h2>            Problem 2: Implementing Red Black Trees</h2>

Implement a Red Black Tree (with integer nodes), closely following the specifications and algorithms from the lecture. Write your code either in C++ or Python – no other languages will be accepted. Save your solution to rbt.py for Python and rbt.cpp (header in rbt.h) for C++. Make sure you handle errors appropriately.

Grading will be based on case-tests, therefore make sure that you use the exact naming of functions and classes below. We will test all functions, classes, structs that are listed below. Feel free to define any number of helper functions.

<strong>enum Color </strong>{ RED, BLACK };

<strong>struct Node</strong>

{

5<strong>int </strong>data;

<strong>Color </strong>color;

<strong>Node </strong>*left, *right, *parent;

};

10<strong>class RedBlackTree</strong>

{ <strong>private</strong>:

<strong>Node </strong>*root; <strong>protected</strong>:

15<strong>void </strong>rotateLeft(<strong>Node</strong>*&amp;);

<strong>void </strong>rotateRight(<strong>Node</strong>*&amp;);

<strong>public</strong>:

<strong>RedBlackTree</strong>(); <strong>void </strong>insert(<strong>int</strong>);

20<strong>void </strong>delete(<strong>Node</strong>*&amp;);

<strong>Node</strong>* predecessor(<strong>Node</strong>*&amp;);

<strong>Node</strong>* successor(<strong>Node</strong>*&amp;);

<strong>Node</strong>* getMinimum();

<strong>Node</strong>* getMaximum();

25<strong>Node</strong>* search(<strong>int</strong>);

};

Listing 1: Methods and classes to implement for a Red Black Tree

<h2>Background: Pre-order tree traversal</h2>

Trees can be represented with the pre-order traversal.

<strong>function </strong>preorder(tree):

<ol>

 <li>Write down tree.value.</li>

 <li>Call preorder(tree.left_child)</li>

 <li>Call preorder(tree.right_child)</li>

</ol>

The following tree is represented via pre-order traversal by: a b d e c f.