# WUPS Plugin Repo
This repository is used for hosting [Wii U Plugin System](https://github.com/Maschell/WiiUPluginSystem) plugins and files to be downloaded within the client.

## Viewing plugins
You can view plugin zips to download/update either in the the WUPS client app directly, or by downloading them directly from this repo. (gh-pages branch, under `zips` folder)

## Plugin Submission
To submit your own plugin, you can create a [pull request](/fortheusers/plugins/pulls) against master. It should be for your own folder within the `packages` folder. The folder should contain an info json file, your plugin, and any other files as they should be installed relative to the root of the SD. For instance, here are two plugins named `plugin1` and `plugin2`, and how they should be laid out in the `packages` folder:

```
.
└── packages
    ├── plugin1
    │   ├── external_folder
    │   │   └── data.cfg
    │   ├── info.json
    │   └── wiiu
    │       └── plugins
    │           └── plugin.wups
    └── plugin2
        ├── info.json
        └── wiiu
            └── plugins
                └── anotherplugin.wups
 ```
 
 If your plugin is simple, and does not require external files to be installed on the console, you can just submit the `.wups` file directly to a folder within `packages` and it will be fixed during the merge. Additionally, if you don't wish to create your own `info.json`, that can be auto-populated as well.
 
 After the PR is merged, a travis job will rebuild the main index, and your plugin update should immediately be available to users within the app.
