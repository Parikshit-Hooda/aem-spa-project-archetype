#set($hash = '#')
${hash} Angular App

This project was bootstrapped with the [Angular CLI](https://github.com/angular/angular-cli).

This application is built to consume the AEM model of a site. It will automatically generate the layout using the helper components from the [`@adobe/cq-angular-editable-components`](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) package.

${hash}${hash} Scripts

In the project directory, you can run the following commands:

${hash}${hash}${hash} `npm start`

Runs the app in development mode by proxying the JSON model from a local AEM instance running at http://localhost:4502. This assumes that the entire project has been deployed to AEM at least once (`mvn clean install -PautoInstallPackage`).

Your app can be viewed on http://localhost:4200/content/${projectName}/en/home.html and the page will reload if you make edits.

If you are getting errors related to CORS, you might want to configure AEM as follows:

1. Navigate to the Configuration Manager (http://localhost:4502/system/console/configMgr)
2. Open the configuration for "Adobe Granite Cross-Origin Resource Sharing Policy"
3. Create a new configuration with the following additional values:
   - Allowed Origins: http://localhost:4200
   - Supported Headers: Authorization
   - Allowed Methods: OPTIONS

${hash}${hash}${hash} `npm test`

Launches the Karma test runner. See the section about [running tests](https://angular.io/guide/testing) for more information.

${hash}${hash}${hash} `npm run test:debug`

Launches the Karma test runner in interactive watch mode.

${hash}${hash}${hash} `npm run e2e`

Executes the end-to-end tests using [Protractor](http://www.protractortest.org).

${hash}${hash}${hash} `npm run build`

Builds the app for production to the `build` folder. It bundles Angular in production mode and optimizes the build for the best performance. See the section about [deployment](https://angular.io/guide/deployment) for more information.

Furthermore, an AEM ClientLib is generated from the app using the [`aem-clientlib-generator`](https://github.com/wcm-io-frontend/aem-clientlib-generator) package.
