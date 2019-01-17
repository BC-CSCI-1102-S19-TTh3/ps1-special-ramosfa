# Windows problems (For Mac problems, see below)

## Problem: " 'javac' is not recognized as an internal or external command "

The issue might be that you have another version of the Java runtime environment (JRE) that is being looked up instead of the version of the Java SE development kit (JDK) that you just installed. There are a couple of possible reasons for this.

1. It might be because you did not use `Move Up` to move your new entry to the top of the table in Step 5 of Part 5. Follow all the steps again in Part 5. If you see another entry in the table for Java in your path, (e.g., c:\Program Files\Java\jre-10.0\bin) either delete that other Java entry or just make sure your new entry is higher in the table by using ``Move Up``.

2. It might be that you did move your new entry to the top but you did not enter the path correctly. I noticed that some people decided to install Java in some random place rather than just letting the installer pick the best place. If you did this, delete what you installed and start over again at step 4, allowing the installer install Java where it wants to. Continue with the instructions and make sure that you add an entry to the path environment variable that corresponds exactly to that installation location, which will probably be something like `c:\Program Files\Java\jdk-1.8.201\bin`. Then follow the instructions immediately above in item 1.

## Problem: "Please tell me who you are" when trying to push to GitHub

In theory, Atom comes with full git support, but it appears it might not be working for some Windows users. Here are some instructions that I found on the web.

1. Quit Atom.

2. Install git from here: https://git-scm.com/downloads

3. Go to cmd, as you know how to do.

4. Type the following but replace `youremailaddress@bc.edu` with your actual email address.

```bash
git config --global user.email "youremailaddress@bc.edu"
```

5. If that works, then type the following but replace `Your Name` with your name.

```bash
git config --global user.name “Your Name”
```

6. Relaunch Atom and try pushing your changes again. 

If steps 4, 5, or 6 did not work, just use the [GitHub Desktop app](https://desktop.github.com).

---

# Mac OSX Problems
## Problem: "unable to push, error 403"
This usually means that your credentials have not been entered or are incorrect. Here's one possible way to try to deal with this:

1. Open your ps1 directory in Atom as described in the problem set, then go to `Packages -> platformio-ide-terminal -> New Terminal`.

2. In the little terminal window that opens up, type the following

```bash
git commit -m "making changes"
```

3. Then type

```bash
git push
```

4. If all goes well, you will be asked for your GitHub username and password. You can enter them, and in theory, you won't have to enter them again.

If this does not help, just use the [GitHub Desktop app](https://desktop.github.com).


## Problem: "unable to find remote helper for https"

The issue is that there is a missing dependency for git that arose in a recent OSX update. If you got a lot of chat from your computer about Xcode or developer tools, it was probably your operating system trying to get that missing dependency for you. Here are some possible solutions. (Remember to quit Atom before trying anything.) Here's a way to try to deal with this:

1. open a Terminal, and type the following:

```bash
xcode-select --install
```

2. In the window that pops up, select `Install` and continue to follow the prompts. (Note that this might take a long time!)

If this does not help, just use the [GitHub Desktop app](https://desktop.github.com).

## Problem: You already have a different version of Java installed

1. Open a Terminal

2. Type these two commands

```bash
cd /Library/Java/JavaVirtualMachines
ls
```
3. You'll see multiple version of the Java sdk. Navigate into the `Contents` directory in the version you don't want to use using `cd`, e.g.,

```bash
cd jdk-10.0.1.jdk/Contents
```

4. Rename `Info.plist` to `Info.plist.disabled`, like this:

```bash
mv Info.plist Info.plist.disabled
```



