-> Observations 

1) The merge didn't occcur as there was a merge conflict, I could only merge once the merge conflicts were resolved
2) I was give multiple options by vscode to resolve the merge conflict namely accept incoming changes, accept current changes , accept both changes and compare changes
3) I tried all four and realised that

   -> Accept Current Change: Keeps your existing changes and discards the incoming changes

   -> Accept Incoming Change: Keeps the changes from the branch being merged and discards your current changes.

   -> Accept Both Changes: Keeps both your changes and the incoming changes, merging them together.

   -> Compare Changes: Opens a side-by-side diff view to compare the conflicting changes.



-> Steps followed

(base) vashistas-Air:leargit vashistavallambhatla$ git branch
* main
(base) vashistas-Air:leargit vashistavallambhatla$ git checkout -b feature1
Switched to a new branch 'feature1'
(base) vashistas-Air:leargit vashistavallambhatla$ echo "feature1" > project.txt
(base) vashistas-Air:leargit vashistavallambhatla$ git add .
(base) vashistas-Air:leargit vashistavallambhatla$ git commit -m 'feature1'
[feature1 4a4380b] feature1
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) vashistas-Air:leargit vashistavallambhatla$ git checkout main
Switched to branch 'main'
(base) vashistas-Air:leargit vashistavallambhatla$ git checkout -b feature2
Switched to a new branch 'feature2'
(base) vashistas-Air:leargit vashistavallambhatla$ echo "feature2" > project.txt
(base) vashistas-Air:leargit vashistavallambhatla$ git add .
(base) vashistas-Air:leargit vashistavallambhatla$ git commit -m 'feature2'
[feature2 af876b2] feature2
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) vashistas-Air:leargit vashistavallambhatla$ git branch
  feature1
* feature2
  main
(base) vashistas-Air:leargit vashistavallambhatla$ git merge feature1
Auto-merging project.txt
CONFLICT (content): Merge conflict in project.txt
Automatic merge failed; fix conflicts and then commit the result.
