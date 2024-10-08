 ```erlang
%------------------------------------------------------------------------------
% Módulo: iterar_indices_valores
% Propósito: Iterar sobre los índices y valores de una lista e imprimirlos.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función para iterar sobre los índices y valores de una lista.
% Utiliza `lists:zip/2` para combinar los índices generados con los valores de la lista.
% Luego imprime cada par índice-valor.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(iterar_indices_valores).
% 2. Llamar a la función:
% iterar_indices_valores:iterar([a, b, c, d]).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo con función para iterar sobre índices y valores.
%
% Notas:
% Este módulo muestra cómo obtener y trabajar con los índices y valores de una lista
% en Erlang, utilizando la función `lists:zip/2`.
%------------------------------------------------------------------------------
% Definición del módulo
-module(iterar_indices_valores).
% Exportación de la función
-export([iterar/1]).
% Definición de la función que itera sobre los índices y valores de una lista
% Usa `lists:zip/2` para emparejar los índices generados con los valores de la lista.
-spec iterar([any()]) -> ok.
iterar(Items) ->
% `lists:seq(1, length(Items))` genera una secuencia de índices del 1 al tamaño de la lista.
% `lists:zip/2` combina los índices con los valores de la lista.
WithIndex = lists:zip(lists:seq(1, length(Items)), Items),
% Imprime la lista de pares índice-valor.
io:format("Índices y Valores: ~p~n", [WithIndex]),
ok.

 ```
