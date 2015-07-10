# Use npm@3 on Azure Web Apps
The new version of everyone's favourite Node package manager, npm@3, contains two major improvements making the life of developers dramatically easier: Flat module installation and a multi-stage installer. If you somehow stumbled into this repository not knowing why you should use npm@3, [check out this blog post](http://felixrieseberg.com/npm-v3-is-out-and-its-a-really-big-deal-for-windows/).

### Regular Node.js Deployments
*To use npm@3 on Azure Websites for regular Node projects, copy `.deployment` and `deploy.sh` to your project's root folder.*

### Custom Deployments
To integrate npm@3 in your custom deployments, simply change your `deploy.sh` or `deploy.cmd` to use npm@3.1.0 as installed in `$PROGRAMFILES\npm\3.1.0`. For a deploy.sh, use for instance the following instruction:

```
NPM_CMD="\"$NODE_EXE\" \"$PROGRAMFILES\\npm\\3.1.0\\node_modules\\npm\\bin\\npm-cli.js\""
```

### There Be Dragons
Before you install npm@3 and use it in production, be warned that this is still beta software (as of July 2015), with potentially a bunch of breaking changes and unknown bugs. Obviously, the whole node community and npm are working hard to get it production-ready as quickly as possible. To quote npm: "During that time we will still be doing npm@2 releases, with npm@2 tagged as latest and next. We'll also be publishing new releases of npm@3 as npm@3.0-next and npm@3.0-latest alongside those versions until we're ready to switch everyone over to npm@3."