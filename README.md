# Use-bootstrap-4-in-Angular-8
How to use bootstrap 4 in angular 8

OPTION-1

execute

npm install bootstrap@4 jquery --save
The JavaScript parts of Bootstrap are dependent on jQuery. So you need the jQuery JavaScript library file too.

"styles": [
    "src/styles.css","node_modules/bootstrap/dist/css/bootstrap.min.css"
],
"scripts": [
    "node_modules/jquery/dist/jquery.min.js",
    "node_modules/bootstrap/dist/js/bootstrap.min.js"
]
OPTION-2

ng-bootstrap It contains a set of native Angular directives based on Bootstrap’s markup and CSS. As a result, it's not dependent on jQuery or Bootstrap’s JavaScript

npm install --save @ng-bootstrap/ng-bootstrap
After Installation import it in your root module and register it in @NgModule imports` array

import {NgbModule} from '@ng-bootstrap/ng-bootstrap';
@NgModule({
    declarations: [AppComponent, ...],
    imports: [NgbModule.forRoot(), ...],
    bootstrap: [AppComponent]
})
ng-bootstrap requires Bootstrap's 4 css to be added in your project. you need to Install it explicitly via:

npm install bootstrap@4  --save 
In your angular.json add the file paths to the styles array in under build target

"styles": [
    "src/styles.css",
    "node_modules/bootstrap/dist/css/bootstrap.min.css"
],
