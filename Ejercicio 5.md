 ```erlang
%------------------------------------------------------------------------------
% Módulo: points
% Propósito: Crear una estructura de datos para un punto 2D.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una estructura de datos para representar un punto en un plano
% 2D utilizando dos números en coma flotante (X e Y). También provee funciones
% para crear un nuevo punto y acceder a sus coordenadas.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(points).
% 2. Crear un nuevo punto:
% P = points:new(1.5, 2.5).
% 3. Obtener las coordenadas X e Y del punto:
% X = points:x(P).
% Y = points:y(P).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación de la estructura de datos `point/0` y funciones
% básicas `new/2`, `x/1` y `y/1`.
%
% Notas:
% Este módulo utiliza mapas para representar puntos. Alternativamente, se puede
% implementar usando tuplas en lugar de mapas.
%------------------------------------------------------------------------------
% Definición del módulo
-module(points).
% Exportación de funciones
-export([new/2, x/1, y/1]).
% Declaración del tipo opaco
% `point/0` es una estructura de datos que contiene dos números en coma flotante, X e Y.
-opaque point() :: #{x => float(), y => float()}.
-export_type([point/0]).
% Especificación de la función new/2
% Crea un nuevo punto con coordenadas X e Y.
-spec new(float(), float()) -> point().
new(X, Y) ->
#{x => X, y => Y}.
% Especificación de la función x/1
% Devuelve la coordenada X de un punto.
-spec x(point()) -> float().
x(#{x := X}) ->
X.
% Especificación de la función y/1
% Devuelve la coordenada Y de un punto.
-spec y(point()) -> float().
y(#{y := Y}) ->
Y.
% Implementación alternativa con mapas
% PointAsAMap = #{x => X, y => Y}.
% Implementación alternativa con tuplas
% PointAsATuple = {X, Y}.

 ```
