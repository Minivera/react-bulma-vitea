# React vitae Bulma theme

![npm](https://img.shields.io/npm/v/react-vitae-bulma-theme.svg) ![npm bundle size](https://img.shields.io/bundlephobia/minzip/react-vitae-bulma-theme.svg)

`react-vitae-bulma-theme` is the Bulma theme for [react-vitae](https://github.com/Minivera/react-vitae).

## Installation

You can install `react-vitae-bulma-theme` with NPM or Yarn.

`npm install --save react-vitae bloomer react-vitae-bulma-theme` or `yarn add react-vitae bloomer react-vitae-bulma-theme`

## Peer dependencies

`react-vitae-bulma-theme` requires an installation of the latest version of `react-vitae` and the [Bloomer framework](https://bloomer.js.org/#/).

## Usage

`react-vitae-bulma-theme` includes a main component to quickly create your resume and a set of smaller components to allow you to customize the resume.

### The `Resume` component

The `Resume` component is a ready made page that will build the entire resume from the valid resume.json file provided to it. It uses the various components exported by this package to create the resume.

```jsx harmony
import { Resume } from 'react-vitae-bulma-theme';

const App = () => <Resume resume={json - resume} />;
```

### Individual components

The package exports individual components used as the building blocks for the main `Resume` component, feel free to import them. They need to be added inside of a `ResumeProvider` from `react-vitae`.

```jsx harmony
import React from 'react';
import { ResumeProvider } from 'react-vitae';
export {
  AwardsList,
  BasicsSection,
  EducationList,
  InterestsList,
  LanguagesList,
  ProjectsList,
  PublicationsList,
  References,
  Skills,
  VolunteerList,
  WorkList,
} from 'react-vitae-bulma-theme';

export const App = () => (
  <ResumeProvider resume={resume}>{/* Include any of hte imported components here */}</ResumeProvider>
);
```

## Development

### Installation

The installation of dependencies is made from the monorepo's root using lerna, see the commands there for more information on dependencies.

### Demo Development Server

`npm start` will run a development server at [http://localhost:1234](http://localhost:1234) with hot module reloading.

### Running Lint

`npm lint` will run eslint in this package.

### Running Tests

`npm test` will run the tests in this packages.

### Building

`npm run build` will build the package and create the built files in the `dist` folder.

`npm run clean` will clean the package, removing the cache, `node_modules` and built resources.

### Publishing

Publishing is done automatically through travis.
