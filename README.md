# Angular Geographical Form
*Form created in angular to treat data according to country, state and city*

`geografia-brasileira-angularjs.js` é um controller em AngularJS que pode ser usado por todos para organizar dados geográficos Brasileiros inseridos por usuários. //`geografia-brasileira-angularJS.js` is an AngularJS controller that anyone can use to organize geographical data from Brazil inserted by users

##Como usar // How to use

1) Configure o angular na seção `<head>`: // Configure angular on your `<head>` section:
```html
<script type="text/javascript" src="angular/angular.js"></script>
```

2) Insira o arquivo `geografia-brasileira-angularjs.js` na seção '<head>': // Insert the `angular-geographical-form.js` file in the `<head>` section:
```html
<script type="text/javascript" src="geografia-brasileira-angularjs.js"></script>
```

3) Insira o controller com a expressão `ng-controller="GeografiaBrasileira"` onde você for usá-lo // Insert the controller with `ng-controller="GeografiaBrasileira"` expression where you're gonna use it

4) Crie três inputs `<select>` que receberão atributos da seguinte forma: // Create three ` <select>` input that receives the following attributes:
```html
<p>País/Country:</p><select ng-change="countryItemChanged()" ng-model="country" ng-options="o for o in countries"><option></option></select>
<p>Estado/State:</p><select ng-disabled="country != 'Brasil'" ng-change="stateItemChanged()" ng-model="state" ng-options="o for o in states"></select>
<p>Cidade/City:</p><select ng-disabled="country != 'Brasil'" ng-options="o for o in cities[indexOfState]" ng-model="city"></select>
```

5) Para imprimir os valores selecionados é só utilizar o ng-model que foi utilizado na parte 3) // To print the selected values you have only to use the right ng-model on part 3)
```html
<span>País/Country: {{country}} </span>
<span>Estado/State: {{state}} </span>
<span>Cidade/City: {{city}}</span>
```

6) Sinta-se convidado para dar feedback para qualquer upgrade/reportar bug // Feel free to give feedback for any upgrade/bug report:

##License

`geografia-brasileira-angularjs.js` is licensed under the MIT license: http://opensource.org/licenses/MIT
