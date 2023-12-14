# Steps

## 1. Create a new workspace

    ng new mono-workspace --create-application=false --skip-tests
    ng g application host-app --routing --style=scss
    ng g application mfe-app --routing --style=scss

---

## 2.

Run the host-app
ng s host-app -o

Run the mfe-app
ng s mfe-app -o

Install webpack
npm i webpack webpack-cli --save-dev

Add module federation
ng add @angular-architects/module-federation --project host-app --port 4200
ng add @angular-architects/module-federation --project mfe-app --port 4300

---

## 3.

Create compoo
ng g c home --project=host-app
ng g c todo --project=host-app

---

## 4.

ng g module todo-list --project=mfe-app
ng g c todo-list --project=mfe-app
