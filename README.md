# Sublime Text Monokai C# theme for Visual Studio Code
[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)

This theme is exactly the same Monokai's theme of Sublime Text but for Visual Studio Code instead. Unlike default VSCode's Monokai, this is an actual, perfect and identical copy of the loved by all Sublime Text's theme. It's name is **Sublime Monokai**.

   - [Visual Studio Marketplace: Theme&Colorizer Extension](https://marketplace.visualstudio.com/items?itemName=maximetinu.identical-sublime-monokai-csharp-theme-colorizer)
## Screenshots
![Sublime monokai theme demo](/screenshots/sublime-monokai-demo.png?raw=true "Sublime monokai theme demo")
### Comparison between this theme and Sublime Text's
![This theme vs Sublime Text's](/screenshots/sublime-monokai-vs-sublime-text.png?raw=true "This theme vs Sublime Text's")
### Comparison between default VSCode Monokai theme and Sublime Text's
Observe the differences. Is subtle but it's there.
![Default VSCode Monokai vs Sublime Text's](/screenshots/default-monokai-vs-sublime-text.png?raw=true "Default VSCode Monokai vs Sublime Text's")
## Instructions
Option 1, search for the extension in Visual Studio Code Marketplace:
1. At the Welcome tab *(Help>Welcome)* click "Tools and languages" and search by my "identical sublime monokai theme". Install it.
2. Ready to code!

Option 2, install it as a local VSCode extension:
1. Copy the folders in this repository *csharp-sublime-colorizer* and *theme-sublime-monokai* into your folder *<User Home>/.vscode/extensions/*.
2. Ready to code!
   
Make sure that you choose the **Sublime Monokai** color theme at the Welcome tab *(Help>Welcome)* and check bottom right if **C# Sublime Colorizer** is working instead of the default C#, as can be seen in the next screenshot:
![Sublime colorizer working](/screenshots/sublime-colorizer-working.png?raw=true "Sublime colorizer working")

**Why override C# parser/colorizer if it's a theme? Keep reading.**

---

## Why default VSCode's Monokai is so different from Sublime Text's?
There are two reasons.

First of all, VSCode's theme assign the same style to certains colorizer rules which differ each other in Sublime Text. It's possible to solve it by modifying the default VSCode Monokai's theme.

Secondly, no matter how much we modify default VSCode's Monokai, it's impossible to get the same color scheme as Sublime Text due to limitations of the C# colorizer that uses VSCode. On the one hand, VSCode groups in the same selector two things which are different styled in Sublime Text, and it is not possible to assign different styles to things with the same selector. On the other hand, the VSCode C# colorizer is more limited due to it is only possible to assign one single selector to each code token, unlike Sublime Text's colorizer, which allows the assignment of multiple selectors to increase flexibility when it comes to styling. This is because VSCode uses a *.tmLanguage* file as colorizer while Sublime Text uses *.sublime-syntax* files to make the parsing. It is possible to convert from *.tmLanguage* to *.sublime-syntax*, but not the opposite, since *.sublime-syntax* is a superset of *.tmLanguage* functionality, so it is not possible to convert in such a way.

In the next screenshot can be seen the gap between the two colorizers:
![tmlanguage vs sublime syntax](/screenshots/tmlanguage-vs-sublimesyntax.png?raw=true "tmlanguage vs sublime syntax")
### So, what's the trick, then?
I've modified the VSCode C# colorizer (the *.tmLanguage* file) to differentiate differents elements. Once that's done, I've modified the default VSCode's Monokai theme to assign the styles as Sublime Text does. That's why it's necessary to modify the official C# parser folder.

**Happy coding!** now with Monokai ;)

---

**UNLICENSED** 

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)

   - Only tested in Windows 10, but it should also work in MacOS and Linux.
   - Only tested with C#, but it should also work for other programming languages. It should be more like Sublime's Monokai working with any language, but it won't be as accurate as with C# since the only colorizer modified is the C# parser.
   - Only tested with Visual Studio Code, but it should also work with Visual Studio IDE as long as the *.tmLanguage* file (the colorizer) is modified or replaced and the theme is installed too.
   
In general, it should also work in any editor which uses the same Text Mate grammar tokens as theme and the *.tmLanguage* as colorizer, as Text Mate editor itself.
