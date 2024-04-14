# Dart

## Variables y tipos de datos

- Existe inferencia de tipos `Tipo dato = Tipo();`
- Se puede tipar de forma estática
- Todo es un objeto (Object)
- Existe el tipo null
- El tipo dynamic admite cualquier dato (sería dinámico)

```dart
Tipo var1 = Tipo(); // Variable
var var2 = Tipo(); // Inferencia de tipo
Tipo? var3; // Dato con opción a null
dynamic var4 = 12; // Cualquier tipo de dato, null incluido
```

### Principales estructuras

- Lo mismo que en todos los lenguajes
- Son calleables `calleable[i]`

```dart
List<String> listaStrings = ['dato 1', 'dato 2', 'dato 3'];
Set<String> setStrings = {'dato 1', 'dato 2', 'dato 3'};
Map<string, int> mapa = {"key1": 1, "key2": 2};
```

## Estructuras de control

## Funciones

```dart
Tipo func1( Tipo arg ) { //argumento normal
    return arg;
}

Tipo func2( [ Tipo arg = Tipo() ] ) { //argumento opcional
    return arg;
}

Tipo func3({ Tipo? arg1, Tipo arg2 = Tipo() }) {
    return arg2;
}

Tipo func4({
    required Tipo argRequerido,
    Tipo? arg1, 
    Tipo arg2 = Tipo() }) {
    return argRequerido;
}
```

## Clases

```dart
Clase clase = Clase(); //constructor, el new es opcional

class Clase {
    Tipo atributo1; //atributo normal
    Tipo? atributo2; //atributo nullable
    Tipo get atributo3 { //getter
        return atributo1 + atributo2 ?? Tipo();
    };

    set atributo3( Tipo atr3 ) { //set
        //logica
    }

    Clase(Tipo atributo1) {
        this.atributo1 = atributo1;
    }

    Clase.otroConstructor2({
        required atributo1, 
        required atributo2
        }) {
            this.atributo1 = atributo1;
    }

    Clase.otroConstructor2( Map<String, String> mapa):
        this.atributo1 = mapa[arg1] ?? Tipo(),
        this.atributo2 = mapa[arg1] ?? Tipo();
}
```

- Las clases abstractas hacen las veces de interfaces
- `extends` se utiliza para heredar

```dart
abstract class ClaseAbstracta {
    ClaseAbstracta()
}

class Clase extends ClaseAbstracta {
    Clase(): super();
}
```

- Los mixins son "interfaces" que agregan comportamiento que si esta definido

```dart
abstract class Mixin {
    void metodo() => funcion();
}

class ClaseConMixin with Mixin () {

}

ClaseConMixin.metodo(); //hereda el metodo
```

## Asincronia

### Asinc await

- Async regreta Future
- Await solamente se puede utilizar en funciones asincronas

### Futures

- Implementacion de asincronia como puede serlo un Promise

```dart
Future<Tipo> futurable() {
    return Future.delayed()
}
```

|Metodo|Funcion|
|---|---|
|`then((valor){logica;})`|Crea un espacio de ejecucion para despues de ejecutar el Future|
|||
