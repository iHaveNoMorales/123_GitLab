# Quiz questions

This is only a "quiz" in the loosest sense that it's asking questions whose
answers will be part of your grade. Please use *any resources you want*, as
long as you list those resources (e.g. peers, websites, etc.)

## Navigating logs

1. What is the SHA for the last commit made by Prof. Xanda on the branch
xanda_0000_movie_processing?
(For this and future questions, the first 5 characters is plenty - neither
Git nor I need the whole SHA.)
9b257
2. What is the SHA for the last commit associated with line 9 of this file?
b2ed3
3. What did line 12 of this file say in commit d1d83?
2. I should really finish writing this
4. What changed between commit e474c and 82045?
The find_top_5 function in process_movie_data.py
## Predicting merges

Assume at the start of each of these three questions that your
branch for switching to a top-10 list was called `top_ten`
and your branch generalizing to any number of movies was called `top_N`.
Predict the behavior of these three possible operations - you don't
have to provide a full `diff` but you should describe at a high level
what changes would happen.

These questions are supposed to be separate paths, not cumulative;
for example, you should *not* assume that the operations of 5 were run
before 6. When testing outcomes later in the lab, you should make sure to
revert back to the state of the branch before you started these questions.

5. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test - you would stay in the test branch and nothing would change
git merge top_N - main would replace top 5 with top N
```

6. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout top_ten - top 5 would switch back to top 10 in the file but not the branch
git merge test - (I know this isn't what was supposed to happen but) I got a merge conflict, I think it was supposed to replace top 10 branch with top 5 from test
```

7. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test - nothing changes stay in test
git rebase top_ten - top 10 failed to replace anything in test but the rebase was still successful?? (think I checked logs to find this out)
git rebase top_N (I know it's supposed to merge conflict but because of above) it successfully rebased top n from top 10 in test branch
```
