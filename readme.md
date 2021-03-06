# Slack Jira Issue Expansion

[![Build Status](https://travis-ci.org/meanbee/slack-jira-bot.svg?branch=travis)](https://travis-ci.org/meanbee/slack-jira-bot)

A killer feature of the integration between Hipchat and Jira is the issue expansion.  Whenever a Jira issue is mention in the chat, the Jira integration would pop up some high level information about the issue and a link.

![](https://kibako-dev.s3.amazonaws.com/kibako/D4C2CE56-D016-4F94-B416-3BB91B93AD58/ScreenShot2015-09-28at18.19.08.png)

With the Jira integration in Slack being a bit light, we decided to implement a simple bot using the [Slack RTM API](https://api.slack.com/rtm):

![](https://kibako-dev.s3.amazonaws.com/kibako/32F4EE67-C0CB-4C02-BA84-AD86DF9082D9/ScreenShot2015-09-28at18.24.12.png)

# Installation

## From Source

    go get github.com/nlopes/slack
    go get github.com/plouc/go-jira-client
    go get github.com/meanbee/slack-jira-bot
    
    cd $GOPATH/github.com/meanbee/slack-jira-bot
    go install
    
    $GOPATH/bin/jira-bot
    
## Docker Image

    docker pull quay.io/meanbee/slack-jira-bot
    
# Configuration

The configuration is run of environment variables:

* `SLACK_API_KEY`
* `JIRA_BASEURL`, e.g. `https://yourcompany.atlassian.net`
* `JIRA_USERNAME`
* `JIRA_PASSWORD`