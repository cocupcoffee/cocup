# How we work

## Tools

[Waffle Board](https://waffle.io/cocupcoffee/cocup) Overview of all Cocup issues.
[![Waffle.io - Columns and their card count](https://badge.waffle.io/cocupcoffee/cocup.svg?columns=all)](https://waffle.io/cocupcoffee/cocup)


## Releases

[Cocup Web App](http://cocup-app.s3-website.eu-central-1.amazonaws.com/) on AWS S3

[API Backend](https://ave52krdnk.execute-api.eu-central-1.amazonaws.com/dev) on AWS Lambda

## Weekly meetings

Every monday after the standup meeting.

### Objectives

1. **Retrospective** We would like to hear what you worked on last week. What did you manage to build? What were your challanges?

2. **Evaluation** Is there unfinished work from the previous planning? Handle the leftover work accordingly.

3. **Planning** Tell the team about the objectives of the new week. Who builds what part of it.

## Development Workflow

We manage work to be done in Github issues under the respective projects. After each meeting the developers create issues describing the work to be done. Then labels are attached. The developer estimates the time it takes to solve the subject issue. 

__Size 0 - briefing__: for discussions about a problem to solve.

__Size 1 - small__: tasks that take 1-2 hours.

__Size 2 - medium__: tasks that take 3-4 hours (half a day).

__Size 3 - large__: tasks that take 7-8 hours (one day).

__Size 4 - too big__: tasks that take over a day. These need to be split up into smaller issues.

The priority label is attached after the Project Owner's estimation.

When an issue contains the `Status - workable` label it means that the developer can start working on solving this specific problem. Always the highest priority issues are picked first.

Each time you make a commit, reference the issue in the commit message like below. You can also add extra information to the message:

`git commit -m "#2 add login page"`

or 

`git commit -m "close #2"` when you want to close an issue.

This way we can see what certain commits are aiming to solve easily without having to go through the code in details. It also aims to help with debugging in the future.

## Labels

Clean all your labels:

`ghi label -l | sed "s/\'/\\\'/g" | xargs -I %lb sh -c 'ghi label -D "%lb"'`

Add the default labels to the project:

```sh
ghi label "Action - awaiting feed-back" -c 6EB82C
ghi label "Action - needs grooming"     -c 009800
ghi label "Prio 1 - must have"          -c E83D0F
ghi label "Prio 2 - should have"        -c EB6420
ghi label "Prio 3 - could have"         -c E8850F
ghi label "Prio 4 - won't have"         -c E8A80F
ghi label "Size 0 - Briefing"           -c C7DEF8
ghi label "Size 1 - small"              -c 20B4E5
ghi label "Size 2 - medium"             -c 208FE5
ghi label "Size 3 - large"              -c 0052CC
ghi label "Size 4 - too big"            -c 100B6B
ghi label "Status - duplicate"          -c 111111
ghi label "Status - to do"              -c EDEDED
ghi label "Status - in progress"        -c EDEDED
ghi label "Status - up next"            -c EEEEEE
```
