 ```erlang
%------------------------------------------------------------------------------
% Módulo: procedimiento
% Propósito: Ejecutar un procedimiento que imprime "#YOLO!" en la consola.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define un procedimiento que imprime "#YOLO!" en la salida estándar.
% No retorna ningún valor, ya que su propósito es ejecutar un efecto secundario
% (imprimir en consola).
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(procedimiento).
% 2. Llamar a la función:
% procedimiento:procedure().
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del procedimiento `procedure/0`.
%
% Notas:
% Este es un procedimiento básico que demuestra cómo funcionan las funciones
% que solo tienen efectos secundarios en Erlang.
%------------------------------------------------------------------------------
% Definición del módulo
-module(procedimiento).
% Exportación de la función procedure/0
-export([procedure/0]).
% Definición del procedimiento
% `procedure/0` imprime "#YOLO!" en la consola.
-spec procedure() -> _.
procedure() ->
io:format("#YOLO!~n").

 ```
