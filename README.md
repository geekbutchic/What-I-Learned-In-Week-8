# What-I-Learned-In-Week-8
* ## Application Building 
* ## How it begins?
* ## How does the data flow?
* ## What are some key things to note?

## Application Building

* How it begins:
  
* Back-end - is where we keep our functions and depending on the user input will result in grabbing that function or not.
* Back-end often times is in a different file from the front-end.
* For example for the current application we are working on, we are using *main.js* as our front-end file and *translate-word.js* has our back-end/function file.
* So how does this all work?
* For this application this user is typing in a word and we are giving them an emoji.
* User types in *node main.js* which is at indices 0 and 1.
* After typing in *node main.js* the user will type in a word.  Let's say octopus and wants to return an emoji symbol.

![Alt Text](https://www.valuecoders.com/blog/wp-content/uploads/2018/02/front-end-development-tools-1024x512.png)

## How does data flow?

* User inputs from the terminal *node main.js octopus*.
* *const userInput = process.argv[2]* is what grabs the value at index 2, which is octopus being held in userInput.
* It therefore is passed to our back-end function that is in a separate file.
  
* The function in that file is verifying if that word is an object in that array and holds an emoji value.
* The value is returned to us and held in the name of our function and exported by *module.exports* back to our front-end.
* The return value goes into results and is printed out by using console.log.

## What are some key things to note?
* Case sensitivity is very important.  Even if the user types in Octopus, OcToPus, octopus, we are able to still return a value due to *.toLowerCase()*.  This allows the user a better experience in that they don't have to be exact.

* What if they type in multiple words and want to check those words emoji value.

* We can manipulate the front-end by using *.slice(2)* - this allows us to make an array of the words after *index[2]*.
* We then can check their value and use *.join(' ')*, adding a space in between.
* *.slice()* creates an array of the words from the user input.
* The words can then be put through our function returning a value if it matches.
* *.join(' ')* brings those words back together with a space.

![Alt Text](https://image.slidesharecdn.com/javascriptatbackend-nodejs-150612075014-lva1-app6891/95/java-script-at-backend-nodejs-12-638.jpg?cb=1434095469)

