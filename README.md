# MiniGrep

MiniGrep is a simple command-line tool written in Rust that allows you to search for a specific query string in a given
text file. It provides both case-sensitive and case-insensitive search options.

## Usage

To use MiniGrep, follow these steps:

### 1. Clone the repository:

```shell
git clone https://github.com/andersonmarin/minigrep
```

### 2. Build the project:

```shell
cargo build
```

### 3. Run MiniGrep with the desired search parameters:

```shell
cargo run -- <query> <file_path>
```

Replace `<query>` with the text you want to search for and `<file_path>` with the path to the text file you want to
search in.

## Unit Tests

You can run the unit tests for MiniGrep using the following command:

```shell
cargo test
```

This will execute the test cases defined in the `tests` module of the code, ensuring the correctness of the search
functions and other components.

## Environment Variable

By default, the search is case-sensitive. However, you can enable case-insensitive search by setting the `IGNORE_CASE`
environment variable:

```shell
export IGNORE_CASE=1
```

## Examples

### Case-Sensitive Search

To perform a case-sensitive search for the query "duct" in the following content:

```shell
Rust:
safe, fast, productive.
Pick three.
```

Run the following command:

```shell
cargo run -- duct path/to/file.txt
```

You should see the output:

```text
safe, fast, productive.
```

### Case-Insensitive Search

To perform a case-insensitive search for the query "rUsT" in the following content:

```shell
Rust:
safe, fast, productive.
Pick three.
Trust me.
```

Run the following command:

```shell
export IGNORE_CASE=1
cargo run -- rUsT path/to/file.txt
```

You should see the output:

```text
Rust:
Trust me.
```

## Disclaimer

This repository and its contents are intended for educational and study purposes only. The code and documentation
provided are not intended for production use. Use at your own risk.