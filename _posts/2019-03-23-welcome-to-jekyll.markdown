---
layout: post
title:  "Testing react component with Jest and Enzyme"
date:   2019-07-23 21:03:36 +0530
categories: Jest Enzyme
---


In today&#39;s fast-growing world of the Internet, users want products to be implemented faster. Users want more software releases with new features to be implemented in a short time frame, but they don&#39;t like to work with defected software. Testing the product is as important as developing it because

-  The quality of the product is most important.
-  A small bug in a product can create huge complications.

In the software development life cycle (SDLC) testing plays an important role, which helps to improve the quality, reliability &amp; performance of the system. Testing also check what all functions application supposed to do &amp; also check that is not supposed to do. We can take simple examples to clear why testing is important,

1. In the Application of Banking, if balance is shown zero instead of thousand because of a bug.
2. Booking a movie ticket is not working in application due to a bug.
3. The wrong percentage of a student is getting calculated because of a bug in university application.

If you have a basic understanding of React and want to know how to test your react component using jest and enzyme this will be helpful to you.

So, let&#39;s get started,

-  Jest is a delightful JavaScript Testing Framework with a focus on simplicity.
- It works with projects using: Babel, TypeScript, Node, React, Angular, Vue and more!
- The enzyme is a JavaScript Testing utility for React that makes it easier to traverse your React components output.
- Both Jest and Enzyme are specifically designed to test React applications, Jest can be used with any other JavaScript app, but Enzyme only works with React.
- Jest is an assertion library, and Enzyme is to provide additional testing utilities to interact with elements.

**Installing Jest to your PC**

- npm install jest
- npm install enzyme

Now we can start implementing test cases for component,

I contributed to develop some react reusable component&#39;s you can see them here [https://www.npmjs.com/package/eternus-react-component](https://www.npmjs.com/package/eternus-react-component) I am going to write test cases for login component which looks like,


 ![](/jest-enzyme.github.io/assets/LoginComponent.PNG)

For this component, test cases can be:

- Checking the Login component is rendered or not?
- Checking the placeholder names for the input field (here Username and Password).
- Checking onClick method for Sign in button is working or not?
- Checking props for the component

And the lists go on, writing test cases varies from person to person, Whatever the props we are passing to the Login component you will get to see in the above link, before actually start writing test cases, look at some important terms  useful in writing test cases:

- describe: Breaks your test suite into components.
-  It: Will contain the name for your test case, where you perform individual tests.
- expect: Expect function is used when you want to test a value.
- wrapper: A Wrapper is an object that contains a mounted component
- shallow:method is used to render the single component that we are testing you can also use mount here, the difference between them is mount renders the children, shallow does not.

1. Let&#39;s see the first test case, it is for LoginComponent mounted or not?

    I created a new file named LoginComponent.test.js inside which we are going to write test     cases

    ![](/assets/1.PNG)

    The Enzyme is built to support different versions of React. So, you have to install an Adapter that corresponds to the version of React that you are using. In this test case we simply render a Login component using shallow and check if that wrapper exists or not.
2. The second test case is testing the signUp button

    I have assigned the value to the props in propsData we will further pass the propsData to the login component. signUp button has id signUp so we can identify the button. We are simply creating the same environment as the actual component is rendered.

    ![](/assets/2.PNG)

3. The third test case for checking the usernameType

    In the previous test case, we pass all the props which were not compulsory to do we can do it another way also, we can pass only one prop which we want to send by the following way

    ![](/assets/3.PNG)

    This is LoginComponent.test.js

    ![](/assets/4.PNG)

    This is LoginComponent.js where usernameType is email now after running the test let&#39;s see what we are getting,

    ![](/assets/5.PNG)

    We are getting a text here, so we are on the right track.


4. Checking the type of password

    ![](/assets/6.PNG)

    After writing all the test cases we are going to run it by,

    -  npm test

    Which will show you this kind of result

    ![](/assets/7.PNG)


So, this was all about how you can test your component using jest and enzyme. Thanks for reading, keep learning keep going.
