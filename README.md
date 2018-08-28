# Phrase-Count-Map-Reduce-Program
Developed a Phrase (Word Pair) Count Map Reduce Program
## Synopsis
1. Developed a Phrase (Word Pair) Count Map Reduce Program that counts word pairs taken sequentially in lines of text.
2. The default input key for the TextInput format is the line number. The required output is the count of word pairs.If the line contains a single word, then that becomes the word pair. 
NOTE: Punctuation will NOT count; so the words ‘(1991)’ and ‘1991’are the same. Therefore, the input file is initially parsed and all characters not in this set: [a-z, A-Z, 0-9] are removed; ‘the-cat’ and ‘the cat’ are counted as the same pair.
e.g. line:
Input:(k,v) = (1,“the cat in the hat is the best cat in the hat”)
Output:(k2,v2) = (“the cat”, 1), (“cat in”,2),(‘in the’,2),(‘the hat’,2’),(‘hat is’,1), etc
3. Input file used is adventures.txt in the input folder and the output file part-r-00000 containing the word pair count is present in the output folder.
4. The WordCountV2.jar contains the map reduce program which is run in the hadoop container in docker to get the output file part-r-00000 when the input file adventures.txt is provided.
5. Technology,Library & Software Tool Used : Java, Docker, Hadoop, Map Reduce
## How to setup
1. Place the WordCountV2.jar file in the hadoop container in Docker.
2. Place the adventures.txt file in the HDFS. I had placed it in user/cloudera/adventures.txt
3. Then run the job by executing the command hadoop jar WordCountV2.jar /user/cloudera/adventures.txt /user/cloudera/output
4. The output path argument should be a unique path, or it will throw an exception. I have mentioned /user/cloudera/output             where I will get the output file generated.
