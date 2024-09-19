 ```erlang
%------------------------------------------------------------------------------
% Módulo: convertir_a_entero
% Propósito: Convertir una cadena de texto a un número entero.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que convierte una cadena de texto que representa un
número entero
% en un valor entero. La función utiliza `list_to_integer/1` para realizar la conversión.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(convertir_a_entero).
% 2. Llamar a la función:
% convertir_a_entero:convertir("123").
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para convertir una cadena de texto a un entero.
%
% Notas:
% La función `list_to_integer/1` toma una cadena de texto en formato decimal y devuelve el
valor entero correspondiente.
%------------------------------------------------------------------------------
% Definición del módulo
-module(convertir_a_entero).
% Exportación de la función
-export([convertir/1]).
% Definición de la función que convierte una cadena de texto a un entero
% Toma una cadena de texto en formato decimal y devuelve el número entero
correspondiente.
-spec convertir(string()) -> integer().
convertir(S) ->
list_to_integer(S).

 ```
