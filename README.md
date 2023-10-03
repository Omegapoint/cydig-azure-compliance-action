
[![OP Compliance Dashboard](https://img.shields.io/badge/OP%20Compliance%20Dashboard-click%20here-blue)](https://cydig.omegapoint.cloud/cydig)<br/><br/>
![Timestamp](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3Dtimestamp)<br/><br/>
![threatModelingDate](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DthreatModelingDate)<br/>
![numberOfReviewers](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DnumberOfReviewers)<br/>
[![secureScore](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DsecureScore)](https://portal.azure.com/#view/Microsoft_Azure_Security/RecommendationsBladeV2/subscriptionIds~/%5B%2215c6235f-9e0f-4073-baf4-4fd0a7913d76%22%5D/source/SecurityPosture_ViewRecommendation)<br/>
[![allowedLocationPolicy](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DallowedLocationPolicy)](https://portal.azure.com/#view/Microsoft_Azure_Policy/PolicyMenuBlade/~/Compliance)<br/>
![pentestDate](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DpentestDate)<br/>
![numberOfDeployedVMs](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DnumberOfDeployedVMs)<br/>
![usersInProduction](https://img.shields.io/endpoint?url=https%3A%2F%2Ffunc-cydig-comp-state-prod.azurewebsites.net%2Fapi%2FReadToReadme%3Fcode%3DxaEvCDsaK01y2Z6SBivwOKndN4o915lpOTt1VkmULgsxgsjkml7u1DOhgULzmAPX%26teamName%3DCyDig%26teamProjectName%3DCyDig%26codeRepositoryName%3Dcydig-azure-compliance-action%26stateType%3DusersInProduction)<br/>


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

By first running `npm install` in the root you get the linting and format rules downloaded. So, every time you make a commit, a pre-hook will run to validate the rules. If there are any violation you will se an error or a warning in the terminal. Read more [here](/LinitingAndFormat.md). To fix format warnings run the following command from the **root**:

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

If you don't have at least 1 test in the ```test``` folder, the workflow won't work.

6. If necessary, add input parameter in ```action.yml```, if it is needed for the control.

7. When pushing the code the repository the workflow will build and push your code to the repository.

*For more information about developing in the CyDig project, please go to the [Wiki](https://dev.azure.com/CyDig/CyDig/_wiki/wikis/CyDig.wiki/5/Att-jobba-i-CyDig)*