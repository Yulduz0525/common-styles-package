# general-styles

Why do we need to install this library?

If you need html and css codes written together using styled-component, responsive design, ready-made typographies, flexboxes, you can install and use this library.

## Installation

Install the package using npm:

```bash
npm install general-styles
```
### Importing Components

Import the `Row` and `Column` components from the package:

```typescript
import React from 'react';
import { Row, Column, mergeColors } from 'general-styles';
import colors from 'general-styles/constants/colors';
```

### Using the Components

Use the `Row` and `Column` components to create a flexible layout. You can also customize the colors by using the `mergeColors` function.

```typescript
import React from 'react';
import { Row, Column, mergeColors, H1, Paragraph, Underline, ButtonDefault, InputDefault,LabelLg, PlaceholderLg } from 'general-styles';

const userColors = {
  "primary-500": "#ff5733",
  "secondary-500": "#33c4ff",
  ...
};

const colors = mergeColors(userColors);

const App = () => (
  <Row backgroundColor="primary-500">
    <Column size={6} difference={2}>
      <H1>its a h1 tag</H1>
      <Paragraph>its a paragraph tag</Paragraph>
      <Underline>its a text underline</Underline>
      <ButtonDefault>its a button</ButtonDefault>
      <InputDefault>its a input</InputDefault>
      <LabelLg>its a label text</LabelLg>
      Content here
    </Column>
  </Row>
);

export default App;
```
#### Custom Colors

You can customize the colors used in the components by providing your own color values using the `mergeColors` function. This function takes an object with your custom colors and merges them with the default colors.

```typescript
import { mergeColors } from 'gcs-flexbox';

const userColors = {
  "primary-500": "#ff5733",
  "secondary-500": "#33c4ff",
  ...
};

const colors = mergeColors(userColors);
```

##### License

This project is licensed under the MIT License.

