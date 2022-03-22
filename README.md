indent
======


**Library to detect and convert indentation in strings and files**, Tabs to spaces or vice versa.

⚡️ Installation
------------

Install via [composer](https://packagist.org/packages/tal7aouy/indent) or just clone the repo.

### Global installation

Install it globally using:

    composer global require tal7aouy/indent


✅  Usage
   ```sh
   ./indent
   ```
-----

    indent [--tabs|--spaces] [-r [--pattern=...]] [files or directories...]

    --tabs       convert all indentation to tabs. Assuming 4 spaces tab length.
    --spaces     convert all indentation to spaces.

    -r           recursively go over all directories given as argument and convert
                 files that match --pattern.

    --pattern    the pattern to match files for when using -r. Defaults to '*.php'.

    --tabstop=N  define number of spaces N to replace a tab with. Defaults to 4.

    --help       shows this usage information.

    If no file is specified input will be read from STDIN.

🚀 Examples
--------

Convert STDIN, which is the content of `index.php` to spaces and print the result to STDOUT:

    cat index.php | ./indent --spaces


Convert `index.php` to tabs:

    indent --tabs index.php

Convert all `.php`-files and the `LICENSE.md` in current dir to spaces:

    indent --spaces *.php LICENSE.md

Convert all `.php`-files in `dir` to tabs (recursively):

    indent --tabs -r dir

Convert all `.md`-files in dir to spaces (recursively):

    indent --spaces --pattern=*.md -r dir


**indent** was created by **[tal7aouy](https://github.com/tal7aouy)** under the **[MIT license](https://opensource.org/licenses/MIT)**.
