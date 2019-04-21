# ExtJs Package Open Tooling Package Wrapper for plyr

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Build Status](https://dev.azure.com/spmeesseman/extjs-pkg-plyr/_apis/build/status/spmeesseman.extjs-pkg-plyr?branchName=master)](https://dev.azure.com/spmeesseman/extjs-pkg-plyr/_build/latest?definitionId=2&branchName=master)
[![Known Vulnerabilities](https://snyk.io/test/github/spmeesseman/extjs-pkg-plyr/badge.svg)](https://snyk.io/test/github/spmeesseman/extjs-pkg-plyr)
[![Average time to resolve an issue](https://isitmaintained.com/badge/resolution/spmeesseman/extjs-pkg-plyr.svg)](https://isitmaintained.com/project/spmeesseman/extjs-pkg-plyr "Average time to resolve an issue")
[![Percentage of issues still open](https://isitmaintained.com/badge/open/spmeesseman/extjs-pkg-plyr.svg)](https://isitmaintained.com/project/spmeesseman/extjs-pkg-plyr "Percentage of issues still open") [![Greenkeeper badge](https://badges.greenkeeper.io/spmeesseman/extjs-pkg-plyr.svg)](https://greenkeeper.io/)

## Description

> This package provides an ExtJS package wrapper for the [plyr html5 media player](https://github.com/sampotts/plyr) by [Sam Potts](https://github.com/sampotts), available on [npmjs.org](https://www.npmjs.com/package/plyr).  The plyr package is used as a dependency and this package will include its distribution files into ExtJs client builds.

## Install

To install this package, run the following command:

    npm install extjs-pkg-plyr

## Usage

To include the package in an ExtJS application build, be sure to add the package name to the list of required packages in the app.json file:

    "requires": [
         "plyr",
        ...
    ]

For an open tooling build, also add the node_modules path to the workspace.json packages path array:

     "packages": {
        "dir": "...${package.dir}/node_modules/extjs-pkg-plyr"
    }

Simply include the control into any class file:

    require: [ 'Ext.plyr.Plyr' ],
    items: [
    {
        xtype: 'plyr',
        audioCtlListTags: 'download',
        currentTime: 0,
        url: 'https://www.mydomain.com/audio/blank.mp4',
        plyrLoaded: function()         // Optional callback
        {
            Utils.log('Loaded!!!');
        },
        plyrLog: function(msg, level)  // Optional callback
        {
            Utils.log(msg, level);
        }
    }]

## Feedback & Contributing

* Please report any bugs, suggestions or documentation requests via the
  [Issues](https://github.com/spmeesseman/extjs-pkg-tniymce/issues)
* Feel free to submit
  [pull requests](https://github.com/spmeesseman/extjs-pkg-tniymce/pulls)
* [Contributors](https://github.com/spmeesseman/extjs-pkg-tniymce/graphs/contributors)

## Builds by spmeesseman

|Package|Use Case|Repository|Marketplace|
|-|-|-|-|
|conventional-changelog-spm|Semantic-Release|[GitHub](https://github.com/spmeesseman/conventional-changelog-spm)|[Npmjs.org Registry](https://www.npmjs.com/package/conventional-changelog-spm)|
|extjs-pkg-plyr|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-pkg-plyr)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-pkg-plyr)|
|extjs-pkg-tinymce|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-pkg-tinymce)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-pkg-tinymce)|
|extjs-pkg-websocket|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-pkg-websocket)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-pkg-websocket)|
|extjs-pkg-webworker|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-pkg-webworker)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-pkg-webworker)|
|extjs-server-net|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-server-net)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-server-net)|
|extjs-theme-graphite-small|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-theme-graphite-small)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-theme-graphite-small)|
|extjs-theme-amethyst|ExtJS Open Tooling|[GitHub](https://github.com/spmeesseman/extjs-theme-amethyst)|[Npmjs.org Registry](https://www.npmjs.com/package/extjs-theme-amethyst)|
|svn-scm-ext|Visual Studio Code|[GitHub](https://github.com/spmeesseman/svn-scm-ext)|[Visual Studio Marketplace](https://marketplace.visualstudio.com/itemdetails?itemName=spmeesseman.svn-scm-ext)|
|vscode-taskexplorer|Visual Studio Code|[GitHub](https://github.com/spmeesseman/vscode-taskexplorer)|[Visual Studio Marketplace](https://marketplace.visualstudio.com/itemdetails?itemName=spmeesseman.vscode-taskexplorer)|
|vscode-vslauncher|Visual Studio Code|[GitHub](https://github.com/spmeesseman/vscode-vslauncher)|[Visual Studio Marketplace](https://marketplace.visualstudio.com/itemdetails?itemName=spmeesseman.vscode-vslauncher)|
