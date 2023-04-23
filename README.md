# Data Structures and Algorithms

## What are we doing in this repository ? 
- Wer're learning Data Structures and Algorithms with example problems in Python.
- We're solving complex coding interview questions from (Apple , Tesle , Google, etc.)
### Okay but what is Data Structures and Algorithms ?
- A data structure is a named location that can be used to store and organize data. And, an algorithm is a collection of steps to solve a particular problem.

# Let's Start ! 

### What is Big O Notation ? 
- Big O Notation is a tool used to describe the time complexity of algorithms.
- It calculates the time taken to run an algorithm as the input grows.
- Big O Notation in Data Structure describes the upper bound of an algorithm's runtime.

In other words , Big O Notation calculates the worst scenario of  an algorithm's time  complexity .

<p align="leading">
  <img src= "https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png" >
</p>

### What is Boyer Moore Algorithm ? 
  <p>Boyer Moore algorithm starts matching from the last character of the pattern.The Boyer–Moore algorithm searches for occurrences of P in T by performing explicit character comparisons at different alignments. Instead of a brute-force search of all alignments (of which there are n - m + 1 ), Boyer–Moore uses information gained by preprocessing P to skip as many alignments as possible. 
  <br/>
   A shift is calculated by applying two rules: the bad character rule and the good suffix rule. The actual shifting offset is the maximum of the shifts calculated by these rules.
   </p>
   
#### The Bad Character Rule
  The bad-character rule considers the character in T at which the comparison process failed (assuming such a failure occurred). The next occurrence of that character to the left in P is found, and a shift which brings that occurrence in line with the mismatched occurrence in T is proposed. If the mismatched character does not occur to the left in P, a shift is proposed that moves the entirety of P past the point of mismatch.
  
#### The Good Suffix Rule

  The good suffix rule is markedly more complex in both concept and implementation than the bad character rule. Like the bad character rule, it also exploits the algorithm's feature of comparisons beginning at the end of the pattern and proceeding towards the pattern's start.Suppose for a given alignment of P and T, a substring t of T matches a suffix of P, but a mismatch occurs at the next comparison to the left.
  
  1. Then find, if it exists, the right-most copy t' of t in P such that t' is not a suffix of P and the character to the left of t' in P differs from the character to the left of t in P. Shift P to the right so that substring t' in P aligns with substring t in T.
  2. If t' does not exist, then shift the left end of P past the left end of t in T by the least amount so that a prefix of the shifted pattern matches a suffix of t in T.
  3. If no such shift is possible, then shift P by m (length of P) places to the right.
  4. If an occurrence of P is found, then shift P by the least amount so that a proper prefix of the shifted P matches a suffix of the occurrence of P in T.
  5. If no such shift is possible, then shift P by m places, that is, shift P past t.

   
