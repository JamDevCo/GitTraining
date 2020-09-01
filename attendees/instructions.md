## Instructions

### Step 1. Fork or clone the repository

> Normally, Git repository hosting services generates two remote URL for each
> project, a **git url** or **https url**.
>
> ```bash
> # Git URL:
> git@github.com:JamaicanDevelopers/GitTraining.git
>
> # Https URL:
> https://github.com/JamaicanDevelopers/GitTraining.git
> ```
>
> For more infromation on remote URLs, see [Github Documentation on Remote URLs](https://docs.github.com/en/github/using-git/which-remote-url-should-i-use).

<a href="https://ibb.co/5RTMSfc"><img src="https://i.ibb.co/mcJD2Mz/Jamaican-Developers-Git-Training-Git-training.png" alt="Jamaican-Developers-Git-Training-Git-training" border="0"></a>

##### Cloning with HTTPS URL
If you don't have a `SSH key` setup on Github, then I recommend that you use the HTTPs version for this tutorial

```bash
git clone https://github.com/JamaicanDevelopers/GitTraining.git
```

##### Cloning with HTTPS URL
```bash
git clone git@github.com:JamaicanDevelopers/GitTraining.git
cd GitTraining
```

#### Create a new branch

```bash
git checkout -b attendee--<username>
```

> Considering that there will be multiple changes by multiple editors, 
> we need to create a working branch that will allow us to encapsulate our individual changes before we integrate it with other changes.
> Once we've made our changes, we're going to push the changes and 
> merge it in the main branch, which will render on Github pages.

### Step 2. Create your own attendee page

In the `attendees` folder create a new file with your github username name as the filename followed by `.md`. Example, [`b4oshany.md`](https://jamaicandevelopers.github.io/GitTraining/attendees/b4oshany).

Copy the following code to your `.md` file and fillout the remainding content:
```
## About <replcae-with-your-github-username>

- **Name**: <your-name> :-( 8-)
- **Nationality**: <your-nationality>
- **Website**: <your-website>

#### Tech Stack
- git
- <frameworks-you've-used>

#### Interests
- Software Development (Web, Mobile, no desktop app unless it is Electron)
- <your-tech-based-interests>

## Event 2 - Using Github for Code Integration and Collaboration
- **Date**: Sept. 1, 2020
- **Time**: 6:00 pm EST
- **Meetup URL**: https://www.meetup.com/Jamaican-Developers-Group/events/272676820/

##### Lesson Learnt
- Learnt the basic of `git` and Github.
- Learnt markdown.
- <what-else-did-you-learn>

##### What I wish to learn next?
- <what-do-you-wish-to-learn-next>
```

> You can also find the code above in the [sample-attendee.md](https://jamaicandevelopers.github.io/GitTraining/attendees/instructions) file.

### Step 3. Commit the changes.

Execute the following command is your git terminal:
```bash
git status
```
You should see the file you've created as an untracked file.
For instance:
```bash
Untracked files:
  (use "git add <file>..." to include in what will be committed)=
        attendees/sample-attendee.md
```

Afterwards, run the following the following command to allow git to track your changes.
```bash
# Use "git add" to add your changes to staging 
git add .

# Afterwards, run "git commit" to capture a snapshot of the current staged changes.
# Change the "Added file" message to "Added <username> attendee profile page."
git commit -am "Added file."
```

Execute the following command to check that everything was committed
```bash
git status
```

You console should output something like this:
```bash
PS /Workspace/training/git/GitTraining> git status
On branch attendee-<username>
Your branch is ahead of 'origin/attendee-<username>' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```


### Step 4. Push your changes.

```bash
git push origin <your-branch>
```

### Step 5. Create a pull request to merge your changes.

- Go to the [project github repository](https://github.com/JamaicanDevelopers/GitTraining)
- Click on `Pull Requests` tab, followed by the `new pull request` button.
   <img src="https://i.ibb.co/xz7GdYc/Pull-requests-Jamaican-Developers-Git-Training.png" alt="Pull-requests-Jamaican-Developers-Git-Training" border="0"> 
- Select the branch you wish to merge into master from the `compare dropdown`.
   <img src="https://i.ibb.co/F3BkT08/Compare-Jamaican-Developers-Git-Training.png" alt="Compare-Jamaican-Developers-Git-Training" border="0"> 
- Click Create pull request to open a new pull request

Once you pull request has been created, you can use the following tabs to comment and review the changes.
- Conversation
- Commits
- Checks
- File Changed

### Step 6. Update the contributor page.
- In your local repository, open the `CONTRIBUTORS.md`
- Under the ***List of contributors*** heading add your name followed github username,
  <br>Example: `Oshane Bailey (@b4oshany)
- Save the file and commit the changes.
  ```bash
  git commit -am "Added my name, <username> to the contributors file."
  ```
- Finally, push the code.
  ```bash
  git push origin <your-branch>
  ```


