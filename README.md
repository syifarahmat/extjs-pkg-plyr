# ExtJs Package Wrapper for plyr

[![perry-johnson](https://img.shields.io/badge/perry%20johnson-pja-blue.svg)](https://www.perryjohnson.com)
[![app-type](https://img.shields.io/badge/category-extjs%20web-blue.svg)](https://www.perryjohnson.com)
[![app-lang](https://img.shields.io/badge/language-c%23%20javascript-blue.svg)](https://www.perryjohnson.com)
[![app-publisher](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-app--publisher-e10000.svg)](https://github.com/perryjohnsoninc/app-publisher)

[![authors](https://img.shields.io/badge/authors-scott%20meesseman-6F02B5.svg?logo=visual%20studio%20code)](https://www.perryjohnson.com)
[![MantisBT issues open](https://app1.development.pjats.com/projects/plugins/ApiExtend/api/issues/countbadge/extjs-pkg-plyr/open)](https://app1.development.pjats.com/projects/set_project.php?project=extjs-pkg-plyr&make_default=no&ref=bug_report_page.php)
[![MantisBT issues closed](https://app1.development.pjats.com/projects/plugins/ApiExtend/api/issues/countbadge/extjs-pkg-plyr/closed)](https://app1.development.pjats.com/projects/set_project.php?project=app-publisher&make_default=no&ref=plugin.php?page=Releases/releases)
[![MantisBT version current](https://app1.development.pjats.com/projects/plugins/ApiExtend/api/versionbadge/extjs-pkg-plyr/current)](https://app1.development.pjats.com/projects/set_project.php?project=extjs-pkg-plyr&make_default=no&ref=plugin.php?page=Releases/releases)
[![MantisBT version next](https://app1.development.pjats.com/projects/plugins/ApiExtend/api/versionbadge/extjs-pkg-plyr/next)](https://app1.development.pjats.com/projects/set_project.php?project=extjs-pkg-plyr&make_default=no&ref=plugin.php?page=Releases/releases)

## Description

> This package provides an ExtJS package wrapper for the [plyr html5 media player](https://github.com/sampotts/plyr) by [Sam Potts](https://github.com/sampotts), available on [npmjs.org](https://www.npmjs.com/package/plyr).  The plyr package is used as a dependency and this package will include its distribution files into ExtJs client builds.

## Install

To install this package, run the following command:

    npm install @perryjohnson/extjs-pkg-plyr

## Usage

To include the package in an ExtJS application build, be sure to add the package name to the list of required packages in the app.json file:

    "requires": [
         "plyr",
        ...
    ]

For an open tooling build, also add the node_modules path to the workspace.json packages path array:

     "packages": {
        "dir": "...${package.dir}/node_modules/@perryjohnson/extjs-pkg-plyr"
    }

Simply include the control into any class file:

    require: [ 'Ext.ux.Plyr' ],
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
