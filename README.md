# PS1 for Problems Cloning

## Due January 18 @ 11:59pm (1 day extension)

---

## It is important that you follow all the directions perfectly. Things do not work unless you follow all the directions.

## If you encounter an error message, please see the problems.md file in this repository before emailing the instructor.

## If you experience problems with git or GitHub, use the GitHub Desktop app to complete this problem set.

### Part 4: Download and install Java 8 SDK

1. You might already have some components of Java installed on your computer. Unless you have a very good reason for keeping other versions of Java around, we recommend that you uninstall all existing versions of Java from your computer (instructions: [Mac](https://www.java.com/en/download/help/mac_uninstall_java.xml), [Windows](https://www.java.com/en/download/help/uninstall_java.xml)). 


2. Although there are several newer versions of Java, we'll be using Java 8. Download the Java SE Development Kit 8u191 (the last three numbers might be different, that's okay!) for your operating system from [here](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). Don't forget to click the radio button indicating that you agree to the terms of the license.

3. After you download the .dmg (Mac) or .exe (Windows), double-click it to start the installation. Click as needed to complete the installation.


### Part 5: Configure and validate Java installation
#### Windows 10 users (If you are using Windows 7, proceed at your own risk.)

1. Launch ``Control Panel -> (Optional) System and Security -> System``. 

2. Click ``Advanced system setting`` in the left pane.

3. Select the ``Advanced`` tab, and click ``Environment Variables`` button.

4. Under ``System Variables`` (the bottom pane), the scroll down to select ``Path``, then select ``Edit...``.

5. In Windows 10, you will see a table listing all the existing ``PATH`` entries.  Click ``New`` then enter the JDK's ``bin`` directory, which should be ``c:\Program Files\Java\jdk-1.8.{x}\bin``, where `{x}` is replaced with the version number you installed in Part 4, Step 2, above. You can determine exactly what it is by looking in that directory called `Java`. Then Select ``Move Up`` to move this entry all the way to the top of the table.

6. Delete all other references to Java in the path.

7. Delete the JAVA_HOME environment variable, if you find it.

8. Open a CMD shell by clicking the ``Start`` button, then selecting ``Windows System -> Command Prompt``.

9. Type ``path`` at the prompt, and you should see output that begins like this, where again the {x} is the exact version you installed from Oracle in Part 4, Step 2.

``PATH=c:\Program Files\Java\jdk-1.8.{x}\bin;``

10. Type ``java -version`` and you should see something like this:

```java

java version "1.8.0_191"
Java(TM) SE Runtime Environment (build 1.8.0_191-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.191-b12, mixed mode)

```

11. Type ``javac -version`` and you should see something like this:

```java

javac 1.8.0_191

```

12. If you get an error message (e.g., "command java not found") or if the numbers are different (e.g., java 1.7...), then something is not right. Go to the problems file in this repository.

#### Max OSX users ####
1. Launch a Terminal. You can do this by finding the Terminal app in your Applications folder, or by going up to the magnifying glass in the upper right corner of your screen and then searching for Terminal.

2. At the prompt in Terminal, type ``java -version`` and you should see something like this:

```java

java version "1.8.0_191"
Java(TM) SE Runtime Environment (build 1.8.0_191-b12)
Java HotSpot(TM) 64-Bit Server VM (build 25.191-b12, mixed mode)

```


3. Type ``javac -version`` and you should see something like this:

```java

javac 1.8.0_191

```

4. If you get an error message (e.g., "command java not found") or if the numbers are different (e.g., java 1.7..., java 10...), then something is not right. Email the instructor and the TAs.


### Part 6: Install and configure Atom

If you have never used Java before, I recommend that you use Atom to write and compile your code for this class. If you have used IntelliJ or Eclipse or another IDE in the past for Java development, you can continue to do so, but I will provide support only for Atom. If you decide to use Atom, follow these instructions to install and configure Atom.


1. [Download Atom](https://atom.io). Double click the downloaded file to unzip it (if necessary), then move Atom **out of your Downloads folder** to a place on your computer where it will be easy to find (e.g., in the Applications folder or on your desktop).

2. Launch Atom. There are a few tabs or frames that open automatically, which you can close by clicking the "X" in the upper right corner of the tab or frame. (If all these windows keep popping up when start Atom, you can disable them.)

3. You now need to install an Atom package that will customize Atom for use in this class. From Atom's menu bar, click the Atom menu, and then select Preferences to open the Settings menu.

<img src="img/atommenu.png" width="300"  />

4. On the left of the Settings area, you’ll see a menu with items like Core, Editor, URI Handling, and so on. Click on the menu item that says Install, which has a plus-sign icon next to it.

<img src="img/install.png" width="600"  />

5. In the search box that appears, enter ``platformio-ide-terminal``. Click Install button for ``platform-ide-terminal``, and wait for installation to complete.


### Part 7: Get a local copy of the repository from GitHub 

We will be using git and GitHub to distribute and collect problem sets. Using GitHub is **not** optional. GitHub and git are  used by millions of software developers at major companies around the world. An important component of this class and of your development as a computer scientist is understanding how to use git and GitHub.

1. Start by creating a folder on your computer for this class called ``CS2`` or ``CS1102``. I have mine on my Desktop so it's easy to find, but you are free to put it wherever is convenient for you.

2. Look up at the top of this webpage you are on right now, and locate the green ``Clone or download`` on the right. Click that button, and then copy the the URL beginning with ``https://`` that appears, which will look something like this, below:

<img src="img/clone.png" width="700"  />

3. In Atom, go to ``Packages -> Command Palette -> Toggle``.

4. In the pop-up window that opens, start typing ``GitHub``, and the GitHub: commands will appear. Select ``GitHub: Clone``.

5. Paste the URL from Part 1 in the first box, and the path to the **course folder** you created to Part 1 followed by the name of your respository in the second box. Here's what the box looks like on my computer. You can see that the repository URL ends in `ps1.git`, while the destination directory ends in `ps1`. Yours will look similar, except the repository URL will end in `ps1-yourusername.git`, and you should choose a directory on your computer that ends in `ps1-yourusername`.

<img src="img/clone-window.png" width="700"  />

6. Click the ``Clone`` button. This will copy your personal `ps1-yourusername` repository to your computer. If you get an error message in red letters, you are probably not following the directions, so try again!

**NOTE:** If you end up with an empty repository following these instructions, [use the GitHub Desktop app](https://desktop.github.com) to do your cloning and your other GitHub activities, as needed. You are free to use the GitHub Desktop application for this class.


### Part 8: Edit a file and push edits to GitHub

1. If you did Part 7 correctly, you should see the contents of the repository in Atom. If you can't see the ``ps1-yourusername`` repository, then go to `File -> Open`, and navigate to your class folder, where you should find your local respoitory. Select `ps1-yourusername`  and click ``Open``. **Do not select your class folder or the `src` folder!** 

2. You should now see something like this, below, with a tree structure showing the files in your current directory in the left pane and an empty pane on the right. (Feel free to close any of the pesky Welcome tabs and panes that Atom likes to open up.)

<img src="img/atom1.png" width="700"  />


3. Click on ``src`` to view the code for this assignment, then click on ``HelloWorld.java``. Code will appear in the panel on the right. Find where you see this in the code:

```java
System.out.println("Hello, World!")
```

Replace the words ``Hello, World!`` with your favorite greeting.

4. From the ``File`` menu, select ``Save`` (or use your usual keyboard shortcut for saving, like command-s in MacOS or control-s in Windows).

5. Go to ``Packages -> GitHub -> Toggle Git Tab``.

6. The Git tab will open, and you'll see something like this, below. Click ``Stage all``.

<img src="img/atom2.png" width="700"  />

7. Type a comment explaining what you did and why where it says ``Commit message``.

8. Click ``Commit to master``.

9. Click the ``Push`` on the right in the bottom menubar, between ``master`` and ``files``. This is the part people always forget, so don't forget!

10. Go to GitHub and confirm that your respository has been updated. You should see the changes reflected in your problem set repository and see ``last updated 1 minute ago`` (or thereabouts). This is what we will grade. Congratulations! 


