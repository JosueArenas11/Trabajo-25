 ```erlang
%------------------------------------------------------------------------------
% Módulo: estructura_arbol
% Propósito: Definir una estructura de árbol recursiva donde cada nodo puede tener cero
o más hijos.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define un registro para representar un nodo en un árbol. Cada nodo puede
tener
% un valor y una lista de nodos hijos. La estructura es recursiva, ya que cada nodo puede
contener
% otros nodos como hijos.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(estructura_arbol).
% 2. Crear un nodo y un árbol:
% NodoHijo = #node{value = 1}.
% NodoPadre = #node{value = 2, children = [NodoHijo]}.
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Creación del módulo para definir una estructura de árbol.
%
% Notas:
% La estructura es recursiva porque cada nodo puede contener una lista de nodos hijos,
% los cuales son instancias de la misma estructura.
%------------------------------------------------------------------------------
% Definición del módulo
-module(estructura_arbol).
% Exportación del registro
-export([node/0]).
% Definición del registro para un nodo en el árbol
-record(node, {
value :: any(), % Valor almacenado en el nodo
children = [] :: [node#{}] % Lista de hijos, que son nodos
}).

 ```
