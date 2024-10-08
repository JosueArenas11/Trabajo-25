 ```erlang
%------------------------------------------------------------------------------
% Módulo: ejecutar_tareas_paralelas
% Propósito: Ejecutar 1000 tareas independientes en paralelo usando procesos.
%
% Autor: Josue Arenas
% Fecha: 17 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo lanza 1000 tareas independientes utilizando procesos concurrentes. Cada tarea
% ejecuta la función f(I), donde I es el índice de la tarea, sin retornar ningún valor.
% Se utiliza spawn para crear procesos ligeros en Erlang.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(ejecutar_tareas_paralelas).
% 2. Llamar a la función para ejecutar 1000 tareas:
% ejecutar_tareas_paralelas:start_tasks().
%
% Historial de Cambios:
% 17/09/2024 - 1.0 - Creación del módulo para ejecutar tareas en paralelo.
%
%------------------------------------------------------------------------------
% Definición del módulo
-module(ejecutar_tareas_paralelas).
% Exportación de la función
-export([start_tasks/0, _f/1]).

% Función principal para iniciar las 1000 tareas en paralelo
start_tasks() ->
    lists:foreach(fun(I) -> spawn(?MODULE, _f, [I]) end, lists:seq(1, 1000)).

% Función f/1 que ejecuta la tarea para cada valor I (no retorna ningún valor)
-f(I) ->
    % Simulación de la tarea a ejecutar para el índice I
    io:format("Ejecutando tarea ~p~n", [I]),
    timer:sleep(1000).  % Pausa para simular trabajo, puedes modificarla según la tarea.
 ```
