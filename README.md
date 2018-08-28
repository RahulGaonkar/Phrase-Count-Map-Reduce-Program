# Phrase-Count-Map-Reduce-Program-and-Fundamentals-Of-Hadoop-Map-Reduce-Docker
Developed a Phrase (Word Pair) Count Map Reduce Program and performed certain exercises to showcase the fundamental knowledge of Hadoop,Map Reduce & Docker
## Synopsis
### Part 1
1. Developed a Phrase (Word Pair) Count Map Reduce Program that counts word pairs taken sequentially in lines of text.
2. The default input key for the TextInput format is the line number. The required output is the count of word pairs.If the line contains a single word, then that becomes the word pair. 
NOTE: Punctuation will NOT count; so the words ‘(1991)’ and ‘1991’are the same. Therefore, the input file is initially parsed and all characters not in this set: [a-z, A-Z, 0-9] are removed; ‘the-cat’ and ‘the cat’ are counted as the same pair.
e.g. line:
Input:(k,v) = (1,“the cat in the hat is the best cat in the hat”)
Output:(k2,v2) = (“the cat”, 1), (“cat in”,2),(‘in the’,2),(‘the hat’,2’),(‘hat is’,1), etc
3. Input file used is adventures.txt in the input folder and the output file part-r-00000 containing the word pair count of the input file adventures.txt is present in the output folder.    
### Part 2
