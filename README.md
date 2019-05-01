## Linux Terminal Controlled Slack WebHook
This is a simple use case of slack webhooks. Slack webhooks can be configured to send messages when some events occur, i.e. we trigger the hook and the hook sends the message to slack channel configured.

I have set up a workspace (for my own personal experimentations) and created a webhook which is a fairly simple process. Web Hook can be called via HTTP POST call with required message. I have configured this in a simple python script (gist below) which works two ways:

1. By providing command line arguments: `slackme this is some random message from my linux console `
2. As Linux piping of command output: Eg: Let's say you want to send the process stats (for java programs) to your slack channel: `ps -ef | grep java| slackme`

Following is a working demonstration of how I have put it to use for my personal tasks.

![slack-me in action](https://sudipbhandari126.github.io/resources/slack-me.gif "slack-me in action")

I can think of lot more applications for this sort of scripts mainly in network and system administration. Instead of traditional mails we can pipe the output of various commands (cron jobs to `slackme`)


## Instruction
1. Replace web_hook with your own slack web hook
2. make `slackme` executabe `sudo chmod +x slackme`

