 ```erlang
%------------------------------------------------------------------------------
% Módulo: iterar_mapa
% Propósito: Iterar sobre las claves y valores de un mapa e imprimirlos.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que itera sobre un mapa y imprime cada clave
% y su valor correspondiente. Utiliza `maps:fold/3` para recorrer el mapa y
% la función `io:format/2` para la salida.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(iterar_mapa).
% 2. Llamar a la función:
% iterar_mapa:imprimir_mapa(#{"a" => 1, "b" => 2, "c" => 3}).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para iterar sobre claves y valores de un mapa.
%
% Notas:
% La función `maps:fold/3` es útil para recorrer mapas y aplicar una función a cada
clave-valor.
%------------------------------------------------------------------------------
% Definición del módulo
-module(iterar_mapa).
% Exportación de la función
-export([imprimir_mapa/1]).
% Definición de la función que itera sobre un mapa e imprime las claves y valores
% Itera sobre el mapa MyMap e imprime cada clave y valor.
-spec imprimir_mapa(map()) -> ok.
imprimir_mapa(MyMap) ->
% Utiliza maps:fold/3 para iterar sobre el mapa.
maps:fold(
fun(K, V, Acc) ->
% Imprime la clave y el valor.
io:format("~p: ~p~n", [K, V]),
Acc
end,
ok,
MyMap
).

 ```
