# coscale-vr
Proof of concept kubernetes monitoring in VR

![screenshot](https://raw.githubusercontent.com/lorgan3/coscale-vr/master/screenshot.png)

## Visualising your own cluster
A demo application on [CoScale](https://www.coscale.com) is used to get data from.
It is possible to visualise your own data, but requires a little bit of work:
1. Get an access token for your application, you can find it using your browser's dev tools or [the CoScale docs](http://docs.coscale.com/api/#!/Login/post_users_login).
2. (optional) Using this access token you can also get your metrics from [here](http://docs.coscale.com/api/#!/Metrics/post_app_appId_metrics). Look for 2 container metrics you want to visualise (ideally in %). The default visualisation uses `Docker container user mode cpu usage` and `Docker container free memory percentage`.
3. Navigate to where this project is hosted and add `?app=<app id>&cpu=<cpu metric id>&memory=<memory metric id>` to the url. The webpage will show a popup asking for your access token and when entered correctly your cluster will be visualised.

## Made with [Aframe](https://aframe.io/)
