# WinLess.lessc
Package for easy compiling of LESS files in your build events.
Contains Node package of less.js.

## Usage
WinLess.lessc comes with 2 commands: lessc and lesscFolder.
Syntax:
  lessc "<lessFile>" "<cssFile>" <otherArguments>
	lesscFolder "<lessFolder>" "<cssFolder>" "otherArguments"
Note: the aditional lessc arguments passed to lesscFolder need to be quoted.
The most noteworthy argument is '--yui-compress', which minifies the outputted css.

## Examples
### Compiling a folder
	CD "$(SolutionDir)packages\WinLess.lessc*\tools"
	CALL lesscFolder "$(ProjectDir)Styles" "$(ProjectDir)Styles" "--yui-compress"

### Compiling a single file
	CD "$(SolutionDir)packages\WinLess.lessc*\tools"
	CALL lessc "$(ProjectDir)Styles\Less\main.less" "$(ProjectDir)Styles\Css\main.css" --yui-compress
	
## Updating less.js
1) Install Node with Node Package Manager: http://nodejs.org/download/
2) Open Command Prompt and cd to the 'packages\WinLess.lessc' folder
3) Execute the following command:
	npm update less
		
## Credits
less.js:
	Official LESS compiler
	Author: Alexis Sellier
	Website: http://lesscss.org/
	
node.js:
	Node.js
	Website: http://nodejs.org/

lesscFolder.cmd
	Simple script which allows you to compile all LESS files in a folder with one command.
	Author: Mark Lagendijk
	Website: http://winless.org
