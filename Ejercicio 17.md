 ```erlang
%------------------------------------------------------------------------------
% Módulo: invertir_lista
% Propósito: Invertir el orden de los elementos de una lista.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que invierte el orden de los elementos de una lista.
% Utiliza la función `lists:reverse/1` para realizar la inversión de la lista.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(invertir_lista).
% 2. Llamar a la función:
% invertir_lista:invertir([1, 2, 3, 4]).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para invertir una lista.
%
% Notas:
% La función `lists:reverse/1` realiza la inversión de la lista, creando una nueva lista
% con el orden de los elementos invertido.
%------------------------------------------------------------------------------
% Definición del módulo
-module(invertir_lista).
% Exportación de la función
-export([invertir/1]).
% Definición de la función que invierte el orden de los elementos de una lista
% Toma una lista y devuelve una nueva lista con los elementos en orden inverso.
-spec invertir([any()]) -> [any()].
invertir(List) ->
lists:reverse(List).

 ```
