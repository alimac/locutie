# Locutie
An experiment in IRC bot design using Node.js and OpenShift.

## Notes

Code based on [Building social IRC Bots with Node.js Part 1](https://www.openshift.com/blogs/building-social-irc-bots-with-nodejs-part-1) and
[Building Social IRC Bots with Node.js Part 2 - Leaderboards](https://www.openshift.com/blogs/building-social-irc-bots-with-nodejs-part-2). 

Instead of using `nodejs-0.6` I used the more recent version:
```
   rhc app create ircbot nodejs-0.10
```
The post also points to a [method](https://www.openshift.com/blogs/secret-free-source-on-paas) of setting environment variables via
`.bash_profile` file, which did not work well for me. I found a more recent 
post about [deploying Node.js apps on OpenShift](https://www.openshift.com/blogs/run-your-nodejs-projects-on-openshift-in-two-simple-steps) which used the following
method:
```
   rhc env set VAR=value
```
I added authentication for the bot based on the [node-irc API](https://node-irc.readthedocs.org/en/latest/API.html#client) docs.
