## Yarn

Yarn is a new JavaScript package manager built by Facebook, Google, Exponent and Tilde. Its purpose is to solve a handful of problems that these teams faced with npm, namely:

- installing packages wasn’t fast/consistent enough, and
- there were security concerns, as npm allows packages to run code on installation. 


### Relevant Links
- [NPM vs Yarn] (https://www.sitepoint.com/yarn-vs-npm/)

### Functional Differences when Yarn first came out
- First of all, npm didn't use a lockfile. A lockfile contains all the information about the exact version of each dependency.
- Yarn solved this problem by generating a yarn.lock file that stores exactly which version of which dependency was installed.

- The second major shortcoming of npm was that it was non-deterministic. Your node_modules folder is likely to differ from the node_modules folder of your colleague, or even of the different testing and production servers.
- Yarn is a deterministic package manager, which means that all computers with a given package.json file will have the exact same dependencies installed in their node_modules folder. This helps avoid scenarios where code would work on your computer, but not on a different computer.

- Whenever npm or Yarn needs to install a package, it carries out a series of tasks. In npm, these tasks are executed per package and sequentially, meaning it will wait for a package to be fully installed before moving on to the next. Yarn executes these tasks in parallel, increasing performance.


