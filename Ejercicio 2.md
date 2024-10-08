 ```erlang
%------------------------------------------------------------------------------
% Módulo: imprimir_hola
% Propósito: Imprimir "Hello" 10 veces en la consola.
%
% Autor: Arenas Herrera josue
% Fecha: 09 septiembre de 2024
% Versión: 1.1
%
% Descripción:
% Este módulo define una función simple que imprime "Hello" 10 veces en la consola.
% Utiliza la función `lists:foreach/2` para iterar sobre una secuencia de números
% y ejecutar la función de salida para cada iteración.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(imprimir_hola).
% 2. Llamar a la función:
% imprimir_hola:imprimir_10_veces().
%
% Historial de Cambios:
% 22/08/2024 - 1.0 - Creación del módulo con función básica `imprimir_10_veces/0`.
% 22/08/2024 - 1.1 - Se añadió un bucle para imprimir "Hello" 10 veces.
%
% Notas:
% Este es un ejemplo básico y no cubre aspectos avanzados de Erlang como
% concurrencia o manejo de errores.
%------------------------------------------------------------------------------
% Esta es la definición del módulo para el programa Erlang.
-module(imprimir_hola).
% Esta línea exporta la función `imprimir_10_veces/0` para hacerla accesible desde fuera del
módulo.
% El `/0` indica que la función no recibe argumentos.
-export([imprimir_10_veces/0]).
% Definición de la función
% `imprimir_10_veces/0` es una función que imprime "Hello" 10 veces en la consola.
imprimir_10_veces() ->
% `lists:foreach/2` toma una función anónima y una lista, ejecutando la función
% para cada elemento de la lista.
% `lists:seq(1, 10)` genera una lista de números del 1 al 10.
lists:foreach(
fun(_) ->
io:format("Hello~n")
end,
lists:seq(1, 10)
).

 ```
