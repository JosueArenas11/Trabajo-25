 ```erlang
%------------------------------------------------------------------------------
% Módulo: verificar_valor
% Propósito: Verificar si una lista contiene un valor específico.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
% Descripción:
% Este módulo define una función para verificar si una lista contiene un valor específico.
% La función utiliza `lists:member/2` para realizar la verificación. También se presentan
% implementaciones alternativas para lograr la misma tarea.
%
% Dependencias:
% Ninguna.
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(verificar_valor).
% 2. Llamar a la función:
% verificar_valor:contiene(3, [1, 2, 3, 4]).
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo con funciones para verificar la existencia de un valor en
una lista.
% Notas:
% La función `lists:member/2` es la forma más directa y eficiente de realizar esta verificación.
% También se incluyen implementaciones alternativas para ilustrar cómo se puede hacer de manera
% recursiva.
%------------------------------------------------------------------------------
% Definición del módulo
-module(verificar_valor).
% Exportación de la función
-export([contiene/2]).
% Implementación principal utilizando `lists:member/2`
% Verifica si el valor X está en la lista Lista.
-spec contiene(any(), [any()]) -> boolean().
contiene(X, Lista) ->
lists:member(X, Lista).
% Implementación alternativa utilizando recursión
% Verifica si el valor Value está en la lista. Retorna true si lo encuentra, false si no.
-spec miembro(any(), [any()]) -> boolean().
miembro(_, []) -> false;
miembro(Value, [H|T]) ->
case H of
Value -> true;
_ -> miembro(Value, T)
end.
% Implementación alternativa utilizando un patrón de coincidencia
% Verifica si el valor Value está en la lista. Retorna true si lo encuentra, false si no.
-spec miembro_parecido(any(), [any()]) -> boolean().
miembro_parecido(_, []) -> false;
miembro_parecido(Value, [H|_]) when Value =:= H -> true;
miembro_parecido(Value, [_|T]) -> miembro_parecido(Value, T).

 ```
