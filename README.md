1. get & install Sublime 
-> http://www.sublimetext.com/2

2. Support CoffeeScript
to support syntax highlighting, navigate to "C:\Users\[USER]\AppData\Roaming\Sublime Text 2\Packages",
add the folder "CoffeeScript" and add the following file to the new folder:
https://github.com/jashkenas/coffee-script-tmbundle/blob/master/Syntaxes/CoffeeScript.tmLanguage


3. get & install node 
-> http://nodejs.org/#download

4. restart computer 
(path variable needs to be updated)

5. get & install json and finally CoffeeScript
open console (cmd) and type:
npm install json
npm install -g coffee-script
(folder will be here: C:\Users\[USER]\AppData\Roaming\npm\node_modules\coffee-script)

6. Create build systen in Sublime (so u can compile with strg+b)
Open Sublime an navigate to:
Tools -> Build-System -> New Build System... 
insert:
{

  "shell" : true,
  "cmd": ["coffee","-c","$file"],
  "file_regex": "^(...*?):([0-9]*):?([0-9]*)",
  "selector": "source.coffee"

}
and save as "Coffee-Script.sublime-build"
(will be saved here: C:\Users\[USER]\AppData\Roaming\Sublime Text 2\Packages\User)


restart sublime


have fun!


also u can have a look here:
http://kevinpelgrims.wordpress.com/2011/12/28/building-coffeescript-with-sublime-on-windows/
http://wesbos.com/sublime-text-build-scripts/
