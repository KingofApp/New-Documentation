# Module requires object

Este objecto indica que el módulo al que pertenece necesita de otros módulos para completar su funcionalidad. La integración de con otros módulos pueden ser manera interna o externa:

* Externa (out): Es el formato por defecto. Implica que cuando el módulo requerido sea llamado el nuevo módulo no seguirá presente. Se utiliza generalmente para llamar subsecciones.
* Interna (in): Permite que el módulo requerido se monte como hijo de un módulo contenedor. Se utiliza para enlazar barras de busqueda y elementos que amplian las funcionalidades de las vistas.

Puede tener dos formatos, [simple](#Simple) y [completo](#Completo):

## Simple

Es un array en especifica los `identifier`s de los módulos requeridos:
```
[
  requiredModuleIdentifier1,
  requiredModuleIdentifier2,
  requiredModuleIdentifier3
]
```

## Completo

Es un objeto de array que define los módulos que se comportan como internos y externos. Una copia del ejemplo anterior en formato completo tendría este aspecto:

```
{
  out: [
    requiredModuleIdentifier1,
    requiredModuleIdentifier2,
    requiredModuleIdentifier3
  ],
  in:  []
}
```

Añadiendo una dependencia como interna el resultado sería:

```
{
  out: [
    requiredModuleIdentifier1,
    requiredModuleIdentifier2,
    requiredModuleIdentifier3
  ],
  in:  [ requiredInModuleIdentifier ]
}
```
