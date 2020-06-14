# NPM

## References
 Official: 
 > Root: https://docs.npmjs.com/  
 > CLI: https://docs.npmjs.com/files/package.json#bin  
 
 Articles: 
 > CLI: https://developer.okta.com/blog/2019/06/18/command-line-app-with-nodejs  
 

## setting npm
1. Set environmental variables  
    ```
    $ npm set init.author.name "NAME"
    $ npm set init.author.email "E-mail"
    $ npm set init.author.url "URL"
    $ npm set init.license "ISC"
    ```
2. Add user  
 sign in at official site (https://npmjs.org/signup) or following command.
    ```
    $ npm adduser
    ```
3. Login  
    ```
    $ npm login
    $ npm whoami
    ```

## publish & install npm  
1. Create Project
    1. create repository in github   
    2. npm init  
    ```
        npm init # --scope=@yocote
    ```
    3. edit package.json  
        ```json
        {
            "name": "npm-study",
            ...
            - "main": "index.js", // module 
            + "bin": {  // cli tool
            +    "hello-npm.js": "./bin/hello-npm.js" 
            + }
        }
        ```


2. Development & Test

3. Publish
    ```
    $ npm publish --access public
    ```

4. Check  
- install local library
    ```
    $ npm install .
    $ # npm instal -g . # cli
    ```
- install published library
    ```
    $ npm install @yocote/npm-study
    $ # npm instal -g @yocote/npm-study # cli
    ```
- fix
    ```
    # npm list -g --depth 0
    # npm uninstall -g @yocote/npm-study
    ```

5. Update
    ```
    $ npm version patch # 1.0.0 -> 1.0.1
    $  # npm version minor # 1.0.0 -> 1.1.0
    $  # npm version major # 1.0.0 -> 2.0.0
    $ npm publish --access public
    $ npm unpublish @yocote/hello-world-cli@1.0.1
    ```
 
