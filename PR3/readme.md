# Практика 3
# Стратегия
```
@startuml
title Практическая работа 3: Strategy
class Variant{
selection()
}
class Game{
strategy: Variant
init()
play()
}

class Paper{
selection()
}
class Rock{
selection()
}
class Scissors{
selection()
}
class Pencil{
selection()
}
class Fire{
selection()
}
class main{
int n
str vibor
playtime()
player1.play(player2)
}
note right of main::"playtime()"
player1 = playtime(vibor)
player2 = playtime(vibor)
end note

Paper --> Variant
Rock --> Variant
Scissors --> Variant
Pencil --> Variant
Fire --> Variant
main *--> Variant
main --Game
@enduml
```

![](5.png)
# Шаблонный метод
```
@startuml
title Практическая работа 3: Template Method
class Algorithm{
template_method()
flagstock()
draw_1()
draw_2()
draw_3()
final()
printer()
}
note right of Algorithm::"template_method()"
self.flagstock()
self.draw_1()
self.draw_2()
self.draw_3()
self.final()
self.printer()
end note

class colors{
painwhite()
painred()
painblue()
}

class RussianFlag{
z = colors
z.pain
draw_1()
draw_2()
draw_3()
final()
}
class  Austria{
z = colors
z.pain
draw_1()
draw_2()
draw_3()
}

Algorithm <|-- Austria :Немецкий флаг
Algorithm <|-- RussianFlag : Российский флаг

RussianFlag -  Austria
(RussianFlag, Austria) - colors:Задает цвет
@enduml

```
![](6.png)
