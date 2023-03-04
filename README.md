# File Compressor
This is a simple Rust command-line tool that compresses a file using gzip compression.

## Usage
```shell
$ cargo run source_file target_file
```
The source_file is the file that needs to be compressed and target_file is the name of the compressed file that will be created.


### Example
```shell
$ cargo run example.txt example.txt.gz
```
This will compress the example.txt file and create a compressed file named example.txt.gz.

## Installation
You can compile and install this tool using Rust's Cargo package manager:

```shell
$ git clone https://github.com/your_username/file-compressor.git
$ cd file-compressor
$ cargo build --release
$ cargo install --path .
```

## How it works
- The program takes two arguments from the command line - source and target. 
- If the number of arguments is not equal to 2, it will display a usage message and terminate. 
- The input file is read using a BufReader and compressed using the GzEncoder from the flate2 library. 
- The compressed data is then written to the output file using a File writer. 
- Finally, the metadata of the source and target files and the elapsed time are printed to the console.

## License
This project is licensed under the MIT License.
