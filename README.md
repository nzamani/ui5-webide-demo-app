# ui5-webide-demo-app

This is just a demo project to illustrate how smoothly you can implement a ui5 app which uses an custom ui5 library using the SAP Web IDE Full-Stack.

# Links
TODO

# Checknig the App Index (after deployment)

1. After deployment to SAPCP check the App Index for each of the deployed projects, i.e.:
    - nabi.sample.ui5app
	    - https://flpnwc-p123456trial.dispatcher.hana.ondemand.com/sap/bc/ui2/app_index/ui5_app_info?id=nabi.sample.ui5app
		- https://flpportal-p123456trial.dispatcher.hanatrial.ondemand.com/sap/bc/ui2/app_index/ui5_app_info?id=nabi.sample.ui5app
		- https://flpnwc-p123456trial.dispatcher.hana.ondemand.com/sap/bc/ui2/app_index/ui5_app_info_json?id=nabi.sample.ui5app


	
	**FYI**: The `id` parameter is the corresponding SAPUI5 Component ID, i.e. try `sap.m` to see how a correct result should look like and compare it with the result of your own component.

1. What about the ABAP App Index?

Yes, there is also an App Index in ABAP. In fact, you only need to replace the host etc so that the URLs above point to your ABAP server, i.e.:

- https://abap.mycompany.com/sap/bc/ui2/app_index/ui5_app_info?id=nabi.sample.ui5app
- https://abap.mycompany.com/sap/bc/ui2/app_index/ui5_app_info_json?id=nabi.sample.ui5app

As you can see, that works because paths (i.e. /sap/bc/ui2/app_index/ui5_app_info_json) are the same on both ABAP and SAPCP.

# Local Build

1. Clone repo and change directory
    `git clone https://github.com/nzamani/ui5-webide-demo-app.git`
    `cd ui5-webide-demo-app`

1. Add SAP's NPM package registry (if you haven't already)
    - Local: `npm config set @sap:registry https://npm.sap.com`
	- Global: `npm config --global set @sap:registry https://npm.sap.com`

1. Install NPM Dependencies and build library
    - `npm install`
	- `grunt`
	- check the dist folder
