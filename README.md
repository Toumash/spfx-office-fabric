## Demo Spfx Sharepoint Online package with Office UI Fabric
![demo](https://user-images.githubusercontent.com/9840635/54468531-e2a5fa80-478d-11e9-8912-631a7cd90286.gif)
If you would just install spfx and `npm install office-ui-fabric-react` it wouldnt work.

This article explains everything http://www.dotnetmafia.com/blogs/dotnettipoftheday/archive/2019/03/14/spfx-1-8-now-support-office-fabric-react-6-156-0.aspx

## How to DIY!
1. Install a new spfx generetor for `yeoman` 
```shell
npm install -g @microsoft/generator-sharepoint
```
2. Install Office UI Fabric
```shell
npm install office-ui-fabric-react
```
3. In package.json change **@microsoft/rush-stack-compiler-2.7** into:
```
@microsoft/rush-stack-compiler-3.0": "0.5.9"
```
4. And then in tslint.config
```
"extends": "./node_modules/@microsoft/rush-stack-compiler-3.0/includes/tsconfig-web.json
```
5. Fabric components should work just fine!





### Building the code

```bash
git clone the repo
npm i
npm i -g gulp
gulp
```

This package produces the following:

* lib/* - intermediate-stage commonjs build artifacts
* dist/* - the bundled script, along with other resources
* deploy/* - all resources which should be uploaded to a CDN.

### Build options

gulp clean - TODO
gulp test - TODO
gulp serve - TODO
gulp bundle - TODO
gulp package-solution - TODO
