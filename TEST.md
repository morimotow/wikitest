````puml
@startuml
title 呼び出し
hide footbox

Actor "太郎" as Taro
Actor "花子" as Hanako

Taro -> Hanako : 同期呼び出し

Taro -\ Hanako : 非同期呼び出し。UML 1.3以前

Taro ->> Hanako : 非同期呼び出し。UML 1.4以降

note over Taro, Hanako
     UML 1.3以前 と 1.4以降で非同期呼び出しの記法が変わっている。
     マーチン・ファウラー著「UMLモデリングのエッセンス 第3版」では、
     1.3以前の記法を推奨している。
end note

[-> Taro : 外部からの呼び出し
Taro -> Taro : 自己呼び出し
Hanako ->] : 外部呼び出し
Hanako <--] : 外部からの戻り
@enduml
````
