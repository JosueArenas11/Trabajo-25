 ```erlang
%------------------------------------------------------------------------------
% Módulo: seleccionar_aleatorio_flotante
% Propósito: Seleccionar un número flotante aleatorio en el intervalo [a..b).
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una función que genera un número flotante aleatorio en el intervalo
% [a..b), donde `a` es inclusivo y `b` es exclusivo. Utiliza la función `rand:uniform/0`
% para generar un número aleatorio en el rango [0, 1) y lo escala al intervalo deseado.
%
% Dependencias:
% Se requiere que el módulo `rand` esté disponible para generar números aleatorios.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(seleccionar_aleatorio_flotante).
% 2. Llamar a la función:
% seleccionar_aleatorio_flotante:aleatorio(2.0, 5.0).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para seleccionar un número flotante aleatorio en
un intervalo.
%
% Notas:
% La precondición es que `a` debe ser menor que `b` para asegurar un intervalo válido.
%------------------------------------------------------------------------------
% Definición del módulo
-module(seleccionar_aleatorio_flotante).
% Exportación de la función
-export([aleatorio/2]).
% Definición de la función que selecciona un número flotante aleatorio en [a..b)
% La precondición es que A < B.
-spec aleatorio(float(), float()) -> float().
aleatorio(A, B) when A < B ->
% Genera un número aleatorio en el intervalo [A, B).
A + (B - A) * rand:uniform().

 ```
