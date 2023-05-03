Download Link: https://assignmentchef.com/product/solved-cs224-lab-6-cache-design-parameters
<br>
In this lab you will study the effect of various cache design parameters.  The first part includes problem solving and writing a program. The second part, the lab part, involves execution of the program (with possible extensions etc. if suggested by your TA) and preparing a report.

In your solutions and report make sure that you have proper tables, numbering etc. All tables must have subtitle and table number furthermore columns must have column names, etc. In your report make sure that you have a nice presentation. Make sure that you number the pages. Try to do everything before coming to the lab but make sure that you demonstrate your work to your TA.

<strong>Summary </strong>

<strong>Part 1</strong> : Preliminary Report/Preliminary Design Report: Involves problem solving related to cache memory design and a program written for cache testing.

<strong>Part 2</strong> : Experiments with caching and experiment report.

<strong>DUE DATE/TIME OF PART 1 –SAME FOR ALL SECTIONS (WEDNESDAY DEC. 18th, 10:40 AM)</strong>

<ol>

 <li>Dear students please bring and drop your preliminary work report into the box provided in front of the lab before 10:40 AM. No late submission!</li>

 <li>Please <strong>upload your Preliminary Design Program (only program part) </strong>to the Unilica Assignment for Preliminary Work by 10:40 AM on Wednesday. Use filename <strong>txt</strong></li>

</ol>




<strong>DUE TIME OF PART 2—DIFFERENT FOR EACH SECTION:</strong>

<ol>

 <li>You have to demonstrate your Part 2 lab work to the TA for grade by <strong>12:15</strong> in the morning lab and by <strong>17:15</strong> in the afternoon lab. Your TAs may give further instructions on this. If you wait idly and show your work last minute, 20 points may be taken off from your grade.</li>

 <li>At the conclusion of the demo for getting your grade, you will <strong>upload your lab program</strong> to the Unilica Assignment, for similarity testing by MOSS. It may be slightly different from the preliminary design program depending on the options defined below or as suggested by your TA.</li>

</ol>

You will also <strong>upload your lab report</strong> to the Unilica Assignment, for similarity testing by MOSS Please see the related section below for further instructions on MOSS and lab report submission.

<strong>If we suspect that there is cheating, we will send the work with the names of the students to the university disciplinary committee.</strong>

<strong>Part 1. Preliminary Work / Preliminary Design Report (50 points)</strong>




You have to provide a neat presentation prepared by <u>Word or a word processor with similar output quality. Handwritten answers will <strong>not be accepted</strong></u>. At the top of the paper on left provide the following information and staple all papers. Please make sure that this info is there for proper grading of your work, otherwise some points will be taken off.




CS224

Section No.: …

Lab No.:

Your Full Name/Bilkent ID:




Solve the problems of this part and print and leave your report in the box provided in the lab as described above. Number the pages, staple your submission and use a word processor for its preparation. Only the program will be uploaded as described above.




<ol>

 <li> <strong>With 3 or more errors you get 0 points. Otherwise full point.)</strong> Fill in the empty cells of the following table. Assume that main memory size is 4GB. <strong>Index Size</strong>: No. of bits needed to express the set number in an address, <strong>Block Offset</strong>: No. of bits needed to indicate the word offset in a block, <strong>Byte Offset</strong>: No. of bits needed to indicate the byte offset in a word. <strong>Block Replacement Policy Needed</strong>: Indicate if a block replacement policy such as FIFO, LRU, LFU etc. is needed (yes) or not (no). If some combinations are not possible mark them.</li>

</ol>

