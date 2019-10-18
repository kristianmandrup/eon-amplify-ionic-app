# E-ON demo

Demo app for E-ON to be used to show off new architecture with async conversational communication

## Technologies

- [AWS AmplifyJS](https://aws-amplify.github.io/)
- [Ionic with React](https://ionicframework.com/blog/announcing-ionic-react/)

## Get started

[Amplify Get started](https://aws-amplify.github.io/docs/)

Install amplify CLI

```sh
$ npm install -g @aws-amplify/cli
$ amplify configure
```

### Amplify React

[Amplify React](https://aws-amplify.github.io/docs/js/react)

```sh
$ amplify init
```

```sh
$ amplify add hosting
```

```sh
$ yarn add aws-amplify aws-amplify-react
```

## Authentication

[Add auth](https://aws-amplify.github.io/docs/js/react#add-auth)

Edit `./sjsrc/App.js` to include the Amplify library, configurations, and React HOC. Then, initialize the library as follows:

```js
import Amplify from "aws-amplify";
import awsconfig from "./aws-exports";
import { withAuthenticator } from "aws-amplify-react"; // or 'aws-amplify-react-native';

Amplify.configure(awsconfig);
```

Wrap the default `App` component using `withAuthenticator` at the bottom of the file as follows:

`export default withAuthenticator(App, true);`

You can now use `amplify publish` to build and publish your app again. This time you’ll be able to register a new user and sign in before opening the main application.
