0x01. ES6 Promises
JavaScript
ES6
 Weight: 1
 Project will start Jun 25, 2024 6:00 AM, must end by Jun 27, 2024 6:00 AM
 Checker was released at Jun 25, 2024 6:00 PM
 An auto review will be launched at the deadline


Resources
Read or watch:

Promise
JavaScript Promise: An introduction
Await
Async
Throw / Try
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

Promises (how, why, and what)
How to use the then, resolve, catch methods
How to use every method of the Promise object
Throw / Try
The await operator
How to use an async function
Requirements
All your files will be executed on Ubuntu 18.04 LTS using NodeJS 12.11.x
Allowed editors: vi, vim, emacs, Visual Studio Code
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the js extension
Your code will be tested using Jest and the command npm run test
Your code will be verified against lint using ESLint
All of your functions must be exported
Setup
Install NodeJS 12.11.x
(in your home directory):

curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
$ nodejs -v
v12.11.1
$ npm -v
6.11.3
Install Jest, Babel, and ESLint
in your project directory, install Jest, Babel and ESList by using the supplied package.json and run npm install.

Configuration Files
Add the files below to your project directory

package.json
Click to show/hide file contents
babel.config.js
Click to show/hide file contents
utils.js
Use when you get to tasks requiring uploadPhoto and createUser.

Click to show/hide file contents

export function uploadPhoto() {
  return Promise.resolve({
    status: 200,
    body: 'photo-profile-1',
  });
}


export function createUser() {
  return Promise.resolve({
    firstName: 'Guillaume',
    lastName: 'Salva',
  });
}


.eslintrc.js
Click to show/hide file contents
and…
Don’t forget to run $ npm install when you have the package.json

Response Data Format
uploadPhoto returns a response with the format

{
  status: 200,
  body: 'photo-profile-1',
}
createUser returns a response with the format

{
  firstName: 'Guillaume',
  lastName: 'Salva',
}
Tasks
0. Keep every promise you make and only make promises you can keep
mandatory
Return a Promise using this prototype function getResponseFromAPI()

bob@dylan:~$ cat 0-main.js
import getResponseFromAPI from "./0-promise.js";

const response = getResponseFromAPI();
console.log(response instanceof Promise);

bob@dylan:~$ 
bob@dylan:~$ npm run dev 0-main.js 
true
bob@dylan:~$ 
Repo:

GitHub repository: alx-backend-javascript
Directory: 0x01-ES6_promise
File: 0-promise.js
  
1. Don't make a promise...if you know you can't keep it
mandatory
Using the prototype below, return a promise. The parameter is a boolean.

getFullResponseFromAPI(success)
When the argument is:


