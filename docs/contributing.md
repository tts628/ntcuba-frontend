# How to contribute
This doc guide to contribute this project.

There are several ways to contribute to ntchba-frontend:
1. Develop and Commit source code.
2. Report issues.
3. Discuss or Answer questions.
4. Share use cases.

## Step 1:  Fork the repository
Fork this [repository](https://github.com/kobe860219/ntcuba-frontend) to your github.

## Step 2: Clone the ntcuba-frontend to your local machine
Clone your ntcuba repository to local.

```
# USERNAME - your github user account name
git clone https://github.com/${USERNAME}/ntcuba-frontend.git

cd ntcuba-frontend

# set upstream
git remote add upstream https://github.com/kobe860219/ntcuba-frontend.git

# Don't push to the upstream master
git remote set-url --push upstream no_push

# Check upstream and origin:
# origin    git@github.com:${USERNAME}/ntcuba-frontend.git (fetch)
# origin    git@github.com:${USERNAME}/ntcuba-frontend.git (push)
# upstream  git@github.com:kobe860219/ntcuba-frontend.git (fetch)
# upstream  no_push (push)
git remote -v
```

## Step 3: Create an issue
* Create an issue on [ntcuba-frontend](https://github.com/kobe860219/ntcuba-frontend)

## Step 4: Create a local branch for your contribution
```
# Make your local master up-to-date
git checkout master
git fetch upstream
git rebase upstream/master

# Create a new branch formatted with NTCUBA prefix and issue number
git checkout -b NTCUBA-${issue_number}

# Example 
# git checkout -b NTCUBA-1

```

## Step 5: Develop and Create commits
* Edit the code on the NTCUBA-${issue_number} branch.
* Create commits.
```
git add .
git commit -m "NTCUBA-${issue_number}. ${Commit_Message}"

# Example
# git commit -m "NTCUBA-1. Add a test file"
```

## Step 6: Push your local branch to your personal fork
`git push origin NTCUBA-${issue_number}`

## Step 7: Create a pull request on github UI
* Visit your fork at your repository.
* Click `Compare & Pull Request` to create a pull request.
* Create a pull request.

## Step 8: Check Github Actions
* Visit https://github.com/kobe860219/ntcuba-frontend/actions
* Please make sure your pull request can pass all workflows.

## Step 9: The Review Process
* Anyone can be a reviewer and comment on the pull requests.
* Reviewer can indicate that a patch looks suitable for merging with a comment such as: "Looks good", "LGTM", "+1". (PS: LGTM = Looks Good To Me)
* Contributors can ping reviewers by commenting 'Ready to review'.
* At least two indication of suitability (e.g. "LGTM") from countributors is required to be merged.