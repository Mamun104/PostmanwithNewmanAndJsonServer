# Automated Api Testing Using Postman, Newman And Json-Server

## Technology and Tool Used
- Postman
- Node Js
- newman
- Json-Server

## Prerequisites

- You must have installed node js to your system
- Postman
- NPM
- Newman
- Json-Server

## Scenario of this project

- The user can create a post
- The user can single and multiple post by post id
- The user can get all post 
- The user can update single post
- The user can update multiple post
- The user can delete a post

## API Documents

      https://documenter.getpostman.com/view/16548351/2s93eVWYqH 


## How to run this project

- clone this project
- hit following commands

              npm i newman
              npx newman run
 
 
## How To HTML Report Generate Using Newman

- Step-1
             npm i newman-reporter-htmlextra

- Step-2 
- Now create another file named report.js
- copy paste following code:

          const newman = require('newman');
          newman.run({
          collection: require('./collection/customer_api_collection.json'), // pointing to local JSON file.
          environment: require('./collection/customer_api_env.json'), // pointing to local env file
          iterationCount: 1,
          reporters: 'htmlextra',
          reporter: {
          htmlextra: {
         export: './Reports/report.html', // If not specified, the file will be written to `newman/` in the current working directory.
        }
       }
       }, function (err) {
       if (err) { throw err; }
       console.log('collection run complete!');
       });


- Now create a folder named Reports. If you do not create this folder, the report will be generate to a new folder named ‘newman’ in current working directory.

- Then go to the package file and update “test” value under scripts as: “node report.js”

- Now hit this command:

             npm test
 
 ## What is Json-Server
 
 
          json-server is an npm(Node Package Manager) module, used for creating a mock REST API effortlessly. 
          Data is transferred in JSON(JavaScript Object Notation) format between client and server.
 
 ## How To install Json-Server
 
                  npm install json-server
                  
 -Check the json-server version
 
                 json-server --version
 
 ### Output: 
 
 
 ![j1](https://user-images.githubusercontent.com/78067017/235963646-486c915a-403b-4a59-a156-dc5c86d63950.png)
![j2](https://user-images.githubusercontent.com/78067017/235963662-1a1816c7-f784-4dfe-91db-c7e9e615bb9f.png)









