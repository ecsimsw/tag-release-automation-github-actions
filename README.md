# github-action-release-automation
Github action sample code for release and tag automation

## Usage
1. Handle pull request [opened, synchronize, closed] events, on specific branch.  ('main' on this sample)  
2. Filters specific labels in PR.  ('release' on this sample)
3. Test job is activated when there is a new commit on this PR
4. When PR is merged,    
   - Test code will be ran again     
   - Get latest tag and make new version of tag (latest tag + 1)     
   - Release with new tag   
