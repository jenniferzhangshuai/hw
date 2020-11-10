# The word-counting application takes as input one or more text files and produces a list of words and their frequencies as output.
Because Hadoop utilizes key/value pairs—the input key is a file ID and line number and the input value is a string, while the output key is a word and the output value is an integer. 
First, each mapper can work on a single document; or if the documents are very large, mappers can work on chunks of single documents—the map operation doesn’t care about the context of the words, just that it can count the words it is given as input.
 Similarly, we can have multiple reducers working on different keys simultaneously because the output key is a word. The Python pseudocode shows how this algorithm:
 
©
