# Day 2 notes
Tip: Don't worry about speed for now, as long as you solve it!

## Git

Git is a tool to keep history of your code.
It keeps track of all changes.
Also allows you to collab with others.

### The Git Process
1. From your terminal, make sure git is installed
2. Make a new folder with the command `mkdir` & add a folder name
3. Navigate to the new folder with `cd`
4. Use command `git init` to initialize empty git repository
5. Use command `git status` to make sure you're on the branch master
6. Add a new file with `touch` command
7. Use the command `git add` and the new file name to add the file
8. Next, use `git commit -m "Message here"`
9. If you need to add more files, repeat steps 6 - 8
10. Any time any files are modified, github will know that there are changes to commit. You can also use `git diff` to compare your files to a previous version.
11. After modifying files, go through the `git add, git commit -m "message"` process again.
12. TIP: You can use `git add .` to add EVERYTHING in the folder to git. This is good if you're working on multiple files and you need to update everything at once.
13. TIP: If you use `git add .` , you only need to use `commit -m "message"` ONCE to commit multiple files.
14. Go to Github and create an empty repository
15. Push the existing files to the empty repository with the instructions shown. Use `git remote add origin main` & `git push` ... (let's double check these instructions next time we create a new repository because the teacher went fast through this part)
16. TIP: DO NOT make changes on Github directly! Only make changes in VS and update with Github.
17. If you need to get your code from Github and put it on a new computer, you can copy the SSH link and use `git clone` plus the link
18. TIP: If you make a mistake and need to go back to a previous version, the best way to do this is to check your commits history on Github, look at the version you want to use, edit your current file and then go through the commit & push process again.

### Approaching Problems

1. Write out every step of the problem in comments before starting code.
2. Start with "Here is what we start with. And this is what we want the result to be."
3. You can split each step up into known/unknown ... ex: (known) I know how to sum 2 numbers, (unknown) how do I add multiple numbers? 
4. With unknowns, such as "how do I convert a string to a number?" we can use google and find out about `Number()` 
5. When you find the solution, great! This is a good time to `commit` to github
6. Once you find the solution, you can always `refactor` your code to make it cleaner and more concise.
7. After refactoring, you can get rid of old comments after figuring things out.
8. When you create functions, you can re-use them as many times as you want.
9. You must run a function with a parameter, such as addNumbers(array) > the parameter is between the brackets.
10. Consider changing c style for loops to for in loops. for example: `for (let i in array)` > in loop goes through everything the array 1 by 1 until the end
11. Same thing with for of loops, `for (let i of array)`
12. Difference between `for in` and `for of`: for in loops through INDEXES, for of loops through VALUES

### I should go back to compass and refactor again using 'for of' and update my answer. i also don't think i needed all those variables. let's do something like

```js
for (let i of array) {
  sum += Number(i);
}

or 

for (let i in array) {
  sum += Number(array[i]);
}