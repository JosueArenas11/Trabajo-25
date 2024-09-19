 ```erlang
%------------------------------------------------------------------------------
% Módulo: remover_item
% Propósito: Remover un elemento de una lista dado su índice.
%
% Autor: Josue Arenas
% Fecha: 17 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que elimina el i-ésimo elemento de una lista. El índice
% debe ser 1 o mayor (siguiendo el estilo de Erlang), es decir, el primer elemento tiene
% índice 1.
%
% Dependencias:
% - lists:split/2 para dividir la lista.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(remover_item).
% 2. Llamar a la función:
% remover_item:remove_at(3, [a, b, c, d, e]).
%
% Historial de Cambios:
% 17/09/2024 - 1.0 - Creación del módulo para remover un elemento de una lista por índice.
%
%------------------------------------------------------------------------------
% Definición del módulo
-module(remover_item).
% Exportación de la función
-export([remove_at/2]).

% Definición de la función para remover el elemento en el índice I (donde el índice empieza en 1)
-spec remove_at(pos_integer(), list()) -> list().
remove_at(I, Items) ->
    {Left, [_|Right]} = lists:split(I-1, Items),
    Left ++ Right.

 ```
