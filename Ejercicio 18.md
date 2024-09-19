 ```erlang
%------------------------------------------------------------------------------
% Módulo: buscar_item
% Propósito: Buscar un ítem X en una matriz 2D M y devolver las coordenadas (i, j) de la
celda que contiene el ítem.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%% Descripción:
% Este módulo define una función que busca un ítem en una matriz 2D. Si el ítem se
encuentra,
% devuelve las coordenadas de la celda en la que se encuentra. Si el ítem no se encuentra,
la función
% lanza una excepción `notfound`.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(buscar_item).
% 2. Llamar a la función:
% buscar_item:search(5, [[1, 2, 3], [4, 5, 6], [7, 8, 9]]).
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para buscar un ítem en una matriz 2D.
%
% Notas:
% La función devuelve una tupla `{i, j}` con las coordenadas del ítem si se encuentra,
% y lanza una excepción si el ítem no se encuentra en la matriz.
%------------------------------------------------------------------------------
% Definición del módulo
-module(buscar_item).
% Exportación de la función
-export([search/2]).
% Definición de la función que busca un ítem en una matriz 2D
% Toma un ítem X y una matriz M, y devuelve las coordenadas {i, j} del ítem.
-spec search(T, [[T]]) -> {pos_integer(), pos_integer()}.
search(X, M) -> search(X, M, 1).
search(_, [], _) -> throw(notfound);
search(X, [R|Rs], RN) ->
case search_row(X, R) of
notfound -> search(X, Rs, RN+1);
CN -> {RN, CN}
end.
search_row(X, Row) -> search_row(X, Row, 1).
search_row(_, [], _) -> notfound;
search_row(X, [X|_], CN) -> CN;
search_row(X, [_|Elems], CN) -> search_row(X, Elems, CN+1).

 ```
