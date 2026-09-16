# AGENTS.md

## Objetivo del proyecto

Roadmap de conocimientos transversales en ingeniería del software. No es un listado de tecnologías, sino una guía para comprender fundamentos, principios y relaciones que se aplican independientemente del stack tecnológico. Especialmente relevante en la era de IA, donde lo importante es entender problemas, diseñar soluciones y validar código generado.

**Público objetivo**: Desarrolladores que quieran construir una base sólida y completa de conocimientos.

**Idioma**: Español.

## Estructura del repo

```
roadmap/
├── README.md              # Página principal con navegación por áreas
├── AGENTS.md              # Este archivo (contexto para IA)
├── assets/
│   └── img/               # Imágenes y assets visuales
├── path/                  # (futuro) Rutas de aprendizaje
└── theory/
    ├── sistemas/
    │   ├── informatica/   # Hardware, SO, arquitectura de computación
    │   ├── redes/         # Redes, protocolos, infraestructura de red
    │   ├── infraestructura/ # Virtualización, contenedores, CI/CD, IaC
    │   └── seguridad/     # Seguridad informática completa
    ├── software/
    │   ├── programacion/  # Fundamentos de programación
    │   ├── arquitectura/  # Diseño, patrones, arquitectura de software
    │   ├── api/           # APIs: REST, GraphQL, gRPC, tiempo real
    │   ├── calidad/       # QA, testing, métricas, revisiones
    │   ├── producto/      # Diseño de producto, UX/UI, gestión
    │   └── ia/            # IA, LLMs, agents, RAG, prompt engineering
    └── datos/
        ├── fundamentos/   # Conceptos de datos, modelado, arquitecturas
        ├── relacionales/  # SQL, normalización, transacciones
        ├── no-relacionales/ # NoSQL, tipos de BD no relacionales
        └── analisis/      # Análisis de datos, BI, visualización
```

Cada área tiene un `README.md` con una lista de temas organizados en secciones, usando checkboxes `- [ ]`.

## Filosofía del contenido

- Explicar conceptos antes que herramientas.
- Evitar tecnologías concretas siempre que sea posible.
- Evitar comandos.
- Evitar configuraciones.
- Evitar ejemplos dependientes de un lenguaje.
- Utilizar pseudocódigo cuando sea suficiente.
- Explicar mecanismos internos.
- Explicar historia y evolución cuando aporte contexto.

## Convenciones de nombres

- Sin tildes en nombres de archivo y carpeta.
- Títulos cortos.
- Extensión `.md`.
- Carpetas: `kebab-case` (guion medio).
- Archivos: `snake_case` (guion bajo).

## Formato del contenido

### Estructura general del documento

Siempre que el tema lo permita, utilizar la siguiente estructura:

```
# Titulo

Introduccion narrativa.

## Secciones con ##
```

- El titulo principal usa un unico `#`. El resto de encabezados usan `##`, `###`, `####` segun sea necesario.
- La introduccion es un texto narrativo que contextualiza el concepto de forma natural.
- No usar listas en la introduccion.
- No comenzar con definiciones de diccionario.
- No escribir: "En este tema veremos...", "El objetivo de este capitulo...", "Aprenderemos..."

### Diagramas

Cuando un concepto pueda entenderse mejor mediante un diagrama, utilizar Mermaid. Preferir:

- `flowchart`
- `sequenceDiagram`
- `classDiagram`
- `stateDiagram`
- `erDiagram`

Los diagramas deben ser sencillos y faciles de leer. Minimizar el codigo. Utilizar pseudocodigo siempre que sea suficiente. Utilizar codigo unicamente para ilustrar conceptos.

### Codigo

- Minimizar la cantidad de codigo.
- Pseudocodigo siempre que sea suficiente.
- Codigo unicamente para ilustrar conceptos.
- No dependan de un lenguaje concreto; si lo requieren, usar el mas representativo.

### Footer de navegacion

Todos los documentos deben finalizar con un footer de navegacion. El footer contiene:

- Enlace al documento anterior.
- Enlace al indice de la ruta.
- Enlace al README principal del proyecto.
- Enlace al documento siguiente.
- Los badges correspondientes, cuando existan.

Las rutas del footer deben calcularse siempre de forma relativa al archivo Markdown actual. Nunca asumir una profundidad fija. No utilizar rutas absolutas. No utilizar `./` suponiendo que representa la raiz del proyecto. Antes de generar el footer, calcular la profundidad real del archivo y construir las rutas correspondientes.

