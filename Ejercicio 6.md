 ```erlang
%------------------------------------------------------------------------------
% Módulo: iterar_lista
% Propósito: Iterar sobre los valores de una lista y aplicar una función a cada elemento.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función para iterar sobre una lista y ejecutar la función
% `do_something/1` para cada elemento de la lista. Se utilizan dos implementaciones:
% comprensión de listas y `lists:foreach/2`.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(iterar_lista).
% 2. Llamar a la función:
% iterar_lista:iterar([1, 2, 3, 4, 5]).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo con funciones para iterar sobre listas.
%
% Notas:
% Este módulo aplica una operación (definida en `do_something/1`) a cada elemento
% de una lista, demostrando diferentes maneras de realizar la iteración en Erlang.
%------------------------------------------------------------------------------
% Definición del módulo
-module(iterar_lista).
% Exportación de las funciones
-export([iterar/1, do_something/1]).
% Definición de la función que itera sobre los elementos de una lista
% Aplica la función `do_something/1` a cada elemento de la lista usando dos métodos:
% - Comprensión de listas
% - `lists:foreach/2`
-spec iterar([any()]) -> ok.
iterar(Items) ->
% Implementación usando comprensión de listas
[do_something(X) || X <- Items],
% Implementación alternativa usando lists:foreach
lists:foreach(fun do_something/1, Items),
ok.
% Definición de la función do_something/1
% Aplica una operación a cada elemento (en este ejemplo, simplemente lo imprime).
-spec do_something(any()) -> ok.
do_something(X) ->
io:format("Procesando: ~p~n", [X]).

 ```
