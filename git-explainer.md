## Explaining git concepts

In this exercise, you will write an explanation for various git concepts.

- Don't assume any prior knowledge of git: imagine you are explaining these concepts to a brand new software developer. Because of this, try not to use jargon.
- Write full, complete prose. Bullet points can be useful, but not what we're after for this module.
- Test the explanation. Try your explanation on a non-technical friend before submitting it.

We want explanations for:

- git

Git is a system that allows programmers and those working on software projects to track the changes they make to files and to allow them to collaborate on one project easily through repositories.
- repository

A repository is the collection of files that make up the project and is stored locally on a computer and remotely on a different computer.
- remote

A remote is a copy of a repository held in a central place that all developers/team members push their changes to branches in copies of the repository to in order to share their work.
- branching

Branching allows team members to segregate the work they're doing on new features or bug fixes and enables them to work and make changes freely without affecting code that's currently in production, a sandbox in effect, that can then be merged into the main branch when theire changes are proven to be safe.
- merging

Merging allows the team to take the changes and features they've made in one or more branches and "merge" them into the current "main" branch and have their fixes and features in the production version of the program. Most merges go smoothly but sometimes there are conflicts.
- merge conflicts

A merge conflict occurs when changes have been made in an area of one file on one branch that were made differently in the same area of another branch.
For example, branch A might have an area of code that reads 
```c++
bool Function10(){
    return false;
}
```
and the exact same function in branch B looks like
```c++
bool Function10(){
    std::cout<<"This is a function that returns false"<<std::endl; //<-Using for Debugging
    return false;
}
```
line for line through this file in both branches everything is the same except for the second line. In branch A it reads `return false; ` but in branch B it reads ` std::cout<<"This is a function that returns false"<<std::endl; //<-Using for Debugging` very obviously these files aren't doing the exact same thing, however Git makes no assumptions as to what is needed and what isn't so it takes both versions and puts them on top of each other and asks you to "make it look the way you need it" and commit again. As we are able to understand that the second line in the file in branch B isn't needed and without it, both files look the same, we can remove that to leave us with Branch A's implementation and solve our conflict.
- the 3 git states:
  - modified
 
 A modified file has been changed from the last committed version but hasn't been staged yet.
  - staging
 
 A file is staged when it is on the list to be added to the version history in its current state on the next commit
  - committed
 
When a file is commited, the version of it in the repository is updated with the changes that were made to it since it was last fetched from the remote, if it didnt exist in the remote and was created after the remote was cloned to the local machine, its entire contents are put into the repository. 

# Submitting the exercise

- Navigate to the repository and select your `submission` branch.
- Navigate to the `submissions` directory.
- In the directory, create a new directory named `module-5`.
- Inside `module-5`, create a file named `git-explainer.md`.
- Fill the file with the contents of your completed exercise.
- Commit the changes.
- Navigate to your pull request and verify that the new commits have been added.
- Remember to complete the [module survey](https://goo.gl/forms/4TgngMoXDDHLL2qE3)
