# jira-worklog

Simple CLI app to add worklogs to JIRA

## Configure

Add environment variables to your `~/.zprofile` or `~/.bash_profile` based on your shell:

```
export JIRA_API_TOKEN=api-token
export JIRA_API_USER=user@test.com
export JIRA_API_HOST=https://test.atlassian.net
```

To create an API token please visit: https://id.atlassian.com/manage-profile/security/api-tokens

## Create worklog

```
Usage: worklog <issue> <time> <comment>
```

> Use time format: 60s, 10m, 1h

Example:

```
$ worklog ISSUE-123 90m "Implement feature"

2022-05-17T07:47:41.825+0000: [PT1H30M] Implement feature
201: Created
```

## List active issues

Without any command line parameters the script will print the list of active issues.

```
Usage: worklog <issue> <time> <comment>
Use time format: 60s, 10m, 1h
Active issues (2)
* ISSUE-123: Very important story [In Progress]
* ISSUE-456: Another very important story [QA]
```

## Dependencies

* Groovy
