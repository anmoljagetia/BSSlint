# BSSlint

Derived from the popular CPPLint from Google, but modified to incorporate code styles by Dr. B.S. Sanjeev for my undergraduate Data Structures and Algorithms courses.

We've all written terrible code, and using proper indentation and code styling is the first step one has to take to improve the quality of code. Linter is a helper, that helps in identifying common style related errors in code.

![BSSLint](https://raw.githubusercontent.com/anmoljagetia/BSSlint/master/Resources/standard.jpg)

The style guidelines this tries to follow are based on [Google's Style Guide](https://google.github.io/styleguide/cppguide.html), however they have since then been modified to incorporate the styles suggest for my course.

 Every problem is given a confidence score from 1-5, with 5 meaning the certainty of the problem, and 1 meaning it could be a legitimate construct. This will miss some errors, and is not a substitute for a code review.

## Installation

### Method 1 (Recommended)

`bsslint` can be installed using both `pip` and `easy_install` globally by running the commands :

```
sudo pip install bsslint
```

or

```
sudo easy_install bsslint
```

### Method 2 (Do It Yourself)
The script can also be directly used by downloading the binary into the folder of execution by running the command :

```
wget -O bsslint http://git.io/vuUVj && chmod +x bsslint
```
Once the executable file is in the desired folder, any code can be evaluated using :

```
./bsslint [FILENAME]
```

## Usage
If you have installed `bsslint` globally, and if it is available in your `$PATH`, a simple command can be used :

```
bsslint [FILENAME]
```

Another cool way of using `bsslint` is to use add the following mapping in `vimrc` to add a key (like F8), to run the lint when desired :

```
autocmd filetype cpp nnoremap<F8> :!bsslint % <CR>
autocmd filetype c nnoremap<F8> :!bsslint % <CR>
```
For similar tools to compile and evaluate results like IDE from within vim, check out my [vimrc](https://github.com/anmoljagetia/dotfiles/blob/master/vim/vimrc#L86-L90) and other [dotfiles](https://github.com/anmoljagetia/dotfiles).

## Full Disclaimer

This is a very old code, that I had lost, and then recovered one day. It is not perfect, however it was extremely helpful to me during the evaluations. I have tried cleaning it up a little.

Contributions are welcome.

## Known Errors

* All variables used in any function are to be declared at the start of the same. This file does not detect this requirement.


## License

[MIT](http://anmoljagetia.mit-license.org/)
