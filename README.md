# Heroku Buildpack for Ghostscript

Currently installs Ghostscript 9.19 on Heroku Cedar.

## Install

    $ cd /path/to/your-app
    $ heroku buildpacks:add https://github.com/wesleycyu/heroku-buildpack-ghostscript.git

    # Push changes to deploy
    $ git push

    # This version of ghostscript will end up deployed at /app/vendor/gs/bin/gs
    # So you may want to set an environment variable to let your app know where it is. e.g.
    $ heroku config:set GS_PATH=/app/vendor/gs/bin/gs