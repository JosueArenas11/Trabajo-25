 ```erlang
%------------------------------------------------------------------------------
% Módulo: crear_matriz
% Propósito: Crear e inicializar una matriz bidimensional.
%
% Autor: Josue Arenas
% Fecha: 17 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que crea una matriz bidimensional de tamaño MxN, donde M
% es el número de filas y N el número de columnas. Cada posición de la matriz contiene un
% número real.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(crear_matriz).
% 2. Llamar a la función:
% crear_matriz:crear(3, 4).
%
% Historial de Cambios:
% 17/09/2024 - 1.0 - Creación del módulo para inicializar una matriz bidimensional.
%
% Notas:
% La función genera una lista de tuplas donde cada tupla representa una fila y columna
% con valores reales.
%------------------------------------------------------------------------------
% Definición del módulo
-module(crear_matriz).
% Exportación de la función
-export([crear/2]).

% Definición de la función para crear una matriz bidimensional de tamaño MxN
-spec crear(integer(), integer()) -> list().
crear(M, N) ->
    X = [{R * 1.0, C * 1.0} || R <- lists:seq(1, M), C <- lists:seq(1, N)],
    X.

 ```
