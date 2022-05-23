# rnAwsAmplifyAuth

Setting up AWS Amplify
In order to use Amplify, you first need to create an AWS Account and have the Amplify CLI installed. Open a terminal and paste the code below to install the Amplify CLI.

Please note, that the following settings are not project-specific settings. That’s why we install the Amplify CLI globally on our machine.

`npm install -g @aws-amplify/cli`
After a successful installation of the Amplify CLI, run the following code to configure the CLI.
`amplify configure`

This interactive CLI command requires your input at two steps before it completes successfully. These steps are:

Authenticating your AWS account
Adding an identity and access management (IAM) user
When creating a user, be sure to create a user with AdministratorAccess to AWS services such as Amplify, Cognito, and Cloudfront. This is necessary for:

Specifying an AWS region
Adding the accessKeyId and the secretAccessKey of the user created
Adding an AWS profile

Navigate to the React Native application directory and run this command:

amplify init
Running the Amplify init command
You’ll be prompted to specify the following:

Name of the project
Name of the environment — I’d recommend sticking with the default dev since we are in a development environment (to choose the default option, press enter)
Your default editor of choice
The type of app you’re building (JavaScript)
The JavaScript framework you’re using (React Native)
Source directory path (press enter to choose the default root directory)
Distribution directory path (press enter to choose the default root directory)
Build command (press enter to choose the default command)
Start command (press enter to choose the default command)
Whether you want to use an AWS Profile (input Yes and press enter)
If yes, which profile you want to use
Upon completion of this form:

A folder called amplify is created in your applications root directory to store the backend configuration of your application, such as authentication
A file called aws-exports.js is created in the source directory path we specified when initializing Amplify. This file contains the information for the services you create with Amplify
The .gitignore file is modified to include files and folders generated by Amplify that shouldn’t be added to your Git repository
A cloud project is generated in the AWS Amplify Console. You can access it anytime by running amplify console