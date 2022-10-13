# How To Install Node.js on Ubuntu 

Published on May 9, 2020 · Updated on August 10, 2021

* [Ubuntu](https://www.digitalocean.com/community/tags/ubuntu "Ubuntu")
* [JavaScript](https://www.digitalocean.com/community/tags/javascript "JavaScript")
* [Ubuntu 20.04](https://www.digitalocean.com/community/tags/ubuntu-20-04 "Ubuntu 20.04")
* [Node.js](https://www.digitalocean.com/community/tags/node-js "Node.js")
* [DigitalOcean App Platform](https://www.digitalocean.com/community/tags/digitalocean-app-platform "DigitalOcean App Platform")

By [Brian Boucheron](https://www.digitalocean.com/community/users/bboucheron) Developer and author at DigitalOcean. English![How To Install Node.js on Ubuntu 20.04](./How To Install Node.js on Ubuntu 20.04 _ DigitalOcean_files/oQQThbYvLztdoVJ7yWZcs77s "How To Install Node.js on Ubuntu 20.04")

##### Not using Ubuntu 20.04 ? Choose a different version or distribution.

Ubuntu 20.04 **  Introduction **

[Node.js](https://nodejs.org/) is a JavaScript runtime for server-side programming. It allows developers to create scalable backend functionality using JavaScript, a language many are already familiar with from browser-based web development.

In this guide, we will show you three different ways of getting Node.js installed on an Ubuntu 20.04 server:

* using `apt` to install the `nodejs` package from Ubuntu's default software repository
* using `apt` with an alternate PPA software repository to install specific versions of the `nodejs` package
* installing `nvm`, the Node Version Manager, and using it to install and manage multiple versions of Node.js

For many users, using `apt` with the default repo will be sufficient. If you need specific newer (or legacy) versions of Node, you should use the PPA repository. If you are actively developing Node applications and need to switch between `node` versions frequently, choose the `nvm` method.

## Prerequisites

This guide assumes that you are using Ubuntu 20.04. Before you begin, you should have a non- **root** user account with `sudo` privileges set up on your system. You can learn how to do this by following the [Ubuntu 20.04 initial server setup tutorial](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-20-04).

## Option 1 — Installing Node.js with Apt from the Default Repositories

Ubuntu 20.04 contains a version of Node.js in its default repositories that can be used to provide a consistent experience across multiple systems. At the time of writing, the version in the repositories is 10.19. This will not be the latest version, but it should be stable and sufficient for quick experimentation with the language.

**Warning:** the version of Node.js included with Ubuntu 20.04, version 10.19, is now unsupported and unmaintained. You should not use this version in production, and should refer to one of the other sections in this tutorial to install a more recent version of Node.

To get this version, you can use the `apt` package manager. Refresh your local package index first by typing:

```
<ol><li data-prefix="$"><span class="token function">sudo</span> <span class="token function">apt</span> update
</li></ol>
```

Then install Node.js:

```
<ol><li data-prefix="$"><span class="token function">sudo</span> <span class="token function">apt</span> <span class="token function">install</span> nodejs
</li></ol>
```

Check that the install was successful by querying `node` for its version number:

```
<ol><li data-prefix="$"><span class="token function">node</span> -v
</li></ol>
```

```
<div class="secondary-code-label" title="Output">Output</div>v10.19.0
```

If the package in the repositories suits your needs, this is all you need to do to get set up with Node.js. In most cases, you'll also want to also install `npm`, the Node.js package manager. You can do this by installing the `npm` package with `apt`:

```
<ol><li data-prefix="$"><span class="token function">sudo</span> <span class="token function">apt</span> <span class="token function">install</span> <span class="token function">npm</span>
</li></ol>
```

This will allow you to install modules and packages to use with Node.js.

At this point you have successfully installed Node.js and `npm` using `apt` and the default Ubuntu software repositories. The next section will show how to use an alternate repository to install different versions of Node.js.

## Option 2 — Installing Node.js with Apt Using a NodeSource PPA

To install a different version of Node.js, you can use a _PPA_ (personal package archive) maintained by NodeSource. These PPAs have more versions of Node.js available than the official Ubuntu repositories. Node.js v12, v14, and v16 are available as of the time of writing.

First, we will install the PPA in order to get access to its packages. From your home directory, use `curl` to retrieve the installation script for your preferred version, making sure to replace `<mark>16.x</mark>` with your preferred version string (if different).

```
<ol><li data-prefix="$"><span class="token builtin class-name">cd</span> ~
</li><li data-prefix="$"><span class="token function">curl</span> -sL https://deb.nodesource.com/setup_<mark>16.x</mark> -o /tmp/nodesource_setup.sh
</li></ol>
```

Refer to the [NodeSource documentation](https://github.com/nodesource/distributions/blob/master/README.md) for more information on the available versions.

Inspect the contents of the downloaded script with `nano` (or your preferred text editor):

```
<ol><li data-prefix="$"><span class="token function">nano</span> /tmp/nodesource_setup.sh
</li></ol>
```

When you are satisfied that the script is safe to run, exit your editor, then run the script with `sudo`:

```
<ol><li data-prefix="$"><span class="token function">sudo</span> <span class="token function">bash</span> /tmp/nodesource_setup.sh
</li></ol>
```

The PPA will be added to your configuration and your local package cache will be updated automatically. You can now install the Node.js package in the same way you did in the previous section:

```
<ol><li data-prefix="$"><span class="token function">sudo</span> <span class="token function">apt</span> <span class="token function">install</span> nodejs
</li></ol>
```

Verify that you've installed the new version by running `node` with the `-v` version flag:

```
<ol><li data-prefix="$"><span class="token function">node</span> -v
</li></ol>
```

```
<div class="secondary-code-label" title="Output">Output</div>v<mark>16.6.1</mark>
```

The NodeSource `nodejs` package contains both the `node` binary and `npm`, so you don't need to install `npm` separately.

At this point you have successfully installed Node.js and `npm` using `apt` and the NodeSource PPA. The next section will show how to use the Node Version Manager to install and manage multiple versions of Node.js.

## Option 3 — Installing Node Using the Node Version Manager

Another way of installing Node.js that is particularly flexible is to use nvm, the Node Version Manager. This piece of software allows you to install and maintain many different independent versions of Node.js, and their associated Node packages, at the same time.

To install NVM on your Ubuntu 20.04 machine, visit [the project's GitHub page](https://github.com/nvm-sh/nvm). Copy the `curl` command from the README file that displays on the main page. This will get you the most recent version of the installation script.

Before piping the command through to `bash`, it is always a good idea to audit the script to make sure it isn't doing anything you don't agree with. You can do that by removing the `| bash` segment at the end of the `curl` command:

```
<ol><li data-prefix="$"><span class="token function">curl</span> -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh
</li></ol>
```

Take a look and make sure you are comfortable with the changes it is making. When you are satisfied, run the command again with `| bash` appended at the end. The URL you use will change depending on the latest version of nvm, but as of right now, the script can be downloaded and executed by typing:

```
<ol><li data-prefix="$"><span class="token function">curl</span> -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh <span class="token operator">|</span> <span class="token function">bash</span>
</li></ol>
```

This will install the `nvm` script to your user account. To use it, you must first source your `.bashrc` file:

```
<ol><li data-prefix="$"><span class="token builtin class-name">source</span> ~/.bashrc
</li></ol>
```

Now, you can ask NVM which versions of Node are available:

```
<ol><li data-prefix="$">nvm list-remote
</li></ol>
```

```
<div class="secondary-code-label" title="Output">Output</div>. . .
       v14.16.0   (LTS: Fermium)
       v14.16.1   (LTS: Fermium)
       v14.17.0   (LTS: Fermium)
       v14.17.1   (LTS: Fermium)
       v14.17.2   (LTS: Fermium)
       v14.17.3   (LTS: Fermium)
       v14.17.4   (Latest LTS: Fermium)
        v15.0.0
        v15.0.1
        v15.1.0
        v15.2.0
        v15.2.1
        v15.3.0
        v15.4.0
        v15.5.0
        v15.5.1
        v15.6.0
        v15.7.0
        v15.8.0
        v15.9.0
       v15.10.0
       v15.11.0
       v15.12.0
       v15.13.0
       v15.14.0
        v16.0.0
        v16.1.0
        v16.2.0
```

It's a very long list! You can install a version of Node by typing any of the release versions you see. For instance, to get version v14.10.0, you can type:

```
<ol><li data-prefix="$">nvm <span class="token function">install</span> v14.10.0
</li></ol>
```

You can see the different versions you have installed by typing:

```
nvm list
```

```
<div class="secondary-code-label" title="Output">Output</div>->     v14.10.0
         system
default -> v14.17.4 (-> N/A)
iojs -> N/A (default)
unstable -> N/A (default)
node -> stable (-> v14.10.0) (default)
stable -> 14.10 (-> v14.10.0) (default))
. . .
```

This shows the currently active version on the first line (`-> v14.10.0`), followed by some named aliases and the versions that those aliases point to.

**Note:** if you also have a version of Node.js installed through `apt`, you may see a `system` entry here. You can always activate the system-installed version of Node using `nvm use system`.

Additionally, you'll see aliases for the various [long-term support (or LTS) releases of Node](https://nodejs.org/en/about/releases/):

```
<div class="secondary-code-label" title="Output">Output</div>. . .
lts/* -> lts/fermium (-> N/A)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.4 (-> N/A)
lts/fermium -> v14.17.4 (-> N/A)
```

We can install a release based on these aliases as well. For instance, to install the latest long-term support version, `fermium`, run the following:

```
<ol><li data-prefix="$">nvm <span class="token function">install</span> lts/fermium
</li></ol>
```

```
<div class="secondary-code-label" title="Output">Output</div>Downloading and installing node v14.17.4...
. . .
Now using node v14.17.4 (npm v6.14.14))
```

You can switch between installed versions with `nvm use`:

```
<ol><li data-prefix="$">nvm use v14.10.0
</li></ol>
```

```
<div class="secondary-code-label" title="Output">Output</div>Now using node v14.10.0 (npm v6.14.8)
```

You can verify that the install was successful using the same technique from the other sections, by typing:

```command
node -v
```

```
<div class="secondary-code-label" title="Output">Output</div>v14.10.0
```

The correct version of Node is installed on our machine as we expected. A compatible version of `npm` is also available.

## Conclusion

There are a quite a few ways to get up and running with Node.js on your Ubuntu 20.04 server. Your circumstances will dictate which of the above methods is best for your needs. While using the packaged version in Ubuntu's repository is the easiest method, using `nvm` or a NodeSource PPA offers additional flexibility.

For more information on programming with Node.js, please refer to our tutorial series [How To Code in Node.js](https://www.digitalocean.com/community/tutorial_series/how-to-code-in-node-js).
[Next in series: How To Install Node.js on CentOS 8 ->](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-centos-8)

***


