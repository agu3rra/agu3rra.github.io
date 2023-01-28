# Authentication using a `.netrc` file

There's many different ways to setup authentication on [GIT](https://git-scm.com/): [SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh) and [personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) when setting up a git remote are pretty straightforward, but my preferred one is using a `.netrc` file.
It works pretty much the same whether you're setting up your local workstation or a CICD pipeline somewhere like [Jenkins](https://www.jenkins.io/) or [AzureDevOps](https://azure.microsoft.com/pt-br/products/devops) and it also works for fetching [Golang](https://go.dev/) dependencies which rely on `git` (when using `go get`).

## The concept

The first time I stumbled upon `.netrc` was in [this documentation by IBM](https://www.ibm.com/docs/en/zos/2.1.0?topic=ftp-netrc-data-set). It consists of a specific file (yes, `.netrc`) which resides in the `$HOME` directory of a [Unix](https://en.wikipedia.org/wiki/Unix) system and allows the computer to authenticate to different machine [hosts](https://en.wikipedia.org/wiki/Host_(network)) for a variety of services (e.g.: git, ftp, etc.).

!!! tip "Added bonus!"
    You can setup access to multiple hosts using different accounts.

## on Unix

1. Open a [terminal](https://en.wikipedia.org/wiki/Unix_shell).
1. Navigate to your `$HOME` folder by `$ cd $HOME` or `$ cd ~`
1. Create a `.netrc` file there with the following contents (one line per host).
```
machine mvs1.tcp.raleigh.ibm.com login tonystark password ironman
machine 9.67.112.25 login tonystark password foobar
machine github.com login <yourId> password <yourPersonalAccessToken>
machine github.acme.com login <yourId> password <yourPersonalAccessToken>
```
1. DONE! Now the terminal is *"aware"* of which credentials to use where for different network services.

As you can see a host can be a DNS name entry, IPv4 or IPv6 address. One special thing about GitHub is that you should set it up using a token instead of you regular GitHub account password.

!!! question "Where do I get a GitHub token?"
    GitHub shows you the steps on [this documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).

!!! danger "Warning"
    **Treat your access tokens like passwords.**
    Don't ever commit them to source control or share them.
    If that happens rotate them immediatelly.
    Also consider using more selective token scopes instead of granting tokens access to everything.
    [GitHub](https://github.com) allows you to do that via [OAuth scopes](https://oauth.net/2/scope/).

## on Windows

!!! quote "Oh, so you're running Windows? Fear not, we've got you covered!"

As windows doesn't have an exact `$HOME` pointing to what it considers a user's `HOME` folder, here's how you can create `.netrc`:

1. Open a command prompt or PowerShell terminal.
1. setup `HOME` to point to Windows' version of it by running `setx HOME %USERPROFILE%`.
1. run `echo %HOME%` and verify it points to the current user's `HOME` folder (e.g.: `C:\Users\YOURNAME`).
1. Create a `_netrc` instead of a `.netrc` file same as on step #3 for [unix](#on-unix).
