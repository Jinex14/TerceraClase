# TerceraClase

----------------------------------------------
------ANGULAR CLI CON MATERIAL DESING---------
----------------------------------------------

crear la aplicacion y en consola pones lo siguiente
npm install --save @angular/material @angular/cdk
luego se instala las animaciones con este comando
npm install --save @angular/animations

se debe agregar esta linea en el app module 
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';
y se agrega al Ngmodule el BrowserAnimationsModule

Soporte para iconos en el index.html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">

Agregar el css a styles.css
@import "~@angular/material/prebuilt-themes/indigo-pink.css";

crear un modulo relacionado con el modulo principal app con el siguiente comando
ng generate module material --module app

----------------------------------------------
----SE TERMINA LA INSTALACIÓN DE MATERIAL-----
----------------------------------------------

Generar nuevo componente dentro de la carpeta material
ng generate component material/material-demo --module material

borramos el contenido de app.component.html
editamos el app-routing.module.ts
dentro de routing ponemos 
  {
    path: 'material-demo',
    component: MaterialDemoComponent
  }
  tabien realizamos el import 
  import {MaterialDemoComponent} from './material/material-demo/material-demo.component';
  luego de eso se debe ver el modulo agregando material-demo a la url

  en el modulo material agregar lo siguiente
  import {MatToolbarModule} from '@angular/material';

  luego en la parte de imports y antes de declarations se agrega esto
  exports: [
    MatToolbarModule
  ],

  En el app.component.html se pone lo siguiente
 -- <mat-toolbar color="primary">
  --  <span>Primera vez con Material</span>
   -- </mat-toolbar>

con eso se tiene una toolbar

para agregar botones se va modulo material
import {MatToolbarModule, MatButtonModule, MatIconModule} from '@angular/material';
tambien en el import y en el export

creamos otro componente
ng generate component home --module app
definimos una nueva configuracion en el routing
