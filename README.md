# NPM

## setting npm
1. author environmental variables  
    ```
    $ npm set init.author.name "NAME"
    $ npm set init.author.email "E-mail"
    $ npm set init.author.url "URL"
    ```
2. add user  
 sign in at official site (https://npmjs.org/signup) or following command.
    ```
    $ npm adduser
    ```
3. login  
    ```
    $ npm login
    ```

## publish npm  
1. Create Project
    1. create repository in github   
    2. npm init  
    3. edit package.json  
        ```json
        {
            "name": "npm-study",
            ...
            - "main": "index.js", // module 
            + "bin": {  // cli tool
            +    "hello-npm": "bin/hello-npm" 
            + }
        }
        ```


2. Development & Test

3. Publish
    ```
    $ npm publish --access public
    ```

4. Check  
- cli application
    ```
    npm install -g @yocote/npm-study
    
    ```

5. Update
    ```
    $ npm version patch # 1.0.0 -> 1.0.1
    $ npm version minor # 1.0.0 -> 1.1.0
    $ npm version major # 1.0.0 -> 2.0.0

    ```
 
