# Meteor stack

Build and deploy [Meteor](http://docs.meteor.com/) based apps.

## Install

Simply use the link below:

[![Fork on devo.ps](https://app.devo.ps/assets/images/fork.png)](https://app.devo.ps/#/fork?git_url=https://github.com/devops-community/meteor.git)

Once you've forked the repository, open it in devo.ps and you will be prompted for a few settings, including the Git URL for the code of your application, the names of your application and database.

To deploy your app, you will need to navigate to the tasks page of the repo and run the task manually (click on "play" icon, right of the "Build Meteor app" task).

## What's in the box?

This setup contains one server (`nodes/meteor.yml`) with **Node.js**, **Meteor**, **MongoDB** and **Nginx**

We have included several tasks to get you started quickly.

First of all there is the task (`tasks/build-meteor.yml`) that can be executed and will deploy your Meteor app and uses Supervisord to ensure your app is automatically (re)started when necessary. It also contains an example to setup webhooks for automatic app deployment.

In addition there is the task (`tasks/backup-meteor.yml`) that saves a backup of your MongoDB database and Meteor app in folders organised by date. The server (`nodes/meteor.yml`) contains an example on how to setup a similar service but only storing the latest (daily) backup.

Feel free to extend the tasks to install any kind of Meteor app! Checkout the [gh-pages builder](https://github.com/devops-community/gh-pages) for some examples.

The current repo provides a very simple setup. Hack at will!

## Questions?

If you have any question, come ask us on the [devo.ps chat](https://www.hipchat.com/gyHEHtsXZ) or shoot us an email at [help@devo.ps](mailto:help@devo.ps) (though, you should really just [ask us in the chat](https://www.hipchat.com/gyHEHtsXZ)).

# Reference

- [Nodes in devo.ps](http://docs.devo.ps/manual/nodes)
- [Tasks in devo.ps](http://docs.devo.ps/manual/tasks)

- [Backups in devo.ps](http://docs.devo.ps/services/backup/)
- [Nginx in devo.ps](http://docs.devo.ps/services/nginx/)
- [MongoDB in devo.ps](http://docs.devo.ps/services/mongodb/)
- [Supervisord in devo.ps](http://docs.devo.ps/services/supervisord/)
