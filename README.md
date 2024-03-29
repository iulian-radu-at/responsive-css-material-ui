# responsive-css-material-ui ![Weekly downloads](https://img.shields.io/npm/dw/responsive-css-material-ui 'Weekly downloads')

A material-ui component which applies different CSS to a child component based on the page's current width (based on material-ui defined breakpoints).

The order of breakpoints: xs, sm, md, lg, xl. You can find [here](https://material-ui.com/customization/breakpoints/#breakpoints) the values defined currently by material-ui for these breakpoints.

---

## Demo

You can access the storybook for this component [here](https://iulian-radu-at.github.io/responsive-css-material-ui/).

## Props

The component accepts the props defined bellow in the table.

### Props accepted by ResponsiveCssMaterialUi

| Name | Type          | Required | Default   | Description                                                                      |
| ---- | ------------- | -------- | --------- | -------------------------------------------------------------------------------- |
| lg   | CSSProperties | no       | undefined | CSS used for the lg breakpoint and wider screens (if not overridden)             |
| md   | CSSProperties | no       | undefined | CSS used for the md breakpoint and wider screens (if not overridden)             |
| sm   | CSSProperties | no       | undefined | CSS used for the sm breakpoint and wider screens (if not overridden)             |
| xl   | CSSProperties | no       | undefined | CSS used for the xl breakpoint and wider screens (if not overridden)             |
| xs   | CSSProperties | no       | undefined | CSS used for the xs breakpoint and bellow, and wider screens (if not overridden) |

---

There must be only one child otherwise an exception is triggered.

## Versions

| ResponsiveCssMaterialUi _uses_ | Material-ui |      React       |
| -----------------------------: | :---------: | :--------------: |
|                          1.0.x |    3.9.3    |      16.8.6      |
|                          2.0.x |    4.0.2    |      16.8.6      |
|                          2.1.x |    4.2.0    |      16.8.6      |
|                          2.2.x |    4.2.1    |      16.8.6      |
|                          2.3.x |    4.3.3    |      16.9.0      |
|                          2.4.x |    4.9.0    |      16.9.0      |
|                          2.5.x |    4.9.7    |      16.9.0      |
|                          2.6.x |   4.10.2    |      16.9.0      |
|                          2.7.x |   4.11.0    |      16.9.0      |
|                          2.8.x |   4.11.3    | 16.9.0 or 17.0.0 |
|                          2.9.x |   4.12.3    | 16.9.0 or 17.0.0 |
|                          3.0.x |   5.10.17   |      18.0.0      |
|                          3.1.x |   5.14.20   |      18.0.0      |

### About versioning schema used for ResponsiveCssMaterialUi

- Major - it will be increased if the major version of the dependat package changes or there are breaking changes in the code of ResponsiveCssMaterialUi
- Minor - it will be increased if no major version of the dependat package changes, but there are changes of the minor or patch versions of it
- Patch - it will be increased if there are no changes of the dependat packages, but there are non breaking changes in the code of ResponsiveCssMaterialUi

---

## Example

Displaying a div aligned differently based on the current window size:

```js
import * as React from 'react';
import ResponsiveCssMaterialUi from 'responsive-css-material-ui';

class App extends React.Component {
  render() {
    var xs = { textAlign: 'center' };
    var md = { textAlign: 'left' };
    var lg = { textAlign: 'right' };
    var style = { color: 'gray' };

    return (
      <div className="App">
        <ResponsiveCssMaterialUi xs={xs} md={md} lg={lg}>
          <div style={style}>Text</div>
        </ResponsiveCssMaterialUi>
      </div>
    );
  }
}

export default App;
```

---

## Changelog

### 1.0.0

- responsive-css-material-ui is made publicly available

### 1.0.1

- Corrected the way we decide which provided style is applied

### 1.0.2

- Removed the requirement to provide at least one prop

### 2.0.0

- Updated packages

### 2.1.0

- Updated packages

### 2.2.0

- Added a storybook
- Updated packages

### 2.2.1

- Added a prop debug for an easier development

### 2.3.0

- Updated packages

### 2.4.0

- Updated packages

### 2.5.0

- Updated packages
- Moved from npm to yarn

### 2.6.0

- Updated packages

### 2.7.0

- Updated packages

### 2.7.1

- Fixed crash produced by "export \* from"

### 2.8.0

- Accepting React 17 as peerDependencies
- Fixed security warnings

### 2.9.0

- Updated the packages

### 3.0.0

- Migrated to material-ui 5
- Supports minimum React 18

### 3.1.0

- Updated the packages

### 3.1.1

- Fixed bundled lib
