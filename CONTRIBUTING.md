# Contributing for LinkUp

First of all thanks for showing interest to contribute to LinkUp 💖
When it comes to open source, there are different ways you can contribute, all of which are valuable. Here's a few guidelines that should help you as you prepare your contribution.

## Setup the Project

In order to contribute to a project on GitHub, you must first get a copy of the project running locally on your computer. This process is sometimes called a "build process". 

There are five steps to building this project:

1. [Set up Git and Install Node.js](#set-up-git-and-install-nodejs)
1. [Fork the repository](#fork-the-repository)
1. [Clone your fork](#clone-your-fork)
1. [Install dependencies](#install-dependencies)
1. [Run the project](#run-the-project)

Once you get the project built, see if you can fix some [issues](https://github.com/arpittyagi102/LinkUp/issues?q=is%3Aissue+is%3Aopen)

### Set up Git and Install Node.js

> All GitHub projects are backed by a version control software called *Git*. You'll need to [set up Git](https://docs.github.com/en/get-started/quickstart/set-up-git) in order to contribute to *any* project on GitHub.

**Link Up** is a real time chatting application project, it utilizes, MERN, socket.io. You'll need to [install Node.js](https://nodejs.org/en/) in order to run the project.

### Fork the repository

A *fork* is a copy of a repository. Forking a repository lets you to make changes to your copy without affecting any of the original code.

Click **Fork** (in the top-right corner of the page) to copy this repository to your GitHub account.

### Clone your fork

A *clone* is a downloaded version of a repository. Cloning our fork lets you download a copy of the repository to your computer.

Use `git` to clone your fork

```
git clone https://github.com/YOUR-USERNAME/LinkUp
```

### Install dependencies

The beauty of open source is that you can install and use code that other people have written, allowing you to focus on the unique requirements of your project. Third-party code that your project installs is called a *dependency* because it is required to work.

This project uses [npm](https://www.npmjs.com/), a command-line tool bundled with Node.js, to maintain third-party dependencies.

First, navigate into the project's directory

```
cd LinkUp
```

Next, Create a branch and switch to the branch which is a good industry practice don't operate on main branch

```
git branch YOUR_BRANCH_NAME
git checkout YOUR_BRANCH_NAME
```

Now, Install the dependencies for the server
```
cd linkup-backend
npm install
```

Install the dependencies for the client

```
cd ../linkup-frontend
npm install
```

Set up the environment variables

```
cp ./env_sample/.env.backend.sample ./linkup-backend/.env
cp ./env_sample/.env.frontend.sample ./linkup-frontend/.env
```

Start the development server

Run the Server
```
../linkup-backend
npm start
```


Run the Client
```
cd ../linkup-frontend
npm start
```

### Run the project

Access on Web-Browser

```
http://localhost:3000
```

**For automatic setup run  ```setup.sh``` in terminal**

For testing purposes this credentials can be used:

```
"email":"rohitsharma@gmail.com",
"password":123456
```

```
"email":"viratkohli@gmail.com",
"password":123456
```

## Submit a Pull Request

Making changes on a *fork* doesn't affect the original code, in order to fix an issue in the main project, you *want* to change the original code. A *pull request* is a GitHub feature that lets you do just that!

There are three steps to submitting a pull request:
1. [Save your changes locally](#save-your-changes-locally)
2. [Send your changes to your fork](#send-your-changes-to-your-fork)
3. [Open a Pull Request](#open-a-pull-request)


### Save your changes locally

First, get a list of all the files you have changed.
```
git status
```

Next, *stage* the file you want to save. This will add the file to a new list that is ready to be saved.

```
git add src/YOUR_FILES
```

Next, verify that the file has been staged correctly. Notice that the text color has changed, and your file is now in a list that says "Changes to be committed" instead of "Changes not staged for commit"
```
git status
```

Finally, save your staged files.
```
git commit -m "Commit_Message"
```

You'll often hear this process called *committing* changes. It's the exact same thing.

### Send your changes to your fork

With one simple `git` command, you can send the changes you just committed locally to your *fork* on GitHub.

```
git push origin BRANCH_NAME
```

### Open a Pull Request

1. Find the **New Pull Request** button
2. Select the option to **compare across forks**
3. Select **your username** in the `head fork` option
4. Select **LinkUp** in the `base fork` option
4. Click **Create Pull Request**


Now that you have successfully opened a pull request, now patiently wait for someone to respond. Always remember the open source community is supportive and generous but they have jobs, families and friends so wait patiently before contacting them directly.
