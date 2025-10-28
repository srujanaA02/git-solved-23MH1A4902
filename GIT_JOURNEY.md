# My Git Mastery Challenge Journey

## Student Information
- Name: Aketi Lakshmi Srujana
- Student ID: 23MH1A4902
- Repository: https://github.com/srujanaA02/git-solved-23MH1A4902
- Date Started: 27-10-2025
- Date Completed: 28-10-2025

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all 
merge conflicts across multiple branches using proper Git workflows.

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

### Merge 2: main + conflict-simulator (6 files)


#### Conflict 1: config/app-config.yaml
- **Issue**: Conflict between updated logging configuration and environment setup  
- **Resolution**: Merged both by including all logging levels under unified structure  
- **Strategy**: Retain environment flexibility with clear default values  
- **Difficulty**: Medium  
- **Time**: 10 minutes  

#### Conflict 2: config/database-config.json
- **Issue**: Added new replica configuration conflicting with SSL settings  
- **Resolution**: Combined both into a multi-profile setup  
- **Strategy**: Keep production with SSL enabled and replicas defined  
- **Difficulty**: Medium  
- **Time**: 12 minutes  

#### Conflict 3: scripts/deploy.sh
- **Issue**: Deployment script had overlapping commands from both branches  
- **Resolution**: Integrated safety checks and consistent environment variables  
- **Strategy**: Merge logic ensuring rollback support  
- **Difficulty**: Hard  
- **Time**: 20 minutes  

#### Conflict 4: scripts/monitor.js
- **Issue**: Extra monitoring hooks from simulator branch  
- **Resolution**: Kept essential metrics, removed redundant logs  
- **Strategy**: Unified monitoring interval for consistency  
- **Difficulty**: Easy  
- **Time**: 8 minutes  

#### Conflict 5: docs/architecture.md
- **Issue**: Conflict between diagram references and updated section titles  
- **Resolution**: Merged both diagrams and provided clear version notes  
- **Strategy**: Retain instructor’s structure but include simulator improvements  
- **Difficulty**: Easy  
- **Time**: 5 minutes  

#### Conflict 6: README.md
- **Issue**: Version and feature descriptions mismatch  
- **Resolution**: Combined features under latest version (v1.1.0)  
- **Strategy**: Simplify and maintain consistent structure  
- **Difficulty**: Easy  
- **Time**: 10 minutes  

## Most Challenging Parts

1. **Understanding Conflict Markers**: Initially confused by `<<<<<<<`, `=======`, `>>>>>>>` symbols. Learned that HEAD is current branch and the other side is incoming changes.

2. **Deciding What to Keep**: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.

3. **Complex Logic Conflicts**: deploy.sh had completely different logic. Had to understand both approaches before combining.

4. **Testing After Resolution**: Making sure resolved code actually worked was crucial.

## Key Learnings

### Technical Skills
- Mastered conflict resolution process
- Understood merge conflict markers
- Learned to use git diff effectively
- Practiced all major Git commands

### Best Practices
- Always read both sides of conflict before resolving
- Test resolved code before committing
- Write detailed merge commit messages
- Use git status frequently
- Commit atomically

### Git Workflow Insights
- Conflicts are normal, not errors
- Take time to understand both changes
- When in doubt, ask for clarification
- Document your resolution strategy
- Keep calm and read carefully

## Reflection
This challenge taught me that merge conflicts aren't scary - they're 
just Git asking "which version do you want?". The key is understanding 
what each side is trying to do before combining them. I now feel 
confident handling conflicts in real projects.

The hands-on practice with all Git commands (especially rebase and 
cherry-pick) was invaluable. I understand the difference between merge 
and rebase, and when to use each. Most importantly, I learned that 
git reflog is a lifesaver!
Added final reflections
