﻿# 1.2-Leo-Casta-eda
                                                        Patrón Singleton

                        
Propósito

El patrón Singleton es un patrón de diseño creacional que garantiza que una clase tenga una única instancia, proporcionando un punto de acceso global a dicha instancia.

Problema

El patrón Singleton resuelve dos problemas:

Garantizar una única instancia: Esto es útil para controlar el acceso a recursos compartidos como bases de datos o archivos.
Acceso global: Permite acceder a un objeto desde cualquier parte del programa sin necesidad de variables globales inseguras.


Solución

El patrón Singleton tiene dos pasos clave:

Constructor privado: Evita que otros objetos usen el operador new para crear una nueva instancia.

Método de creación estático: Este método invoca al constructor privado para crear una instancia y la almacena en un campo estático. 
Las siguientes llamadas a este método devuelven la instancia almacenada.

Analogía en el Mundo Real
El gobierno es un ejemplo de Singleton: un país solo puede tener un gobierno oficial que actúa como un punto de acceso global.

Implementación en JavaScript

javascript
class Singleton {
    constructor() {
        if (Singleton.instance) {
            return Singleton.instance;
        }
        this.value = Math.random(); // Valor aleatorio para demostrar la unicidad
        Singleton.instance = this;
    }

    getValue() {
        return this.value;
    }
}
