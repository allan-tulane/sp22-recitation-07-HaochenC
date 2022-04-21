# CMPS 2200 Recitation 7
## Answers

**Name:**__Haochen Chen ______Zeyi Chen_________________


Place all written answers from `recitation-07.md` here for easier grading.



- **d.**

File | Fixed-Length Coding | Huffman Coding | Huffman vs. Fixed-Length
----------------------------------------------------------------------
f1.txt    |       1340            |       826         | 0.616418
alice29.txt    |       1039367              |       676374         | 0.650756
asyoulik.txt    |           876253          |       a606448         | 0.692092
grammar.lsp    |          26047           |        17356        | 0.666334
fields.c    |           78050          |       56206         | 0.720128

The huffman cost is about 0.666 of the size of the fixed-length cost.


- **e.**

Since each character has the same frequency, the huffman cost will be the sum of the length of the encodings times the frequency.
To be specific, suppose there is *n* characters in the document and each character has frequency *f*.
The problem becomes computing the expected sum of path lengths in a full binary tree wiht *n* leaves.
In what follows, we prove that the average height of a full binary tree with *n* leaves is larger than *log n*
Suppose that for n < N, the hypothesis holds, the consder a binary tree with N leaves.
Assume there is nl and nr leaves in the left subtree and right subtree of root seperately, then *d = nl/N + nr/N + 1 >= nl/N log nl + nr/N log nr + 1 >= log N*.
Thus, the expected huffman cost is *n log n f*.

