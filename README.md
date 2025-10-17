# CyDig Azure Compliance Action

This repository contains a action with azure compliance controls.

## Azure Compliance Controls

The azure compliance controls that are currently available are listed below.

* Azure Secure Score
* Number of users in a subscription (production) in Azure
* Number of deployed VMs in Azure
* Azure resources in EU only

## Development on already existing or new azure control

1. To start development, create a branch named **feature/your-branch-name**.

2. Run the command below from the root.

```bash
npm install
```

By first running npm install in the root you get the linting and format dependencies downloaded. To enable so that every time you make a commit, a pre-hook will run to validate the rules read more [here](/LinitingAndFormat.md). To fix format warnings manually run the following command from the **root**:

```bash
npm run format:write
```

3. If you are developing a new control, create a new folder for your control in the ```src``` folder.

4. Start developing. To compile your code, run the following command:  

```bash
npm run build
```

5. To run the tests, run the following command:
```bash
npm run test
```

To generated test results in a XML-file, run the following command:

``` bash
npm run testScript
```

6. If necessary, add input parameter in ```action.yml```, if it is needed for the control.

7. When pushing the code the repository the workflow will build and push your code to the repository.

*For more information about developing in the CyDig project, please go to the [Wiki](https://dev.azure.com/CyDig/CyDig/_wiki/wikis/CyDig.wiki/5/Att-jobba-i-CyDig)*

## Creating a release for the action
At cydig, we follow [Semantic Versioning](https://semver.org/) for our action releases. Practically, this means that when you're developing and creating a pull request (PR), you can assign one of three labels to the PR: Major, Minor, or Patch. These labels correspond to version numbers in the format vX.Y.Z, where X is the major version, Y is the minor version, and Z is the patch version.For example, if you add the "Patch" label to your PR, and it's approved and merged, a workflow will automatically run to create a release for the action. Here's an illustration of how the version number would change before and after the PR:
* Version before PR: v1.0.1
* Version after PR: v1.0.2
