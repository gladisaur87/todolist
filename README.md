# todolist

The project source for our class projects.

## Prerequisites

- NodeJS
- npm

## Usage

This is a development server that serves static assets. Running `npm start` in the terminal will start a server and all of your files are served out of a `public/` directory, where you can modify files.

## Installation

**The installation instructions are a _one time_ run set of instructions.**

First, go to the [https://github.com/chaseadamsio/todolist](https://github.com/chaseadamsio/todolist) and click the `Fork` button in the top right corner. This will create a new fork of the project in your repositories.

Next, clone your repository into your workspace (mine is `~/workspace`) by running (make sure to replace `<YOUR USERNAME>` with your username:

    git clone git@github.com:<YOUR USERNAME>/todolist.github.io.git

Once that's cloned to your computer, change into that directory and run:

    npm install

Once `npm install` is complete, run:

    npm start

Now you should be able to visit `http://localhost:3000`  in your browser and see the `index.html`. You can modify any file in the `public/` directory and you will see updates when you refresh the browser.

## Troubleshooting

### Server starts and immediately goes back to the command line

This means that the process for the server failed to quit. We can check it by running the following command in the command line:

    ps -ef | grep "[n]ode ./index"

If the server is still running, you should see something like this:

    501 25117 25116   0  7:08PM ttys007    0:00.66 node ./index.js

The important thing to note here is that the output will contain `node ./index.js`, even though everything to that point may be different.

To kill the server, copy the **second number** in the output (in this case it's `25117`) and run (be sure to replace my process number with the one that was output):

    kill 25117
