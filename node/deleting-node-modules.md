# Deleting Node Modules

We all know an easy way to remove node modules. But we've all come to a situation where we have too many folders and subfolders where we can't move and remove node modules.

Below are the methods that can be used for the same :

## Method 1 | Using npkill

Directly use npkill using npx

```bash
npx npkill
```

![Demonstrating npkill](https://i.stack.imgur.com/B6GlX.gif)

## Method 2 | Using find and rm

List out all the directories to be deleted:

```bash
find . -name 'node_modules' -type d -prune
```

Delete directories from the current working directory:

```bash
find . -name 'node_modules' -type d -prune -exec rm -rf '{}' +
```

---

> PS : Above methods were taken from a [stackoverflow discussion](https://stackoverflow.com/questions/42950501/delete-node-modules-folder-recursively-from-a-specified-path-using-command-line)
