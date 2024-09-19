 ```erlang
%------------------------------------------------------------------------------
% Módulo: barajar_lista
% Propósito: Generar una permutación aleatoria de los elementos de una lista.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que baraja una lista generando una permutación
% aleatoria de sus elementos. Utiliza la función `rand:uniform/0` para asignar
% valores aleatorios a cada elemento y luego ordena la lista por esos valores.
%
% Dependencias:
% Se requiere que el módulo `rand` esté disponible para generar números aleatorios.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(barajar_lista).
% 2. Llamar a la función:
% barajar_lista:barajar([a, b, c, d]).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para barajar una lista utilizando permutaciones
aleatorias.
%
% Notas:
% La función `rand:uniform/0` genera un número decimal aleatorio entre 0 y 1,
% lo cual se utiliza para ordenar la lista y así barajar los elementos.
%------------------------------------------------------------------------------
% Definición del módulo
-module(barajar_lista).
% Exportación de la función
-export([barajar/1]).
% Definición de la función que baraja una lista
% Genera una permutación aleatoria de los elementos de la lista X.
-spec barajar([any()]) -> [any()].
barajar(X) ->
% Genera una lista de pares {valor_aleatorio, elemento} para cada elemento en X.
% Luego, ordena esta lista por el valor aleatorio y extrae los elementos.
[Y || {_, Y} <- lists:sort([ {rand:uniform(), N} || N <- X])].

 ```
