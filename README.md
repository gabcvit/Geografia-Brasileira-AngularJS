# Angular Geographical Form
*Form created in angular to treat data according to country, state and city*

`angular-geographical-form.js` is an angular controller that anyone can use to organize geographical data inserted by users

##How to use

1) Configure angular on your `<head>` section:
```html
<script type="text/javascript" src="angular/angular.js"></script>
```

2) Insert the `angular-geographical-form.js` file in the `<head>` section:
```html
<script type="text/javascript" src="angular-geographical-form.js"></script>
```

3) Create a ` <select>` input that receives the following attributes:
```html
<select ng-change="stateItemChanged()" ng-model="state" ng-options="o for o in states"></select>
```

4) Create another `<select>` input that receives the following attributes:
```html
<select ng-model="city" ng-options="o for o in cities[indexOfState]"></select>
```

5) Now to insert this form in your project you only have to change the `ng-model` attribute on your `<select>` tag.

##License

`angular-geographical-form.js` is licensed under the MIT license: http://opensource.org/licenses/MIT
