# Phrase-Count-Map-Reduce-Program
Developed Phrase (Word Pair) Count MapReduce Program and executed the job in Docker and AWS EMR
## Synopsis
1. Developed a Phrase (Word Pair) Count MapReduce Program that counts word pairs taken sequentially in lines of text.
2. The default input key for the TextInput format is the line number. The required output is the count of word pairs.If the line contains a single word, then that becomes the word pair. 
NOTE: Punctuation will NOT count; so the words ‘(1991)’ and ‘1991’are the same. Therefore, the input file is initially parsed and all characters not in this set: [a-z, A-Z, 0-9] are removed; ‘the-cat’ and ‘the cat’ are counted as the same pair.
e.g. line:
Input:(k,v) = (1,“the cat in the hat is the best cat in the hat”)
Output:(k2,v2) = (“the cat”, 1), (“cat in”,2),(‘in the’,2),(‘the hat’,2’),(‘hat is’,1), etc
3. Input file used is adventures.txt in the input folder and the output file part-r-00000 containing the word pair count is present in the output folder.
4. The WordCountV2.jar contains the MapReduce program to get the output file part-r-00000 when the input file adventures.txt is provided.
## How to setup
The instructions for executing the Phrase Count MapReduce job in Docker and AWS EMR are provided in the following link:
[Hadoop_Job_Execution_Instruction](Hadoop_Job_Execution_Instruction.pdf)