```md
---

<br>

<div align="center">
  <a href="ruta-anterior"><img src="ruta-badge-footer-anterior.svg" alt="Anterior"/></a>
  &nbsp;&nbsp;
  <a href="ruta-indice"><img src="ruta-badge-footer-indice.svg" alt="Indice"/></a>
  &nbsp;&nbsp;
  <a href="ruta-inicio"><img src="ruta-badge-footer-inicio.svg" alt="Inicio"/></a>
  &nbsp;&nbsp;
  <a href="ruta-siguiente"><img src="ruta-badge-footer-siguiente.svg" alt="Siguiente"/></a>
</div>
```

### Listas, tablas y notas

- No abusar de listas. Preferir parrafos explicativos. Utilizar listas unicamente cuando mejoren la comprension.
- Utilizar tablas unicamente para comparar conceptos. No convertir el documento en una coleccion de tablas.
- Utilizar blockquotes unicamente cuando aporten contexto adicional. No incluir una nota en todas las secciones.

### Profundidad

Cada documento debe ser suficientemente completo como para servir como referencia. No generar definiciones superficiales. Explicar:

- Funcionamiento.
- Arquitectura.
- Implicaciones.
- Ventajas.
- Inconvenientes.

Sin convertir el documento en un libro.

## Estilo y tono

### Estilo

Escribir como un libro tecnico. No escribir como un tutorial, una conversacion, un curso o un articulo comercial. No escribir para convencer. Escribir para explicar.

### Tono

- Tecnico.
- Preciso.
- Didactico.
- Objetivo.
- Natural.

Evitar frases motivacionales. Evitar exageraciones. Evitar opiniones personales.

### Convenciones generales

- Markdown limpio.
- Sin texto introductorio del asistente. Comenzar directamente con el contenido.
- Espanol tecnico. Seguir las normas de la RAE.
- Evitar palabras innecesariamente en mayusculas.
- No usar emojis.

## Estructura de carpetas por area

Los encabezados `##` del README de cada area se convierten en **carpetas** (`kebab-case`). Los items `- [ ]` de cada seccion se convierten en **archivos `.md`** (`snake_case`) dentro de esa carpeta.

Ejemplo con `theory/sistemas/informatica/`:

```
theory/sistemas/informatica/
├── README.md
├── arquitectura-de-hardware/
│   ├── arquitectura_de_la_computacion.md
│   ├── placa_base.md
│   ├── procesador_cpu.md
│   └── ...
├── software-de-sistema/
│   ├── conceptos_y_tipos_de_software.md
│   ├── arquitectura_del_software_y_capas_de_abstraccion.md
│   └── ...
└── sistemas-operativos/
    ├── conceptos_fundamentales.md
    ├── gestion_de_procesos.md
    └── ...
```

## Formato de archivos README (listas de temas)

Cada README de area sigue esta estructura:

1. **Titulo** centrado con `<h1 align="center">`
2. **Secciones** con `##` agrupando temas relacionados
3. **Temas** como items de lista con checkbox `- [ ] [Nombre del tema]()`
4. Los enlaces de los checkboxes apuntan a archivos `.md` individuales dentro de la carpeta del tema

Ejemplo de enlace en el README:

```md
- [ ] [Arquitectura de la computacion](./arquitectura-de-hardware/arquitectura_de_la_computacion.md)
```

## Flujo de trabajo

1. **Leer el AGENTS.md** para contexto general
2. **Leer el README.md del area** que se va a desarrollar para ver los temas pendientes
3. **Leer el archivo de contenido existente** (si hay) para mantener consistencia
4. **Desarrollar el contenido** del tema pendiente creando el archivo `.md` dentro de la carpeta correspondiente al `##` del README
5. **Actualizar el enlace** del checkbox en el README del area para que apunte al archivo creado
6. **Mantener coherencia** con el resto de archivos ya desarrollados

## Orden de desarrollo

El usuario indicara por que area y tema empezar. En caso de no indicarlo, priorizar:

1. Fundamentos primero (lo que sea prerequisito de otros temas)
2. De mas general a mas especifico
3. Dentro de cada area, seguir el orden del README

## Reglas importantes

- **NO INSTALAR NADA SIN PERMISO DEL USUARIO.**
