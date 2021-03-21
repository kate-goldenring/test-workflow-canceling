# test-workflow-canceling
This repo tests using the [Cancel Workflow Action](https://github.com/marketplace/actions/cancel-workflow-action). Specifically, it tests that previous workflows on a PR are canceled when new commits are made to the PR. It affirms that the workflows of PR1 are not canceled by new commits to PR2. The action manages this by only canceling previously running workflows for that branch. 
Tests performed:
1. Cancel workflow is not run on push to main (on PR merge)
2. Cancel workflow is run on every commit to a PR
3. Cancel workflow cancels previous workflow runs upon new commits to a PR
4. Workflows of PR1 are not canceled by new commits to PR2
5. Multiple workflows can be specified in the Cancel workflow
