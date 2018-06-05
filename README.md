# AngularDataTable

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.7.4. We're creating a single page angular application from CLI command and then integrate material with it and create a sample data table using MatTableModule and mat-table directive.The data table will support pagination, sorting, filtering and row selection provided by MatPaginator and matSort in MatPaginatorModule and MatSortModule.

To enable pagination, angular provides mat-paginator directive that accepts required parameter to perform pagination.This directive should be placed after the mat-table directive.But before using this directive, we need to import MatPaginatorModule in the our material.module.ts.


For filtering material does not provide any specific directive similar to sorting and pagination but we can achieve filtering by defining our custom method for it.We can have a similar implementation like below which can be called from .html on keyup event.

`<mat-form-field>
      <input matInput (keyup)="applyFilter($event.target.value)" placeholder="Filter">
    </mat-form-field>`
    
`applyFilter(filterValue: string) {

    filterValue = filterValue.trim();
    
    filterValue = filterValue.toLowerCase();
    
    this.dataSource.filter = filterValue;
    

}`
  

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
