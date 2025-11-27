###### by Galileon Destura
# Git Exerecises
Hello, CSS students! Welcome to the repository for our Git exercises. Do your best to follow along. If you feel stuck or if you need any help, raise your hand or approach any officer in the vicinity. Don't feel pressured, and don't be afraid to ask any questions! Thank you for participating!

## Scenario 1: git clone
###### i like your code, g
 For this scenario, you will need to ***clone*** a repository. Speficially, *this* repository! Its *suuuper* easy a baby could do it. We'll be using codespaces for this. Make a *blank template* file in Codespaces

<img width="1865" height="880" alt="image" src="https://github.com/user-attachments/assets/30c39c44-eb83-483b-a0e3-ff8e83e51405" />

And paste this into the terminal:

`git clone https://github.com/Leon7774/CSS-Git-Exercises.git`

This clones/downloads the repository into the active directory. After that, move into the downloaded repository using

`cd CSS-Git-Exercises`

 Notice that your terminal directory changes after doing `cd`. `cd` is short for "change directory', which changes your active directory.
 
<img width="602" height="36" alt="image" src="https://github.com/user-attachments/assets/8effd634-9ca0-44c1-98b8-f0c2e06f8b6f" />



After moving into the downloaded repository using "cd" earlier, we can now open the repository in VSCode using 

`code .`

The command `code [directory]` opens the given directory in VSCode. We used `.`, which opens the *current* directory. `code` can be used like `code ./Downloads` or `code ./ProjectNemo`. Opening projects like this is *faster* than downloading a repo with Git and manually finding the folder in VSCode


### Congrats! 🎉🎉🎉🎉 You've officially cloned your (maybe) first repo! 

## Scenario 2: git status
###### ~~Makima~~ git is watching
##### Before we save anything, we need to create something! And then, we need to check if Git is watching.

1.  **Create a file:** Create a new file in the folder named `YourName.java` (e.g., `Galileon.java`). 
2.  **Add code:** Write a simple `System.out.println("Hello World");` inside.
3.  **Check Status:** Run the following command to see what Git thinks of your new file:

    ```bash
    git status
    ```

    > **Observation:** You should see your file listed in **RED** under "Untracked files". This means Git sees the file, but isn't saving it yet.

---

## Scenario 3: git add
###### secure the bag
##### We need to move our file from "Untracked" to the "Staging Area". Think of this like putting items in your shopping cart before checking out.

1.  **Stage the file:** Tell Git to track this specific file:

    ```bash
    git add YourName.java
    ```

    *(Pro-tip: You can type `git add .` to add everything at once, but be careful!)*

2.  **Verify:** Let's check the status again to make sure it worked.

    ```bash
    git status
    ```

    > **Observation:** The filename should now be **GREEN**. This means it's "Staged" and ready to be saved.

---

## Scenario 4: git commit
###### put a ring on it
##### The file is staged, but it's not permanently saved in the history yet. We need to "commit" the changes. This is like hitting the "Buy Now" button.

1.  **Commit:** Run the command below. **IMPORTANT:** Always include a message inside the quotes!

    ```bash
    git commit -m "Added my first Java file"
    ```

2.  **Final Check:** Run status one last time to make sure your desk is clean.

    ```bash
    git status
    ```

    > **Observation:** It should say `nothing to commit, working tree clean`. You did it!
    

---

## Scenario 5: git checkout
###### it's rewind time
##### Sometimes we mess up, or we just want to see how things looked in the "good old days." Git lets us time travel to any point in history.

1.  **Get the Receipts:** First, we need the ID of the commit we want to visit. This ID is called a "Hash".
    ```bash
    git log --oneline
    ```
    *Copy the random string of characters (like `f3a2b1`) next to your **first** commit.*

2.  **Travel Back:** Paste that ID into the checkout command.
    ```bash
    git checkout <paste-your-hash-here>
    ```

3.  **Look Around:** Open your `YourName.java` file.
    * *Observation: If you made changes recently, they are gone! You are looking at the file exactly as it existed in the past.*

    > **WARNING:** You are now in a **"Detached HEAD"** state. 💀
    > Don't panic! It just means you are in "Museum Mode"—you can look, but you shouldn't touch or save new changes here.

4.  **Back to the Future:** Let's return to the present day (the latest version of your code).
    ```bash
    git checkout main
    ```
    *(Note: If your main branch is called `master`, type `git checkout master` instead.)*
