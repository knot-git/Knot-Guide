# Try It Yourself

This repository is both the Knot guide and a local practice repository. The notes and changes in `Examples/` are prepared exercises, not signs of a failed sync or damaged files.

No remote repository or network connection is needed, and nothing is pushed to an account. You can also browse the guides, branches, and history.

## Get to Know the States

On your first visit, Changes contains 3 files and the Stash box contains 1 draft:

| Note | Initial state | What it means |
| --- | --- | --- |
| [Weekly Review](Examples/Weekly%20Review.md) | Staged | This week's completed tasks are ready to commit |
| [Reading Notes](Examples/Reading%20Notes.md) | Unstaged | A new reading reflection still needs polishing |
| [Idea Inbox](Examples/Idea%20Inbox.md) | Unstaged | A quick idea that does not belong in the weekly review commit |
| [Weekend Plan](Examples/Weekend%20Plan.md) | Draft saved in Stash | Plans are undecided, so the draft is set aside; the file shows the version before that draft |

**Staging** selects what goes into your next commit. **Stash** sets unfinished changes aside so you can restore them later.

## 1. Commit What Is Ready

1. Open the diff for Weekly Review: the added tasks are what you are about to save.
2. Tap Commit and check that only Weekly Review is listed.
3. Enter a message, such as "Record this week's completed tasks", and commit.
4. Return to Changes: Reading Notes and Idea Inbox are still there, untouched by that commit.

Next, review the diffs for those two notes, stage them, and commit with a message such as "Collect reading reflections and new ideas". Changes should now be empty.

## 2. Restore a Draft You Set Aside

1. Tap the Stash box in the repository header and open "Set aside weekend plan draft".
2. Review its diff: it contains a Saturday walk and a Sunday note-organizing session.
3. Choose Pop and Delete: the draft returns to Weekend Plan and the stash entry is removed. Apply and Keep also restores the draft, but keeps the stash entry.
4. Review, stage, and commit the restored changes, for example with "Plan the weekend".

Before continuing, check that Changes is empty. Commit or stash any other changes you made during the exercises.

## 3. Resolve Two Different Edits

[Daily Summary](Examples/Daily%20Summary.md) simulates editing the same note on a phone and a computer:

- The current `main` branch sets the next step to "read 10 pages".
- The local `notes/desktop` branch changes that same line to "review today's notes".

Two local branches represent these edits; no connection to a computer is needed.

1. Stay on `main`, tap the branch name in the header, find `notes/desktop`, and merge it into the current branch. Do not switch to it first.
2. The merge produces **1 conflicted file with 1 conflict block**. This is the expected result of the exercise.
3. Open Daily Summary in Changes. Choose Use ours or Use theirs, or edit manually to keep both tasks and remove the conflict markers.
4. Check the result, tap Mark as resolved, then Continue Merge to finish the commit.

To cancel instead, choose Abort Merge to return to the state before the conflict. After aborting, you can merge again to retry; after completing it, the merge appears in History.

These exercises make real changes to this repository. Restarting the app does not reset your progress, and the initial file counts change as you work.

See [Git Operations](05-Git%20Operations.md) for more details.
