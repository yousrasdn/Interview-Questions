# IO Interview Questions

## Overview Questions

### What is an IO stream?

It is a flow of data that we can read from or write to.

### What are types of IO streams?

- Character streams
- Byte streams

### What are classes available for the different stream?

- For Character streams: java.io.Reader and java.io.Writer
    
- For Byte streams: java.io.InputStream and java.io.OutputStream


## Writers Questions

### Waht are the different writers available for Character streams?
    1- FileWriter
    2- BufferedWriter
    3- PrintWriter
    
### Whats the difference between FileWriter and BufferedWriter?

BufferedWriter cannot communicate with File directly. We have to use a writer with it.

### ... And PrintWriter?

PrintWriter can communicate directly to file and also via a writer.

### Why we have to use flush and close?

flush() is used to clear all the data charactrs stored in the buffer and clear the buffer.
It flushes the stream (thus we are certain that the data has properly written to the file).

close() is used to close the character stream and releases the system resources associated with
the strea,

** flush() is applicable for all the writers.
   close() is applicable for both the writers and readers.

   
## Readers Questions

### What are the different types of readers?
    1- FileReader
    2- BufferedReader

### What's the difference between FileReader and BufferedReader?

FileReader reads data from a file character by character.
BufferedReader reads data either character by character, or line by line.

BufferedReader is most effecient reader because it buffers the input from the specefied file.

-> it reads large chuncks of data from a file at once and keep this data in a buffer. When we ask for the next
character or line of data, it gets it from that buffer.

## Writer / Reader hierarchy

### Present the Writer / Reader hierarchy

                                                                    
            
                        InputStreamReader  -> FileReader
            Reader -> 
                        BufferedReader

object -> 

            
                        OutputStreamWriter -> FileWriter
            Writer ->   BufferedWriter
                        PrintWriter
                        
## Stream vs ReaderWriters

### When to use ByteStreams?

Byte streams process data byte by byte. So byte stream is suitable for processing binary files.
                        
### When to use FileInputStream/FileOutputStream and FileReader/FileWriter?

Both FileInputStream/FileOutputStream and FileReader/FileWriter are used to read/write data from a source 
(either file or socket).

FileInputStream/FileOutputStream are used to read/write binary data, 
while FileReader/FileWriter are used to read text data (unicode characters).















