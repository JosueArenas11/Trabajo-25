 ```erlang
%------------------------------------------------------------------------------
% Módulo: arbol_binario
% Propósito: Definir una estructura de datos para un árbol binario.
%
% Autor: Josue Arenas
% Fecha: 9 de Septiembre de 2024
% Versión: 1.0
%
% Descripción:
% Este módulo define una estructura de datos recursiva para un árbol binario.
% Cada nodo del árbol contiene un dato y referencias a sus hijos izquierdo y derecho,
% que también son árboles binarios. La estructura no tiene referencia al nodo padre.
%
% Dependencias:
% Ninguna.
%
% Ejemplo de Uso:
% 1. Compilar el módulo:
% c(arbol_binario).
% 2. Crear un árbol binario:
% Arbol = #{data => 10, left => #{data => 5, left => #{data => 3, left => none, right =>
none}, right => none}, right => #{data => 15, left => none, right => none}}.
%
% Historial de Cambios:
% 09/09/2024 - 1.0 - Definición de la estructura de datos `binary_tree/1`.
%
% Notas:
% La estructura `binary_tree/1` es un mapa que permite representar árboles binarios
% con datos de tipo `T`. Los hijos izquierdo y derecho también son árboles binarios.
%------------------------------------------------------------------------------
% Definición del módulo
-module(arbol_binario).
% Exportación de tipos
-export_type([binary_tree/1]).
% Definición del tipo de árbol binario
% Un árbol binario tiene un dato y dos hijos, que son también árboles binarios.
-type binary_tree(T) ::
#{ data := T
, left := binary_tree(T) | none
, right := binary_tree(T) | none
}.
% Definición de `none` para representar nodos vacíos
-type none() :: none.

 ```
