
# Material de apoyo — Desarrollo de aplicaciones móviles

## 1. Ejemplos de apoyo

Repositorios con ejemplos prácticos para reforzar conceptos de Swift, SwiftUI, UIKit y Kotlin Multiplatform.

### 1.1. Contador con UIKit

**Repositorio:** [counter](https://github.com/salvathor/counter)

Aplicación básica de contador desarrollada con UIKit.

**Conceptos:**
- Patrón MVC.
- Interfaces mediante código.
- Auto Layout y `NSLayoutConstraint`.
- Target-Action.
- Ciclo de vida de `UIViewController`.
- Ambientes QA y PRD mediante `.xcconfig`.

### 1.2. Contador con SwiftUI

**Repositorio:** [counter_swiftui](https://github.com/salvathor/counter_swiftui)

Aplicación de contador utilizando SwiftUI y manejo de estados.

**Conceptos:**
- `@State`.
- Vistas declarativas.
- `VStack`, `HStack`, `Text` y `Button`.
- Modificadores y animaciones.
- Ciclo de vida mediante `scenePhase`.

### 1.3. Flash Cards

**Repositorio:** [flash_cards](https://github.com/salvathor/flash_cards)

Aplicación de tarjetas de estudio desarrollada con SwiftUI y arquitectura MVVM.

**Conceptos:**
- MVVM.
- `ObservableObject` y `@Published`.
- `@StateObject`.
- Modelos, vistas y ViewModels.
- Interacción con componentes visuales.

### 1.4. Kotlin Multiplatform

**Repositorio:** [kmp](https://github.com/salvathor/kmp)

Proyecto multiplataforma con lógica compartida entre Android e iOS.

**Conceptos:**
- Kotlin Multiplatform.
- Código compartido.
- Integración con SwiftUI.
- Repositorios y modelos de datos.
- Compose Multiplatform.

### 1.5. Fundamentos de UIKit

**Repositorio:** [ejemplo1_UIKit](https://github.com/salvathor/ejemplo1_UIKit)

Proyecto introductorio de desarrollo iOS con UIKit y Storyboards.

**Conceptos:**
- Navegación y paso de datos.
- `UIViewController`.
- Storyboards y Segues.
- Tablas y alertas.
- Extensiones de Swift.
- MVC.

### 1.6. Audio, video y gestos

**Repositorio:** [audio_video_gestos_swiftui](https://github.com/salvathor/audio_video_gestos_swiftui)

Ejemplo de reproducción multimedia y manejo de eventos táctiles con SwiftUI.

**Conceptos:**
- AVKit y `AVPlayer`.
- `VideoPlayer`.
- Gestos Tap, Long Press, Drag, Magnification y Rotation.
- `TabView`.

### 1.6. Swift Data

**Repositorio:** [Ejemplo Swift Data](https://github.com/salvathor/ejemplo_SwiftData)

Ejemplo de Lista de Tareas con Swift Data.

**Conceptos:**
- Swift Data
- Persistencia de datos

---

## 2. Notas

### Nota 1. Property Wrappers, macros y atributos en Swift

Un **Property Wrapper** permite encapsular comportamientos reutilizables asociados a una propiedad.

#### Tabla comparativa

| Property Wrapper / Macro | Framework | Descripción |
|---|---|---|
| `@State` | SwiftUI | Administra el estado local de una vista y actualiza la interfaz cuando cambia. |
| `@Binding` | SwiftUI | Permite compartir y modificar el estado entre vistas. |
| `@Environment` | SwiftUI | Accede a valores y dependencias del entorno. |
| `@StateObject` | SwiftUI | Crea y administra el ciclo de vida de un objeto `ObservableObject`. |
| `@ObservedObject` | SwiftUI | Observa un objeto externo que implementa `ObservableObject`. |
| `@Query` | SwiftData | Consulta datos persistidos y actualiza automáticamente la interfaz. |
| `@AppStorage` | SwiftUI | Almacena valores simples mediante `UserDefaults`. |
| `@Published` | Combine | Publica cambios de propiedades para sus observadores. |
| `@Observable` | Observation | **Macro.** Permite observar cambios en propiedades de una clase. |
| `@Model` | SwiftData | **Macro.** Define modelos de datos persistentes. |
| `@main` | Swift | **Atributo.** Identifica el punto de entrada de una aplicación. |

#### Diferencias importantes

- **`@State` vs. `@AppStorage`:** estado local frente a almacenamiento persistente de preferencias.
- **`@ObservedObject` vs. `@StateObject`:** observación de un objeto externo frente a administración de su ciclo de vida.
- **`@Published` vs. `@Observable`:** publicación mediante Combine frente a seguimiento de propiedades mediante Observation.
- **`@Query` vs. `@AppStorage`:** persistencia de modelos con SwiftData frente a preferencias sencillas con UserDefaults.

#### Recomendaciones

Para proyectos con **iOS 17 o superior**, generalmente se recomienda utilizar `@Observable` y `@State` para administrar modelos de estado en SwiftUI.

`@StateObject`, `@ObservedObject` y `@Published` continúan siendo útiles en proyectos basados en `ObservableObject` y Combine.

#### Conceptos fundamentales

- **Property Wrapper:** encapsula comportamientos reutilizables asociados a una propiedad.
- **Macro:** genera o transforma código durante la compilación.
- **Atributo:** proporciona información o modifica el comportamiento de una declaración.
