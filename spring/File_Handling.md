**File Handling in Java**

In Java, file handling means working with files like creating them, reading data, writing data or deleting them. It helps a program save and use information permanently on the computer.

**Why File Handling is Required?**
* To store data permanently instead of keeping it only in memory.
* To read and write data from/to files for later use.
* To share data between different programs or systems.
* To organize and manage large data efficiently.

**I/O Streams in Java**
In Java, I/O streams are the fundamental mechanism for handling input and output operations. They provide a uniform way to read data from various sources (files, network, memory) and write data to different destinations.

1. Byte Streams
In Java, Byte Streams are used to handle raw binary data such as images, audio files, videos or any non-text file. They work with data in the form of 8-bit bytes.

The two main abstract classes for byte streams are:

* InputStream: for reading data (input)
* OutputStream: for writing data (output)

Since abstract classes cannot be used directly, we use their implementation classes to perform actual I/O operations.

* FileInputStream: reads raw bytes from a file.
* FileOutputStream: writes raw bytes to a file.
* BufferedInputStream / BufferedOutputStream: use buffering for faster performance.
* ByteArrayInputStream: reads data from a byte array as if it were an input stream.
* ByteArrayOutputStream: writes data into a byte array, which grows automatically.

2. Character Streams
In Java, Character Streams are used to handle text data. They work with 16-bit Unicode characters, making them suitable for international text and language support.

The two main abstract classes for character streams are:

* Reader: Base class for all character-based input streams (reading).
* Writer: Base class for all character-based output streams (writing).

Since abstract classes cannot be used directly, we use their implementation classes to perform actual I/O operations.

* FileReader: reads characters from a file.
* FileWriter: writes characters to a file.
* BufferedReader: reads text efficiently using buffering; also provides readLine() for reading lines.
* BufferedWriter: writes text efficiently using buffering.
* StringReader: reads characters from a string.
* StringWriter: writes characters into a string buffer.

File Operations
The following are the several operations that can be performed on a file in Java:

1. Create a File
In order to create a file in Java, you can use the createNewFile() method.
If the file is successfully created, it will return a Boolean value true and false if the file already exists.

2. Write to a File
We use the FileWriter class along with its write() method in order to write some text to the file.

3. Read from a File
In Java, the read() method is used with classes like FileReader or InputStream to read data from a file one character or byte at a time.

* It returns an integer value representing the character or byte read.
* When the end of the file is reached, the method returns -1 indicating no more data is available.

4. canRead a File
canRead() check if the file is readable.

5. canWrite a File
canWrite() checks whether the file can be written to by the program.

6. Existance of a File
exists() checks whether the specified file or directory exists on the file system.

7. Getting a path
getAbsolutePath() returns the full path of the file or directory in the file system.

8. Delete a File
We use the delete() method in order to delete a file.

