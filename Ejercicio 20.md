 ```erlang
%------------------------------------------------------------------------------
% Módulo: convertir_a_cadena
% Propósito: Convertir un número real a una cadena de texto con 2 decimales.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que convierte un número real en su representación en
cadena de texto
% con 2 dígitos decimales. La función utiliza `io_lib:format/2` para realizar la conversión.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(convertir_a_cadena).
% 2. Llamar a la función:
% convertir_a_cadena:convertir(123.456).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para convertir un número real a una cadena con 2
decimales.
%
% Notas:
% La función `io_lib:format/2` toma un formato de cadena con especificador `~.2f` para
indicar 2 decimales
% y devuelve la cadena de texto resultante.
%------------------------------------------------------------------------------
% Definición del módulo
-module(convertir_a_cadena).
% Exportación de la función
-export([convertir/1]).
% Definición de la función que convierte un número real a una cadena con 2 decimales
% Toma un número real y devuelve su representación en cadena con 2 dígitos decimales.
-spec convertir(float()) -> string().
convertir(X) ->
io_lib:format("~.2f", [X]).

 ```
