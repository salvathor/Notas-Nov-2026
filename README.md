
# Property Wrappers, Macros y Atributos en Swift

## 1. Tabla comparativa

| Property Wrapper / Macro | Framework | Descripción |
|---|---|---|
| `@State` | SwiftUI | Administra el estado local de una vista y actualiza la interfaz cuando cambia. |
| `@Binding` | SwiftUI | Permite compartir y modificar el estado de una propiedad entre vistas, sin duplicarlo. |
| `@Environment` | SwiftUI | Permite acceder a valores y dependencias disponibles en el entorno de una vista. |
| `@StateObject` | SwiftUI | Crea y administra el ciclo de vida de un objeto que implementa `ObservableObject`. |
| `@ObservedObject` | SwiftUI | Observa un objeto externo que implementa `ObservableObject` y actualiza la vista cuando publica cambios. |
| `@Query` | SwiftData | Consulta modelos persistidos y mantiene los resultados sincronizados con la interfaz SwiftUI. |
| `@AppStorage` | SwiftUI | Almacena y recupera valores sencillos mediante `UserDefaults` y actualiza la vista al cambiar. |
| `@Published` | Combine | Publica los cambios de una propiedad para que sus observadores puedan reaccionar. Se utiliza habitualmente con `ObservableObject`. |
| `@Observable` | Observation | **Macro**, no Property Wrapper. Convierte una clase en observable y permite que SwiftUI detecte cambios en las propiedades utilizadas. |
| `@Model` | SwiftData | **Macro**, no Property Wrapper. Convierte una clase en un modelo persistente administrado por SwiftData. |
| `@main` | Swift | **Atributo**, no Property Wrapper. Identifica el punto de entrada de una aplicación. |

## 2. Diferencias importantes

- **`@State` vs. `@AppStorage`:** ambos pueden actualizar la interfaz, pero `@State` mantiene estado local y `@AppStorage` persiste valores sencillos en `UserDefaults`.
- **`@ObservedObject` vs. `@StateObject`:** el primero observa un objeto proporcionado externamente; el segundo administra la instancia y su ciclo de vida.
- **`@Published` vs. `@Observable`:** `@Published` pertenece a Combine y publica cambios mediante publishers. `@Observable` pertenece a Observation y utiliza seguimiento de acceso a propiedades.
- **`@Query` vs. `@AppStorage`:** `@Query` consulta modelos persistentes de SwiftData, mientras que `@AppStorage` está orientado a preferencias y configuraciones simples.

## 3. Recomendaciones

Para proyectos nuevos con **iOS 17 o superior**, generalmente se recomienda utilizar `@Observable` junto con `@State` para los modelos de estado de SwiftUI.

`@StateObject`, `@ObservedObject` y `@Published` siguen siendo útiles cuando trabajas con `ObservableObject` y Combine.

## 4. Conceptos fundamentales

- **Property Wrapper:** encapsula comportamientos reutilizables asociados a una propiedad.
- **Macro:** genera o transforma código durante la compilación.
- **Atributo:** proporciona información o modifica el comportamiento de una declaración.

## 5. Repositorios de ejemplo

Los siguientes repositorios contienen proyectos prácticos para reforzar los conceptos de desarrollo iOS, Swift, SwiftUI, UIKit y Kotlin Multiplatform.

### 5.1. Contador con UIKit

**Repositorio:** [counter](https://github.com/salvathor/counter)

Aplicación básica de un contador desarrollada con UIKit.

Permite practicar:

- Patrón MVC.
- Construcción de interfaces mediante código.
- Auto Layout y `NSLayoutConstraint`.
- Eventos mediante Target-Action.
- Ciclo de vida de `UIViewController`.
- Configuración de ambientes QA y PRD mediante `.xcconfig`.

### 5.2. Contador con SwiftUI

**Repositorio:** [counter_swiftui](https://github.com/salvathor/counter_swiftui)

Aplicación de contador desarrollada con SwiftUI para comprender el manejo de estados y la actualización reactiva de interfaces.

Permite practicar:

- `@State`.
- Vistas declarativas con SwiftUI.
- Uso de `VStack`, `HStack`, `Text` y `Button`.
- Modificadores de vistas.
- Animaciones.
- Ciclo de vida mediante `scenePhase`.

### 5.3. Flash Cards

**Repositorio:** [flash_cards](https://github.com/salvathor/flash_cards)

Aplicación de tarjetas de estudio desarrollada con SwiftUI utilizando el patrón arquitectónico MVVM.

Permite practicar:

- Arquitectura MVVM.
- `ObservableObject` y `@Published`.
- `@StateObject`.
- Separación de modelos, vistas y ViewModels.
- Manejo de eventos e interacción.
- Componentes visuales de SwiftUI.

### 5.4. Kotlin Multiplatform

**Repositorio:** [kmp](https://github.com/salvathor/kmp)

Proyecto multiplataforma con aplicaciones Android e iOS que comparten lógica de negocio desarrollada en Kotlin.

Incluye una aplicación básica de administración de tareas.

Permite practicar:

- Kotlin Multiplatform (KMP).
- Separación de lógica compartida y código específico de plataforma.
- Integración de Kotlin con SwiftUI.
- Interfaces mediante repositorios.
- Modelos de datos compartidos.
- Compose Multiplatform.

### 5.5. Fundamentos de UIKit

**Repositorio:** [ejemplo1_UIKit](https://github.com/salvathor/ejemplo1_UIKit)

Proyecto introductorio de desarrollo iOS utilizando UIKit, Swift y Storyboards.

Permite practicar:

- Navegación entre pantallas.
- Paso de información entre vistas.
- `UIViewController`.
- Storyboards y Segues.
- Tablas mediante UIKit.
- Alertas.
- Extensiones de Swift.
- Fundamentos del patrón MVC.

### 5.6. Audio, Video y Gestos con SwiftUI

**Repositorio:** [audio_video_gestos_swiftui](https://github.com/salvathor/audio_video_gestos_swiftui)

Aplicación de ejemplo para trabajar con recursos multimedia y eventos táctiles utilizando SwiftUI.

Permite practicar:

- Reproducción de audio y video.
- `AVPlayer` y `VideoPlayer`.
- Framework AVKit.
- Gestos Tap y Long Press.
- Gestos Drag, Magnification y Rotation.
- Manejo de eventos táctiles.
- Navegación mediante `TabView`.
