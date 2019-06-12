# Homework 6 Template

## Getting started

1.  Fork a repository for yourself with the github `Fork` button.

1.  Clone your repository to your local machine.

1.  If command line utility `gcloud` is not available, download and install
    [Google Cloud SDK](https://cloud.google.com/sdk/docs/quickstarts) (Japanese
    guides evailable).

    -   Then install App Engine components for the programming language of your
        choice.
        -   Go: `gcloud components install app-engine-go`
        -   Python: `gcloud components install app-engine-python
            app-engine-python-extras`
    -   Run `gcloud init` to initialize the SDK and create a new Cloud Platform
        project. This newly created Cloud Platform project will allow you to try
        many Google Cloud Platform products, but we will only use Google App
        Engine for this homework.
    -   If you already have Google Cloud SDK installed, run `gcloud components
        update` to update to the latest version.

1.  Start a local App Engine server with `dev_appserver.py go/` or
    `dev_appserver.py python-flask/` (depending on whether you're using Go or
    Python).

1.  Add functionality and test your app by viewing the local instance at
    http://localhost:8080.

1.  Deploy your app to App Engine with `gcloud app deploy go/` or `gcloud app
    deploy python-flask/`.

    -   The first time you deploy an App Engine app to your Cloud Platform
        project, you will be asked to select a region for the location of your
        App Engine app. Select `asia-northeast1` (Tokyo), `asia-northeast2`
        (Osaka) or
        [a region](https://cloud.google.com/compute/docs/regions-zones/) that is
        close to you.
    -   Use `--version` flag to specify a version string manually, e.g. `gcloud
        app deploy python-flask/ --version=python-flask-20190612`.

1.  Test your app in production by accessing the target url shown in the command
    line console. To access a specific app version, use
    `https://{VERSION}-dot-{PROJECT_NAME}.appspot.com`, e.g.
    https://python-flask-20190612-dot-my-project-name.appspot.com.

1.  To stream production server logs in the command prompt console, run `gcloud
    app logs tail -s default`. You can also use
    [the web console](https://console.cloud.google.com/logs/viewer) to
    view/stream server logs for debugging and troubleshooting.

1.  `git add .` and `git commit` and `git push` to upload your changes to your
    GitHub repository.

1.  Send email to the STEP mailing list to show everyone your awesome app!

Feel free to repeat steps 4-10 as much as you like!
