# learn-meteor
Learn about meteor

# Install
- Install
  - https://meteor.com

# Commands
- **Create** _project_
```
meteor create projectName
```
- **Run** _project_
```
meteor
```
- **Open** databse _mongo_
```
meteor mongo
```
- **Add** _plugin_
```
meteor add pluginName
```
- **List** _plugins_ added
```
meteor list
```
- **Remove** _plugins_ added
```
meteor remove pluginName
```
- **Update** _plugins_ added
```
meteor update
```
- **Added Deploy** _project_ || Push to **cloud** in meteor.com
```
meteor deploy name.meteor.com
```
- **Remove Deploy** _project_ || Remove to **cloud** in meteor.com
```
meteor deploy usedName.meteor.com --delete
```

# Libraries
- **Creating** _templates_ with **BLAZE**
```html
<template name="templateName"></template>
```
- **Using** _templates_ with **BLAZE**
```html
{{> templateName}}
```
- **Creating** _HELPERS_ with **BLAZE**
```js
Template.templateName.helpers({
  # ...
})
```
- **Creating** _EVENTS_ with **BLAZE**
```js
Template.templateName.events({
  "selector": function(event, template){}
})
```
- **Using** _accounts_ with **accounts-ui** || ui for _login/logout/register_
```html
{{> loginButtons}}
```
- **Verify logged** _accounts_ with **accounts-ui** || **verify** if _user_ is _logged_
```html
{{currentUser}}
```
- **Get id user logged** _accounts_ with **accounts-ui**
```js
this.userId
```
- **Creating** _Colletions_
```js
new Mongo.Colletions('colletionName')
```


# Methods
- **Loop** with **BLAZE**
```html
{{#each helperDefinition}}
  {{propertyName}}
{{/each}}
```
- **Conditions** with **BLAZE**
```html
{{#if}}
{{else}}
{{/if}}
```

- **Startup** run when server started
```js
Meteor.startup(function(){

  })
```
- **Publish** database _manually_ in **server**
```js
Meteor.publish("name", function(){
  # ...
  })
```
- **Subscribe** database _manually_ in **client**
```js
Meteor.subscribe("namePublish");
```
- **Creating** _Methods_
```js
Meteor.methods({
  # ...
  })
```
- **Call** _Methods_
```js
Meteor.call("methodName", params);
```




# Hierarchy
- All code in **client** and **server** brothers folders _run_ for _both_
- - client
- - server

# Observations

- Use for _SPA_
- **Meteor** use **MongoDb**
- **Motor** is _reactive_
- By Default **don't added** _tag_ <html></html> in **client** file _index.html_ | **Meteor** **added** _automatically_
- With **server** _started_ **meteor** _auto refresh changes in files_
- Use https://atmospherejs.com for _plugins_
- **Autopublish** is _actived__ by _default_ | _database_ **server** is _cloned automatically_ for **client**
```
meteor remove autopublish
```
