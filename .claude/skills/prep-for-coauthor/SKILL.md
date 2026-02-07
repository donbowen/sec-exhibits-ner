---
name: prep-for-coauthor
description: Prepare code and analysis for sharing with a co-author.
disable-model-invocation: true
---

Help me prepare this code/analysis for sharing with a co-author. Review the current project and:

1. **Documentation**: Are notebooks and scripts clearly commented? Would a co-author understand the workflow without a phone call?
2. **Setup instructions**: Is the README sufficient for someone to clone and run this? Are dependencies captured in environment.yml or requirements.txt?
3. **Data dependencies**: Are input data files documented? If they can't be shared (e.g., WRDS data), is that noted with instructions on how to obtain them?
4. **Naming**: Are files, variables, and outputs named clearly enough for someone unfamiliar with the project?
5. **Cleanup**: Are there dead code, scratch files, or debugging artifacts that should be removed?

Provide a prioritized list of changes to make before sharing.
