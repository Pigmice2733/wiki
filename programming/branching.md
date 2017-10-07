# Branching

In Git, *branches* are different paths of development. They allow multiple developers to work on code simultaneously without interfering with each other.

The default branch is named `master`. The code to be deployed on the robot belongs on this branch.

When you want to make changes to the code, create *feature branches* for your work. Feature branches should start with a present tense verb, and should be in kebab case. They also should be prefixed with your initials followed by a `/`. Examples:

- `pch/update-robotpy`
- `cee/implement-flying`
- `cee/delete-drivetrain`

To create a branch, run:
```
git checkout -b cee/implement-flying
```

To upload that branch to GitHub, run:
```
git push -u origin cee/implment-flying
```

You should create a *pull request* on GitHub for your branch so that others can review your code. Use the `WIP` (work in progress) label until you feel that your branch is ready to be merged.

As you develop your feature, deploy your code to the robot to test whether it works. Be sure to frequently integrate others' changes from master using:
```
git rebase origin/master
```

Once you feel confident that your code is ready, replace the `WIP` pull request label with `Ready`. Then request review from a mentor or a student. Students can review smaller changes, while large changes should be reviewed by mentors. Requiring all code to be reviewed ensures that the code stays high quality.

Once a mentor or a student have approved your changes, you may merge your code into `master`. At that point you can delete your feature branch.
