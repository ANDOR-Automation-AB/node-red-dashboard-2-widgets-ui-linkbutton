# UI Linkbutton Widget

[![GitHub](https://img.shields.io/badge/GitHub-gray?style=flat-square&logo=github&logoColor=white&label=)](https://github.com/ANDOR-Automation-AB/node-red-dashboard-2-widgets-ui-linkbutton)
[![npm](https://img.shields.io/badge/npm-gray?style=flat-square&logo=npm&logoColor=white&label=)](https://www.npmjs.com/package/@andor-automation/node-red-dashboard-2-widgets-ui-linkbutton)
![GitHub last commit](https://img.shields.io/github/last-commit/ANDOR-Automation-AB/node-red-dashboard-2-widgets-ui-linkbutton?color=gray)
[![npm version](https://img.shields.io/npm/v/@andor-automation/node-red-dashboard-2-widgets-ui-linkbutton.svg)](https://www.npmjs.com/package/@andor-automation/node-red-dashboard-2-widgets-ui-linkbutton)
[![npm downloads](https://img.shields.io/npm/dt/@andor-automation/node-red-dashboard-2-widgets-ui-linkbutton.svg)](https://www.npmjs.com/package/@andor-automation/node-red-dashboard-2-widgets-ui-linkbutton)
[![License](https://img.shields.io/npm/l/@andor-automation/node-red-dashboard-2-widgets-ui-linkbutton.svg)](https://github.com/ANDOR-Automation-AB/node-red-dashboard-2-widgets-ui-linkbutton/blob/main/LICENSE)

This widget provides options to open an url target in a new tab by pressing a button or loads the target embedded

## Version history

### 1.0.0
- Initial release.

## Install or Update

Make sure you install this widget inside your `.node-red` directory.
```
cd ~/.node-red
```

Install this widget in your `~/.node-red` folder by using the following command
```
npm i @andor-automation/node-red-dashboard-2-widgets-ui-linkbutton
```

## Properties

**Text**  
Label shown on the button.

**URL**  
Target address.

- Absolute e.g. `https://example.com/page`
- Relative

When using a relative URL, the file is served from the directory configured as
`httpStatic` in your Node-RED `settings.js`. Example: `httpStatic: '/var/local/'`.

A relative URL like /manuals/guide.pdf will resolve to http://<dashboard-host>:<port>/manuals/guide.pdf  
Files must exist under the configured static directory for the link or embedded view to load correctly.

**New tab**  
Opens the target in a new browser tab.

**Embedded**  
Replaces the button with an iframe that loads the target directly.