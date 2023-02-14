# github-action-release-automation
Github action sample code that automate tag / release generation.

## Usage
Performs tests and automatic tagging/distribution, filtered by specific branch and PR label.     
With the PR requested, the test shall be executed when a commit is added to the PR.      
After merged, final test is executed. If it passes a new tag is created by adding 1 to the last number of the most recent tag value and released with the tag.

## Workflow
[Event from PR opened, Synchronize]
1. `pr_opened_synchronize` file is triggered.
2. Filters specific labels and dest branch on PR.  ('release', 'main' on this sample)
3. `test_job` is activated when there is a new commit on this PR.

[Event from PR closed]
1. `pr_closed file` is triggered.
2. Filters specific labels and dest branch on PR.  ('release', 'main' on this sample)
3. `test_job` is activated if this PR is merged properly.
4. `release_job` is activated. Get latest tag and make new version of tag and create relea se with this tag.
