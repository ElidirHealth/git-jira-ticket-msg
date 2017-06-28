# Require JIRA issue ref in every commit message

## Setup

    git clone git://github.com/elidirhealth/git-jira-ticket-msg.git
    ln -vis `pwd`/git-jira-ticket-msg/commit-msg My-Project/.git/hooks
    cd My-Project
    git config --add jira.project MYPROJ
    git config --add jira.project MYPROJ2

## Global Config

    git config --add --global jira.project MYPROJ
    git config --add --global jira.project MYPROJ2

## Usage

#### Hack hack hack...

    git commit -am 'test'
    
    Aborted! Your commit message's first line must reference a ticket from projects MYPROJ or MYPROJ2

    > git commit -am 'add widget MYPROJ-1'
    [master 981b439] add widget MYPROJ-1

#### Hack hack hack...

    > git commit -am 'fix gizmo ALTPROJ-5'
    [master 459ec03] fix gizmo ALTPROJ-5

