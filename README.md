# Github Workshop: Breakout Room Guide
[Link to Slides](https://docs.google.com/presentation/d/1SGffEW3yXhyKxpsX4FsUYjsyCjeVO-j-nl6I3uQgZyw/edit#slide=id.g1244dfa059c_3_0)

### Agenda (1hr 30min)
* Intro to Git (10 min)
* Demo 1: Repository (5 min)
    * Task 1: Breakout room (~5 min)
* Demo 2: Collab on Main (10 min)
    * Task 2: Breakout room (~15 min)
* Demo 3: Create Branch & Checkout (10 min)
    * Task 3: Breakout room (~15 min)
* Demo 2: Merge to main using pull requests (5 min)
    * Task 4: No breakout room ???
* Questions (10 min)

### Intro to Git
* What is Git?  
* Bias in the industry
    * Let's abandon the `master-slave` terminology
    * Github and Gitlab recently renamed their inital branch from `Master` to `Main`
    * What you can do in the future: 
        * Refer to the inital branch as `Main`, not `Master`
        * Rename your initial branch to Main, if you can
            * To rename, do`git branch -m main`

:::warning
:warning: Don't follow along during the demo. You will do it in the breakout room. 
:::

## Task 1: Create a repository (5 min)

:::success
:information_source: **Breakout Room Reminders** 
* You will stay with the same partner for all the breakout room tasks. 
* Choose which one of you will be Dev 1 and Dev 2. 
* Execute the commands in `grey box`  on your terminal
* Any command wrapped with a `< >` should be replaced with your own unique value
    * For example, `cd <>` → `cd My-Desktop`
:::

#### Before you begin
* Choose which one of you will be Dev 1 and Dev 2
* One person can share their screen

#### Instruction
* Dev 1 creates a new repository on github.com
    ![](https://i.imgur.com/Gxtohub.png)
    * Choose public not private 
    * Check the `Add a README file` box to create a default `Main` branch 
    * Leave the rest the way they are
    ![](https://i.imgur.com/cOlArNg.png)
* Dev 1 adds Dev 2 as a collaborator so that Dev 2 has access to modify the repository
    * Dev 2 shares their Github username with Dev 1
    * Dev 1 follows this: `Settings` > `Collaborator` > `Add people` button > Search username > `Add username to this repository`
    * Dev 2 should accept the email invite from Dev 1, the repository owner

**Both Dev 1 and Dev 2 individually execute the following:** 
* Open the terminal and navigate to where you want to clone the repository
    * For example, `cd Desktop`
* Clone the repository by running `git clone <url>`
    * The URL can be found in your Github repository. Use the HTTPS URL 
    ![](https://i.imgur.com/CLroIyl.png)
    * The cloned repository will show up as a folder on your local computer

:::info
:raised_back_of_hand: Return to the main room for Demo 2!
:::

## Task 2: Collaborate on Main (10 min)

:::success
:information_source: **Breakout Room Reminders** 
* Execute the commands in `grey box`  on your terminal
* Any command wrapped with a `< >` should be replaced with your own unique value
    * For example, `cd <>` → `cd My-Desktop`
:::

#### Instruction

1. **Dev 1 creates a new file** `collab1.txt` and adds a line to the file
    ![](https://i.imgur.com/mQv8XJ9.png =x200)
    * To create a new file, do the following. This is the *only* command in this workshop that is different for Mac and Windows
        * Mac: `touch collab1.txt`
        * Windows: `type NUL > collab1.txt` or `echo . > collab1.txt`
2. **Dev 1 pushes `collab1.txt` to the remote repository** by running the following:
    * `git add collab1.txt`
    * `git commit -m "Add collab1.text"`
    * `git push origin main`
3. Once Dev 1 is finished, **Dev 2 should pull** the current version of the main branch
    * `git pull`
4. **Dev 2 updates the `collab1.txt` file** by adding a new line
![](https://i.imgur.com/I8nzcLi.png =x200)
5. **Dev 2 pushes new changes to the main branch**
    * `git add collab1.txt`
    * `git commit -m "Add collab1.text"`
    * `git push origin main`

:::info
:raised_back_of_hand: Return to the main room for Demo 3!
:::

## Task 3: Branching & Checkout (15 min)

:::success
:information_source: **Breakout Room Reminders** 
* Execute the commands in `grey box`  on your terminal
* Any command wrapped with a `< >` should be replaced with your own unique value
    * For example, `cd <>` → `cd My-Desktop`
:::

#### Instruction for Both Devs 

1. **Create a new branch `git checkout -b <>`**
    * `<>` is the branch name
        * Dev 1 `git checkout -b dev-1`
        * Dev 2 `git checkout -b dev-2`
    * You will automatically be switched to the new branch
    * The new branch will inherit all the files that were on the Main branch, including the `README.md` and `collab1.txt`
2. **Create a new file** titled `dev1.txt` or `dev2.txt` in the new branch and add some text
    * To create a new file, do the following. Replace `<>` with your file name, `dev1.txt` or `dev2.txt`
        * Mac: `touch <>.txt` 
        * Windows: `type NUL > <>.txt` or `echo . > collab1.txt`
3. **Stage, commit and push the file** to your branch (refer to Task 1 for the terminal commands)
    * `git add <>` (replace <> with your file name)
    * `git commit -m "Add file <>"` (replace <>)
    * `git push origin <branch-name>` (replace <> with your branch name `dev-1` or `dev-2`)
4. Now, we are ready to create a pull request on Github (next demo)

:::info
:raised_back_of_hand: Return to the main room for Demo 4!
:::

## Task 4: Merge to Main using Pull Requests
* What is a pull request?
    * Request changes in your branch to be merged into the main branch
    * Your pull request will contain all your new change
    * In an ideal scenerio, you will have someone review your code and either accept or request changes for your code
* Go to your branch on Github
    * You should see a notification to make a pull request
    ![](https://i.imgur.com/wV7rtKy.png)
    * Click on `Compare & pull request`
    * Add a description for your pull request
    * Add your partner Dev as a reviewer
    * Click `Create pull request`
* Your partner Dev can review & accpet the pull request and merge to main
* To verify on your terminal: 
    * Go back to the main branch by running `git checkout main`
    * Pull everything to your local computer by running`git pull origin main`
    * `ls` to see that all your files are here

## Task 5
Please fill out the survey [here](https://www.surveymonkey.com/r/githubworkshopspring2022)! 

💯 **Great work finishing everyone!**
