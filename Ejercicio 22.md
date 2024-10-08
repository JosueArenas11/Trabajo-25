 ```erlang
%------------------------------------------------------------------------------
% Módulo: crear_array_3d
% Propósito: Crear e inicializar un arreglo tridimensional con valores reales aleatorios.
%
% Autor: Josue Arenas
% Fecha: 17 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define funciones para crear un arreglo tridimensional de tamaño MxNxP.
% Los elementos de este arreglo son números reales generados aleatoriamente entre 0 y 1.
%
% Dependencias:
% - rand:uniform/0 para generar números reales aleatorios.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(crear_array_3d).
% 2. Llamar a la función:
% crear_array_3d:array(3, 4, 2).
%
% Historial de Cambios:
% 17/09/2024 - 1.0 - Creación del módulo para inicializar un arreglo tridimensional.
%
% Notas:
% - La función `rand:uniform/0` debe estar inicializada con `rand:seed/1` para resultados
%   reproducibles.
%------------------------------------------------------------------------------
% Definición del módulo
-module(crear_array_3d).
% Exportación de la función
-export([array/3]).

% Definición de la función para crear un arreglo tridimensional de tamaño MxNxP
-spec array(pos_integer(), pos_integer(), pos_integer()) -> [[[float()]]].
array(M, N, P) ->
    [array(M, N) || _ <- lists:seq(1, P)].

% Definición de la función para crear una matriz bidimensional de tamaño MxN
array(M, N) ->
    [array(M) || _ <- lists:seq(1, N)].

% Definición de la función para crear una lista de tamaño M con números reales aleatorios
array(M) ->
    [rand:uniform() || _ <- lists:seq(1, M)].

 ```