<table>

 <tbody>

  <tr>

   <td><strong>No.</strong></td>

   <td><strong>Cache</strong><strong>Size KB</strong></td>

   <td><strong>N way</strong><strong>cache</strong></td>

   <td><strong>Word</strong><strong>Size</strong></td>

   <td><strong>Block size</strong><strong>(no. of words)</strong></td>

   <td><strong>No. of</strong><strong>Sets</strong></td>

   <td><strong>Tag Size</strong><strong>in bits</strong></td>

   <td><strong>Index Size</strong><strong>(Set No.) in bits</strong></td>

   <td><strong>Word Block</strong><strong>Offset</strong><strong>Size in bits</strong><strong><sup>1</sup></strong></td>

   <td><strong>Byte</strong><strong>Offset</strong><strong>Size in bits</strong><strong><sup>2</sup></strong></td>

   <td><strong>Block</strong><strong>Replacement</strong><strong>Policy Needed (Yes/No)</strong></td>

  </tr>

  <tr>

   <td>1</td>

   <td>64</td>

   <td>1</td>

   <td>32 bits</td>

   <td>4</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>2</td>

   <td>64</td>

   <td>2</td>

   <td>32 bits</td>

   <td>4</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>3</td>

   <td>64</td>

   <td>4</td>

   <td>32 bits</td>

   <td>8</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>4</td>

   <td>64</td>

   <td>Full</td>

   <td>32 bits</td>

   <td>8</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>9</td>

   <td>128</td>

   <td>1</td>

   <td>16 bits</td>

   <td>4</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>10</td>

   <td>128</td>

   <td>2</td>

   <td>16 bits</td>

   <td>4</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>11</td>

   <td>128</td>

   <td>4</td>

   <td>16 bits</td>

   <td>16</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

  <tr>

   <td>12</td>

   <td>128</td>

   <td>Full</td>

   <td>16 bits</td>

   <td>16</td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

   <td> </td>

  </tr>

 </tbody>

</table>

<strong><sup>1 </sup></strong><strong>Word Block Offset Size in bits: </strong>Log<sub>2</sub>(No. of words in a block)

<strong><sup>2 </sup></strong><strong>Byte Offset Size in bits: </strong>Log<sub>2</sub>(No. of bytes in a word)




<ol start="2">

 <li><strong>2</strong>. <strong>With 3 or more errors you get 0 points. Otherwise full point.)</strong> Consider the following MIPS code segment. Cache capacity is 8 words, Block size: 2 words, N= 1.</li>

</ol>

addi       $t0, $0, 5

loop:              beq        $t0, $0, done

lw           $t1, 0x4($0)

lw           $t2, 0xC($0)

lw           $t3, 0x8($0)

addi       $t0, $t0, -1

j               loop

done:




<ol>

 <li>In the following table indicate the type of miss, if any: Compulsory, Conflict, Capacity.</li>

</ol>

<table>

 <tbody>

  <tr>

   <td rowspan="2" width="107"><strong>Instruction</strong></td>

   <td colspan="6" width="519"><strong>Iteration No.</strong></td>

  </tr>

  <tr>

   <td width="104"><strong>1</strong></td>

   <td width="104"><strong>2</strong></td>

   <td width="104"><strong>3</strong></td>

   <td width="104"><strong>4</strong></td>

   <td width="104"><strong>5</strong></td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="107">lw $t1, 0x4($0)</td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="107">lw $t2, 0xC($0)</td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="107">lw $t3, 0x8($0)</td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="1"> </td>

  </tr>

 </tbody>

</table>




<ol>

 <li>What is the total cache memory size in number of bits? Include the V bit your calculations. Show the details of your calculation.</li>

</ol>




<ol>

 <li>State the number of AND and OR gates, EQUALITY COMPARATORs and MULTIPLEXERs needed to implement the cache memory.</li>

</ol>







<ol start="3">

 <li><strong>3</strong>. <strong>(5 points:</strong> <strong>With 3 or more errors you get 0 points. Otherwise full point.)</strong> Consider the above MIPS code segment. The cache capacity is 2 words, block size is 1 word. There is only 1 set. The block replacement policy is LRU.</li>

</ol>




<ol>

 <li>In the following table indicate the type of miss, if any: Compulsory, Conflict, Capacity.</li>

</ol>

