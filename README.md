# kandy-cpaas2-sample-2fa-node

This is an elementary login authentication use case of two-factor authentication via SMS or Email. The main focus of this application is to understand the 2FA flow.

## Development
These instructions will get you a copy of the project. Running on your local machine for development and testing purposes.

### Prerequisites
Your system should have the following installed to complete pass this project:
- [NodeJS](https://nodejs.org/en/) >= 10.15.0
- Chrome browser - Last 3 major version

### Setup
1. To setup the project repository, run these commands
```bash
git clone https://github.com/hclsampleapps/kandy-cpaas2-sample-2fa-node-red.git
cd kandy-cpaas2-sample-2fa-node-red
```
2. To install nodered, run these commands
```bash
npm install -g --unsafe-perm node-red
```

### Installation
1. To install dependencies, run
```bash
npm install @kandy-io/node-red-contrib-cpaas-sdk
```
2. To start the server, run
```bash
node-red
```

### Branching strategy
To learn about the branching strategy, contribution & coding conventions followed in the project. Please refer [GitFlow based branching strategy for your project repository](https://gist.github.com/ribbon-abku/10d3fc1cff5c35a2df401196678e258a)

## Usage
The application comprises of simple flows of send code and code verification.
- Open the localhost url in the browser. On the right side click on three bar menu and then click on import. Select the file `2FA.json` from the repository and then import.
- Click on `Deploy` for deployment of flow.
- Double click on `Send 2FA` node. Edit the `CPaaS Credentials`.
- Choose any `Authentication type` and enter the other fields. And then click on `Update` button.
- Choose the `method` verification type by email or sms. And enter the `Destination address` in case of sms. And in case of email enter the `Subject` of email also.
- Click on `Done` button.
- Click on`Inject` node of `Send 2FA` for send sms or email.
- Copy the both `codeId` from debug menu and `Verifaction Code` received at destination address.
- Double click on `Verify 2FA` node. Select the `CPaas Credentials` from the dropdown. Enter the `Code Id` and `Verification Code` from above step. Anc click on `Done` to setup the values.
- Click on `Inject` node of `Verify 2FA` for verification. Check the output in debug window.
