# Check the date of the last commit

This action checks whether the specified interval for the last commit was reached. If this was reached, the action returns true otherwise false. This can be used to check whether the nightly build has to be started, for example.

## Inputs

## `token`

**Required** The authentication token for the repository. Example `${{ secrets.GITHUB_TOKEN }}`.

## `interval`

The interval (in seconds) to check the last commit. Default `86400` -> 24 hours

## Outputs

## `has-updates`

true indicates that the build has been done and the last commit was 24 hours ago. 
false indicates that the build should not be started

## Example usage

```yml
uses: actiwaredevelopment/action-io-repo-last-commit-check@v0.1
with:
  token: ${{ secrets.GITHUB_TOKEN }}
```
