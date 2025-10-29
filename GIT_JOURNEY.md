# My Git Mastery Challenge Journey

## Student Information
- Name: KARRI SHAHANTH KRISHNA REDDY
- Student ID: 23A91A05G1
- Repository: https://github.com/shahanth4444/git-solved-23A91A05G1.git
- Date Started: 29-10-2025
- Date Completed: 29-10-2025

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all merge conflicts across multiple branches using proper Git workflows.

## Commands Used

| Command | Times Used | Purpose |
|---------|------------|----------|
| git clone | 1 | Clone instructor's repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View and manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved changes |
| git push | 10+ | Push to my repository |
| git fetch | 2 | Fetch updates from instructor |
| git pull | 1 | Pull updates |
| git stash | 2 | Save temporary work |
| git cherry-pick | 1 | Copy specific commit |
| git rebase | 1 | Rebase feature branch |
| git reset | 3 | Undo commits (soft/mixed/hard) |
| git revert | 1 | Safe undo |
| git tag | 2 | Create release tags |
| git status | 50+ | Check repository state |
| git log | 30+ | View history |
| git diff | 20+ | Compare changes |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Production used port 8080, development used 3000
- **Resolution**: Created unified config with environment-based settings
- **Strategy**: Keep production as default, add dev as optional
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 2: config/database-config.json
- **Issue**: Different database hosts and SSL modes
- **Resolution**: Created separate profiles for production and development
- **Strategy**: Restructured JSON to support both environments
- **Difficulty**: Medium
- **Time**: 10 minutes

#### Conflict 3: scripts/deploy.sh
- **Issue**: Different deployment strategies (production vs docker-compose)
- **Resolution**: Added conditional logic based on DEPLOY_ENV variable
- **Strategy**: Made script handle both environments dynamically
- **Difficulty**: Hard
- **Time**: 20 minutes

#### Conflict 4: scripts/monitor.js
- **Issue**: Different monitoring intervals and log formats
- **Resolution**: Environment-based configuration object
- **Strategy**: Used process.env.NODE_ENV to determine behavior
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 5: docs/architecture.md
- **Issue**: Different architectural descriptions
- **Resolution**: Merged both descriptions into comprehensive document
- **Strategy**: Created sections for each environment
- **Difficulty**: Easy
- **Time**: 10 minutes

#### Conflict 6: README.md
- **Issue**: Different feature lists and version numbers
- **Resolution**: Combined all features with clear environment labels
- **Strategy**: Organized features by category
- **Difficulty**: Easy
- **Time**: 10 minutes

### Merge 2: main + conflict-simulator (5 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: New experimental settings introduced.
- **Resolution**: Maintained the stable combined production/development config.
- **Strategy**: Commented out the experimental settings to prevent breakage.
- **Difficulty**: Medium

#### Conflict 2: scripts/deploy.sh
- **Issue**: Experimental docker purge step added.
- **Resolution**: Maintained the stable multi-environment deploy script.
- **Strategy**: Commented out the experimental deploy steps.
- **Difficulty**: Easy

#### Conflict 3: config/database-config.json
- **Issue**: New experimental database connection added.
- **Resolution**: Maintained the stable production/development profiles.
- **Strategy**: Commented out the experimental configuration to maintain stability.
- **Difficulty**: Medium

#### Conflict 4: docs/architecture.md
- **Issue**: Documentation for experimental services added.
- **Resolution**: Merged the experimental sections into the document.
- **Strategy**: Created a new "Experimental Services" section in the documentation.
- **Difficulty**: Easy

#### Conflict 5: scripts/monitor.js
- **Issue**: New experimental AI monitor function added.
- **Resolution**: Maintained the stable environment-based monitoring script.
- **Strategy**: Commented out the experimental AI monitoring function.
- **Difficulty**: Easy

## Most Challenging Parts
1. **Understanding Conflict Markers**: Initially confused by `<<<<<<<`, `=======`, `>>>>>>>` symbols. Learned that HEAD is current branch and the other side is incoming changes.
2. **Deciding What to Keep**: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.
3. **Complex Logic Conflicts**: deploy.sh had completely different logic. Had to understand both approaches before combining.

## Key Learnings
- Mastered conflict resolution process by manually editing files.
- Understood the difference between `git merge` (history graph) and `git rebase` (linear history).
- Practiced using `git stash` for context switching with unfinished work.
- Learned to use `git revert` for a safe undo on shared history.
- Used `git tag` to mark project releases.

## Reflection
This challenge taught me that merge conflicts aren't scary—they're just Git asking "which version do you want?". The key is understanding what each side is trying to do before combining them. I now feel confident handling conflicts in real projects.