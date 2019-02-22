# Replace all code with one branch
You should be able to use the "ours" merge strategy to overwrite master with seotweaks like this:

```bash
git checkout seotweaks
git merge -s ours master
git checkout master
git merge seotweaks
```

The result should be your master is now essentially seotweaks.

(```-s ours``` is short for ```--strategy=ours```)

From [the docs](https://git-scm.com/docs/git-merge) about the 'ours' strategy:

This resolves any number of heads, but the resulting tree of the merge is always that of the current branch head, effectively ignoring all changes from all other branches. It is meant to be used to supersede old development history of side branches. Note that this is different from the -Xours option to the recursive merge strategy.


Original content in [StackOverFlow](https://stackoverflow.com/questions/2862590/how-to-replace-master-branch-in-git-entirely-from-another-branch)


