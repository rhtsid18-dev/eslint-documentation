# ESLINT DOCUMENTATION

## Tutorial Reference : <https://www.youtube.com/playlist?list=PL_euSNU_eLbeVd_eDmWzUpEmXizWQRmEm>

## What is ESLint and why to use it: -

- ES stands for ecma-script and linting is the process of identifying the standard problems in your code.
- ESLint is a library that is used for Javascript and is essentially a javascript linter.
- Since Javascript is a dynamically typed language and has various ways to write the same functionality because of the different versions of the code like ES5 and ES6, it has a lot of freedom in the way you can write code.
- This makes the code more vulnerable to basic errors from the developer.
- This is where ESLint comes in using which we can standardize some syntax rules in the project which every developer working on the project has to follow.
- The main goal or usecase of this tool is to make the code more consistent and avoid bugs.
- Example usecase: -

```javascript
function checkPositive(number)
{
    var x = 3;
    if (number > 0) {
        return true;
    }
}

checkPositive(3);
```

- Following are some of the problems with the above showcased example: -
    - The function returns true only when the number is positive
    - Variable x is defined but not used in code.
    - The code works fine but will throw errors in edge case.

- These ^ issues can automatically be handled by ESLint if it is confirgured to address these issues.
- We can and should run ESLint as part of our CI ( Continous Integration ) Pipeline.

## How to install and use ESLint in your Javascript project: -

- Prerequisite : Node > V10
- ESLint can be installed in two ways: -
    - Globally using the -g flag. ( Not recommended as not all projects have the same linting requirements )
    - locally within the project with the --save-dev flag. ( The recommended approach to more precicesly define the linting rules in your project/workspace )
- In case of local install ( with --save-dev flag ), we can run eslint by going to the directory `./node_modules/.bin/eslint --help`
- If you don't have your package.json initialized then before the ^ step, we would have to run `npm init`.
- After that we can install eslint locally on the project using the command : `npm install --save-dev eslint`
- Before we can run eslint on our project, we need to setup an eslint configuration file which we can initialize with `./node_modules/.bin/eslint --init`.

- When you run the `eslint --init` you will get the following options to choose from: -
    - <img src="images/eslint_init_screenshot_1.png" height="200" />
- For the purpose of this document, I have chosen `To check syntax, find problems, and enforce code style`.
- After that there will be some self explanatory questions that you can answer easily based on your project's requirements.

### WHERE I AM AT IN THE TUTORIAL RIGHT NOW : -

Completed the 2nd video in the playlist. Need to start from video 3 tomorrow.
