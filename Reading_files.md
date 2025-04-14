## Note: use the with open() to ensure that file is properly closed after reading or writing, which is good practice in file handling

# Open file in read mode
with open('file.txt', 'r') as f: # Opens file.txt in read mode, stores it into 'f' object 
    content = f.read()  # Reads entire file content into "content" object 
    print(content)

# Read specific number of bytes
with open('file.txt', 'r') as f:
    first_five_chars = f.read(5)  # Reads first 5 characters 
    print(first_five_chars)

# Open file in append mode
with open('file.txt', 'a') as f: 
    f.write('\nThis line is appended.') # i.e. adds a new line with this text at the end of the file without modifying the existing content 

# Open file in write mode (creates file if it doesn't exist)
with open('file.txt', 'w') as f:
    f.write('Hello, World!\n')
    f.write('Writing more text.') #writes these texts to the file. If the file does not exist, will create a new file. If the file exists, write() will overwrite it 

## Multiple modes 
# Open file in read and write mode
with open('file.txt', 'r+') as f:
    content = f.read()  # Read existing content
    f.write('\nThis is new content.')  # Write new content

# Append to the file
with open('file.txt', 'a') as f:
    f.write('\nAppending more text.')

# Read the file to see changes
with open('file.txt', 'r') as f:
    content = f.read()
    print(content)


Summary of Modes:
Mode	Description
'r'	Open for reading (default). File must exist.
'w'	Open for writing. Truncates the file or creates it.
'a'	Open for appending. Data is written at the end of the file.
'r+'	Open for reading and writing. File must exist.
'w+'	Open for reading and writing. Truncates the file.
'a+'	Open for reading and appending. Data is added at the end.

