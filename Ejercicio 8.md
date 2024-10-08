 ```erlang
%------------------------------------------------------------------------------
% Módulo: crear_mapa
% Propósito: Crear un mapa con pares clave-valor como contenido inicial.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función para crear un mapa (associative array) en Erlang
% con algunos pares clave-valor proporcionados como contenido inicial.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(crear_mapa).
% 2. Llamar a la función:
% crear_mapa:nuevo_mapa().
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo con un ejemplo básico de creación de mapas.
%
% Notas:
% Los mapas en Erlang permiten asociar claves con valores. Las claves pueden ser
% átomos, cadenas, binarios u otros tipos de datos.
%------------------------------------------------------------------------------
% Definición del módulo
-module(crear_mapa).
% Exportación de la función
-export([nuevo_mapa/0]).
% Definición de la función que crea un nuevo mapa con contenido inicial
% Crea un mapa con varias claves y valores de diferentes tipos.
-spec nuevo_mapa() -> map().
nuevo_mapa() ->
% Crear un mapa con claves y valores de diferentes tipos.
X = #{one => 1, "two" => 2.0, <<"three">> => [i, i, i]},
% Imprimir el mapa.
io:format("Mapa creado: ~p~n", [X]),
X.

 ```
