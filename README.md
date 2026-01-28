# hazbrow
Welcome to Hazbrow!

Read this readme file to get acquainted with Hazbrow!

## How to use Hazbrow
###### Hazbrow is in early development so expect terminal use
###### also expect erratic behaviour during errors ie "url not existing" ect...
## This Guide expects you to be on linux (specifically a Debian based distro with apt ) if you're on windows use WSL
First run this:
```shell
sudo ./install.sh
```
And you're done! If you want to run hazbrow open up a terminal and run this:
```shell
hazbrow
```

## How to make sites for Hazbrow
Hazbrow uses the Yeep-PLUS-PLUS programming language for sites. (see the yeep plus plus github page [here](https://github.com/JohnDoggoLover/YEEP-plus-plus))
## new keywords
For hazbrow Yeep-PLUS-PLUS gains three new keywords:
### obj
obj has three operands
#### Operand 1, string
Operand 1 is a string, it is the type of the object.
currently there is only one object type which is "text".
#### Operand 2, string
Operand 2 is a string, it is the identifier for the object.
As of now you cannot change / manipulate objects but this is important for future-proofing.
#### Operand 3, string
Operand 3 is the additional operand. it is a string.
What it does changes with the type of object but for now text is the only type.
For text Operand 3 is the contents of the text object.
### hazbrow
Arguably the most important tag, hazbrow has to be the first thing in the file,
the reason you need it is to tell hazbrow that this site is supported.
### flip
Flip displays all of the text to the screen I recomend to put right before the halt loop.
## site components
A site only needs two components a root directory and a index.ypp file.
```shell
.
└── index.ypp

1 directory, 1 file
```
An index.ypp file only needs two things to be considered a site.
A hazbrow tag as the first thing in the file.
And a halt loop at the end of the file.
A bare minimum index.ypp file looks like this:
```python
hazbrow
halt:
jmp "halt"
EOF
```
Here is a template for a basic hazbrow site:
```python
hazbrow
obj "text" "text1" "Hello everybody welcome to my site!\n"
flip
halt:
jmp "halt"
EOF
```