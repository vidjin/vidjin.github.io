Angular 4 is the latest version of the angular. To start and check whether you have all the resources ready to give a try, this basic blog will help you install angular and related stuff (for Windows). so let's begin!


Open the command prompt and begin.
Installation: 
1. Check for  node.js existence by executing this command:
```
node -v 
```
if the result from the previous command says 'unrecognized command' then it means we need to install the node.js also, which can be done by downloading it from their website. 

2. Check for the angular installation:
```
ng -v
```
if the result from this command says 'unrecognized command' then we need to execute the follwoing command to get it installed. 
```
npm install -g@angular/cli
```
After installation is done, we can create test it for default and basic application.

1. In the command prompt, execute
```
ng new basic-app
```

2. Now to enter into app directory, 
```
cd basic-app
```

3. Install TypeScipt by executing following command
```
npm install typescript --save
```
it will install the latest version of the typescript. If you want to install any specific version say 2.5.6
npm install typescript@2.5.6 --save

4. To launch the app, execute
```
ng -serve
```
5. Check your basic app in the browser at http://localhost:4200