<table>

 <tbody>

  <tr>

   <td rowspan="2" width="107"><strong>Instruction</strong></td>

   <td colspan="6" width="519"><strong>Iteration No.</strong></td>

  </tr>

  <tr>

   <td width="104"><strong>1</strong></td>

   <td width="104"><strong>2</strong></td>

   <td width="104"><strong>3</strong></td>

   <td width="104"><strong>4</strong></td>

   <td width="104"><strong>5</strong></td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="107">lw $t1, 0x4($0)</td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="107">lw $t2, 0xC($0)</td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="1"> </td>

  </tr>

  <tr>

   <td width="107">lw $t3, 0x8($0)</td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="104"> </td>

   <td width="1"> </td>

  </tr>

 </tbody>

</table>







<ol>

 <li>How many bits are needed for the implementation of LRU policy? What is the total cache memory size in number of bits? Include the V bit and the bit(s) used for LRU in your calculations. Show the details of your calculation.</li>

</ol>




<ol>

 <li>State the number of AND and OR gates, EQUALITY COMPARATORs and MULTIPLEXERs needed to implement the cache memory.</li>

</ol>







<ol start="4">

 <li><strong>4</strong>. <strong>(5 points)</strong> Consider a three-level memory: L1 and L2 are for cache memory and the third level is for the main memory. Access time for L1 is 1 clock cycle, the access time for L2 is 4 times more than L1 and main memory access time is 10 times more than L2. The miss rate for L1 is 20% and the miss rate for L2 is 5%. What is the effective clock cycle for memory access (AMAT in number of clock cycles)?</li>

</ol>

With 4 GHz clock rate how much time is needed for a program with 10<sup>12</sup> instructions to execute?

Show your work briefly.




<ol start="5">

 <li><strong>5</strong>. <strong>(30 points)</strong> Write a program to find the summation of the elements of a square matrix. Provide a user interface for user interaction to demonstrate that your program is working properly. Assume that in the main memory matrix elements are placed column by column. Create an array for the matrix elements and initialize them column by column with consecutive values. For example, a 3 by 3 (N= 3) matrix would have the following values.</li>

</ol>




<table>

 <tbody>

  <tr>

   <td>1</td>

   <td>4</td>

   <td>7</td>

  </tr>

  <tr>

   <td>2</td>

   <td>5</td>

   <td>8</td>

  </tr>

  <tr>

   <td>3</td>

   <td>6</td>

   <td>9</td>

  </tr>

 </tbody>

</table>




The column by column placement means that you will have the values of the above 3 x 3 matrix are stored as follows in the memory.

<table>

 <tbody>

  <tr>

   <td><strong>Matrix Index</strong><strong>(Row No., Col. No.)</strong></td>

   <td>(1, 1)</td>

   <td>(2, 1)</td>

   <td>(3, 1)</td>

   <td>(1, 2)</td>

   <td>(2, 2)</td>

   <td>(3, 2)</td>

   <td>(1, 3)</td>

   <td>(2, 3)</td>

   <td>(3, 3)</td>

  </tr>

  <tr>

   <td><strong>Displacement</strong><strong>With respect the beginningof the array containing the matrix</strong></td>

   <td>0</td>

   <td>4</td>

   <td>8</td>

   <td>12</td>

   <td>16</td>

   <td>20</td>

   <td>24</td>

   <td>28</td>

   <td>32</td>

  </tr>

  <tr>

   <td><strong>Value stored</strong></td>

   <td>1</td>

   <td>2</td>

   <td>3</td>

   <td>4</td>

   <td>5</td>

   <td>6</td>

   <td>7</td>

   <td>8</td>

   <td>9</td>

  </tr>

 </tbody>

</table>




In this configuration accessing the matrix element (i, j) simply involves computation of its displacement from the beginning of the array that stores the matrix elements. For example, the displacement of the matrix element with the index (i, j) with respect to the beginning of the array is (j – 1) x N x 4 + (i – 1) x 4, for a matrix of size N x N.




