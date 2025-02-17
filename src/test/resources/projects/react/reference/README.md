# AEM SPA Project

**This is a single-page application (SPA) project generated from the [AEM SPA Project Archetype](https://github.com/adobe/aem-spa-project-archetype).**

## Modules

- **[`core`](./core/):** OSGi bundle containing Java classes (e.g. Sling models, servlets, business logic)
- **[`ui.apps`](./ui.apps):** AEM components with their scripts and dialog definitions
- **[`ui.content`](./ui.content/):**
  - [`ui.content/src/main/content/jcr_root/conf`](./ui.content/src/main/content/jcr_root/conf/): AEM content package with editable templates stored at `/conf`
  - [`ui.content/src/main/content/jcr_root/content`](./ui.content/src/main/content/jcr_root/content/): AEM content package containing sample content (for development purposes)
- **[`react-app`](./react-app/):** SPA source code
- **[`all`](./all/):** All-in-one package

## Usage

### Requirements

- Java 8 or higher
- Maven 3.5 or higher

### Building modules

To build all modules, run the following command **in the project root directory**:

```sh
mvn clean install
```

For example, to build your SPA and deploy it on a local AEM author instance, you can run:

```sh
mvn clean install -PautoInstallPackage
```

After deploying, you can view the sample content page in your browser: http://localhost:4502/content/editor.html/content/test-spa-react-project/en.html

### Maven profiles

- **`autoInstallBundle`**: Installs the `core` bundle with the `maven-sling-plugin` to the Felix console
- **`autoInstallPackage`**: Installs the `ui.content` and `ui.apps` content packages with the `content-package-maven-plugin` to the package manager of the default author instance.
- **`autoInstallPackagePublish`**: Installs `ui.content` and `ui.apps` on the default publish instance.

In the all-in-one package ([`all`](./all/) directory), there are additional profiles for packaging all dependencies into a single content package and installing everything on an existing AEM instance:

- **`autoInstallSinglePackage`**: Installs the all-in-one package to an existing AEM author instance
- **`autoInstallSinglePackagePublish`**: Installs the all-in-one package to an existing AEM publish instance

## Documentation

- [Framework setup](./react-app/README.md)
