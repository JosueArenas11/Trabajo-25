 ```erlang
%------------------------------------------------------------------------------
% Módulo: ordenar_por_propiedad
% Propósito: Ordenar listas de mapas o registros según el campo 'birth'.
%
% Autor: Josue Arenas
% Fecha: 17 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo proporciona funciones para ordenar listas de objetos (mapas o registros)
% basados en una propiedad específica, en este caso 'birth'.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(ordenar_por_propiedad).
% 2. Llamar a las funciones:
% ordenar_por_propiedad:sort_by_birth([{birth, 1990}, {birth, 1985}]).
%
% Historial de Cambios:
% 17/09/2024 - 1.0 - Creación del módulo para ordenar listas por una propiedad.
%
% Notas:
% - Para los mapas, se asume que el campo 'birth' existe, pero en caso de no existir se
%   retorna 'undefined'.
% - Para los registros, el campo 'birth' debe ser parte del registro.
%------------------------------------------------------------------------------
% Definición del módulo
-module(ordenar_por_propiedad).
% Exportación de las funciones
-export([sort_by_birth/1, sort_by_birth/2]).

% Definición de la función para ordenar una lista de mapas por el campo 'birth'
-spec sort_by_birth([map()]) -> [map()].
sort_by_birth(ListOfMaps) ->
    lists:sort(
      fun(A, B) ->
          maps:get(birth, A, undefined) =< maps:get(birth, B, undefined)
      end, ListOfMaps).

% Definición de la función para ordenar una lista de registros por el campo 'birth'
% Asume que el registro tiene la forma #item{birth = BirthDate}.
-spec sort_by_birth([#item{}]) -> [#item{}].
sort_by_birth(ListOfRecords) ->
    lists:keysort(#item.birth, ListOfRecords).
 ```