Your user interface must provide at least the following functionalities,

<ol>

 <li>Ask the user the matrix size in terms of its dimensions (N),</li>

 <li>Allocate an array with proper size using syscall code 9,</li>

 <li>Ask user the matrix element to be accessed and display the content,</li>

 <li>Obtain summation of matrix elements row-major (row by row) summation,</li>

 <li>Obtain summation of matrix elements column-major (column by column) summation,</li>

 <li>Display desired elements of the matrix by specifying its row and column member</li>

</ol>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<ol start="2">

 <li><strong> [50 pts] Experiments with Data Cache Parameters</strong>Run your program with two reasonably large different matrix sizes that would provide meaningful observations. Modify your original program if needed. For large matrix initialization you may use a loop rather than user interface.</li>

</ol>




<strong>Report for Matrix Size 1: 25 Points</strong>



<strong>Report for Matrix Size 2: 25 Points</strong>




As described above make sure that you have an easy to follow presentation with numbered tables having proper heading etc.




Make sure that you find the summation of matrix elements by performing row-major and column-major addition. Note that the column-major addition is a simple array addition from the beginning to the end; however, the row-major addition is somewhat tricky.

<ol start="8">

 <li><strong>Direct Mapped Caches</strong>: For the matrix sizes you have chosen, conduct tests with various cache sizes and block sizes, to determine the hit rate, miss rate and number of misses. Use at least 5 different cache sizes and 5 different block sizes (make sure your values are reasonable) in order to obtain curves like those of Figure 8.18 (see below) in the textbook. Make a 5 x 5 table with your values, with miss rate and # of misses as the data at each row-column location.  Make the graph of miss rate versus block size, parameterized by cache size, like Figure 8.18 both for row-major and column-major additions.</li>

</ol>




Hint: You can reach the Cache Simulator from MARS/Tools/Data Cache Simulator as shown in the following image:




<ol>

 <li><strong>Fully Associative Caches</strong>: Pick 3 of your parameter points obtained in part for row-major addition a), one with good hit rate, one with medium hit rate, and one with poor hit rate. For these 3 results, there were 3 configuration pairs of cache size and block size that resulted in the data.  Take the same 3 configuration pairs, but this time run the simulation with a fully associate cache, using LRU replacement policy.  Compare the results obtained: The Direct Mapped good result versus the Fully Associative good result, the Direct Mapped medium result versus the Fully Associative medium result, and the Direct Mapped poor result versus the Fully Associative poor result. How much difference did the change to fully associative architecture make?  Now change the replacement policy to Random replacement, and run the 3 tests again (using the same 3 configuration pairs). Does replacement policy make a significant difference?  Record these 9 values in a new graph, with 3 lines: for Direct Mapped, for Fully Associative-LRU and for Fully Associative-Random. Note that this step is only for row-major addition so that by the end of the lab you’ll have (2+1)x2 = 6 graphs.</li>

 <li><strong>N-way Set Associative Caches</strong>: To save on hardware costs, fully set-associative caches are rarely used. Instead, most of the benefit can be obtained with an N-way set associative cache. Pick the medium hit rate configuration that you found in a) and used again in b), and change the architecture to N-way set associative. For several different set sizes (at least 4) and LRU replacement policy, run the program and record the hit rate, miss rate and number of misses. What set size gives the best result?  How much improvement is gained as N (the number of blocks in a set) increases each step?  Now repeat the tests, but for the good hit rate configuration from a) and b). Record these data and answer the same question again. Finally, repeat for the poor hit rate configuration.</li>

</ol>

<strong> </strong>

<strong>Oral Interview with TA and Submission of your Data</strong>

Get ready for the interview with your TA, by gathering and analyzing your data, having it ready to submit in a clean understandable format.  Be sure that you understand what you have done, and can interpret your data to the TA. Then call him/her over, and answer the questions he/she asks you.




<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>