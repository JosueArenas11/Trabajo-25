 ```erlang
%------------------------------------------------------------------------------
% Módulo: seleccionar_aleatorio_entero
% Propósito: Seleccionar un número entero aleatorio en el intervalo [a..b].
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que genera un número entero aleatorio en el intervalo
% [a..b], donde tanto `a` como `b` son inclusivos. Utiliza la función `crypto:rand_uniform/2`
% para generar un número aleatorio en el rango deseado.
%
% Dependencias:
% Se requiere que el módulo `crypto` esté disponible para generar números aleatorios.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(seleccionar_aleatorio_entero).
% 2. Llamar a la función:
% seleccionar_aleatorio_entero:aleatorio(3, 7).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para seleccionar un número entero aleatorio en
un intervalo.
%
% Notas:
% La precondición es que `a` debe ser menor que `b` para asegurar un intervalo válido.
%------------------------------------------------------------------------------
% Definición del módulo
-module(seleccionar_aleatorio_entero).
% Exportación de la función
-export([aleatorio/2]).
% Definición de la función que selecciona un número entero aleatorio en [a..b]
% La precondición es que A < B.
-spec aleatorio(integer(), integer()) -> integer().
aleatorio(A, B) when A < B ->
% Genera un número entero aleatorio en el intervalo [A, B].
crypto:rand_uniform(A, B + 1).

 ```
