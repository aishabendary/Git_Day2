# Creating SSH Key
![SSH Key](https://github.com/aishabendary/Git_Day2/assets/144475232/fd3ca6b6-ca61-4fa9-bd8c-72438f40d8f4)


# Merging Branches

![Screenshot from 2023-11-27 13-49-46](https://github.com/aishabendary/Git_Day2/assets/144475232/2eba4949-5fe7-4e5e-bf99-9412d862657c)


# Remove Branch Locally:
Switch to a Different Branch:
Before deleting a branch, ensure you are not currently on the branch you want to delete. If you are on the branch you want to delete, switch to a different branch:
``` git checkout <another_branch> ```
Replace <another_branch> with the name of an existing branch.
# Delete the Local Branch:
Delete the branch locally using the following command:
``` git branch -d <branch_to_delete> ```
If the branch has unmerged changes, use -D instead of -d to force the deletion:
``` git branch -D <branch_to_delete> ```
Replace <branch_to_delete> with the name of the branch you want to remove.

# Remove Branch Remotely (on GitHub):
Delete the Remote Branch Locally:
Use the following command to delete the remote branch locally:
``` git push origin --delete <branch_to_delete> ```
Replace <branch_to_delete> with the name of the branch you want to delete on the remote repository.

Push Changes to GitHub:
Push the changes to the remote repository on GitHub:
``` git push origin --delete <branch_to_delete> ```

# How to list tags locally
``` git tag ```
Running this command in the terminal or command prompt, within the directory of your Git repository, will display a list of all the tags in that repository. If no tags exist, the output will be empty.

If you want to see additional information, such as the commit hash associated with each tag, you can use the following command:
```git show-ref --tags```

#How to delete tag locally and remotely.

Delete Locally:
``` git tag -d <tag_name> ```
Replace <tag_name> with the name of the tag you want to delete.

Delete Remotely:
``` git push origin --delete <tag_name> ```

# What is git rebase
git rebase is a Git command used to integrate changes from one branch into another. It is a powerful and flexible tool, but it should be used with caution, especially when working with shared branches, as it rewrites commit history.

The basic idea of rebasing is to take a sequence of commits and apply them onto a different base commit. This is different from merging, which creates a new merge commit to reconcile the changes from different branches.

``` git checkout feature_branch```
```git rebase main```

Complete the Rebase:
After resolving conflicts (if any) and completing the rebase, you might need to force-push the branch to update the remote repository:

```git push origin feature_branch --force```


