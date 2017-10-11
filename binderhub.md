Host a binderhub (https://github.com/jupyterhub/binderhub) at binder.surfsara.nl (for binder launcher) and hub.binder.surfsara.nl (for jupyter notebooks)

# Out of the box

The binder out of the box allow anonymous users to build and launch a repo (using https://github.com/binder-examples/requirements as example).

After filling form and pressing launch button the browser is redirected to
https://binder.surfsara.nl/v2/gh/binder-examples/requirements/master .

This url shows a build progress page, when build is completed it will redirect to a launched Jupyter notebook at https://hub.binder.surfsara.nl/user/binder-examples-requirements-bolz0rob/tree

The https://binder.surfsara.nl/v2/gh/binder-examples/requirements/master url is also used as badge for visitors.

During build an eventsource connection (aka server-sent events) to https://binder.surfsara.nl//build/gh/binder-examples/requirements/master is used to print the progress.

# Project enhancements

## Authenticated building

Only SURFConext authenticated users should be allowed to register/build a repo and anonymous users should only be able launch repos which have already have been registered and build.

### Solution

We could modify binderhub so that when a anonymous user visits https://binder.surfsara.nl/v2/gh/binder-examples/requirements/master
it checks if the repo has been build then launches it else a login is required to continue.
