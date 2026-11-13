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
Ejemplo básico del uso de Combine

**Conceptos:**
- Swift Data
- Persistencia de datos
- Combine
- Programación Reactiva

### 1.7. Módulos SwiftUI con MVVM

**Repositorio:** [ModulosSwiftUI](https://github.com/salvathor/ModulosSwiftUI)

Aplicación de ejemplo que muestra cómo organizar una app por funcionalidades con MVVM, inyección de dependencias y fábricas de vistas. Permite consultar usuarios, revisar sus datos, ver su ubicación en un mapa, obtener la posición del dispositivo y calcular una ruta en automóvil hacia el usuario seleccionado.

**Conceptos:**
- MVVM (Model–View–ViewModel).
- Inyección de dependencias mediante un contenedor (`DIContainer`).
- Fábricas de vistas (`Factory`) por módulo.
- Repositorios y protocolos con implementación de datos en memoria.
- `ObservableObject`, `@Published` y `@StateObject`.
- `NavigationStack` y flujo Usuarios → Detalle → Ubicación.
- Core Location: permisos, `CLLocationManager` y callbacks del delegado.
- MapKit: mapas, marcadores, rutas y tiempo estimado.
- `async/await` para el cálculo de rutas.
- Kingfisher (`KFImage`) para imágenes remotas.
- Pruebas unitarias con Swift Testing y pruebas de interfaz.

### 1.8. VIPER con SwiftUI

**Repositorio:** [VIPER-SwiftUI](https://github.com/salvathor/VIPER-SwiftUI)

Ejemplo de cómo implementar la arquitectura VIPER en una app SwiftUI. La app carga de forma asíncrona una lista de productos y permite abrir una vista de detalle para cada uno.

**Conceptos:**
- Arquitectura VIPER: View, Interactor, Presenter, Entity y Router.
- View (`ProductListView`, `ProductDetailView`): muestra el estado y envía eventos al Presenter, sin lógica de negocio.
- Interactor (`ProductInteractorProtocol`, `ProductInteractor`): lógica de negocio y acceso a datos, sin conocer la interfaz.
- Presenter (`ProductListPresenter`): solicita datos al Interactor y publica el estado que dibuja la View.
- Entity (`Product`): modelo de datos.
- Router (`ProductRouter`): ensambla módulos mediante inyección de dependencias y gestiona la navegación.
- Inyección de dependencias por protocolos, para usar un Interactor simulado en pruebas.
- `@MainActor` en el Presenter y `@StateObject` en la View.
- `async/await` y `NavigationStack` con `navigationDestination`.

### 1.9. Aprender pruebas con XCTest

**Repositorio:** [Pruebas](https://github.com/salvathor/Pruebas)

Proyecto didáctico con seis pruebas unitarias y una prueba de interfaz escritas con XCTest. La app muestra formularios de acceso, registro y recuperación, todos de demostración, sin autenticación real ni conexión a un servidor.

**Conceptos:**
- Diferencia entre pruebas unitarias y pruebas de interfaz (UI).
- XCTest, `XCTestCase` y `XCTAssert…`.
- Patrón Arrange, Act y Assert (AAA) y el objeto bajo prueba (`sut`).
- Ciclo de vida de una prueba: `setUpWithError` y `tearDownWithError`.
- Aserciones: `XCTAssertEqual`, `XCTAssertTrue`, `XCTAssertNotNil` y `XCTUnwrap`.
- Manejo de opcionales en pruebas.
- `XCUIApplication`, `waitForExistence`, `isHittable` y `continueAfterFailure`.
- Ejecución e interpretación de resultados en Xcode (⌘U y navegador de pruebas).
- Ejercicios propuestos: división entre cero, búsqueda sin coincidencia y precios decimales.

### 1.10. Contador con MVVM

**Repositorio:** [Contador-MVVM](https://github.com/salvathor/Contador-MVVM)

Aplicación de ejemplo con SwiftUI que muestra un contador que inicia en cero y un botón **Incrementar**. Sirve para entender cómo separar el modelo de dominio, la vista y la coordinación del estado.

**Conceptos:**
- MVVM (Model–View–ViewModel).
- Modelo inmutable (`Contador`) cuyo método `incrementar()` devuelve una nueva instancia.
- Lógica de dominio independiente de SwiftUI, por lo que puede probarse sin interfaz.
- `ObservableObject` y `@Published` (Combine).
- `private(set)` para limitar quién puede modificar el estado.
- `@MainActor` en el ViewModel.
- `@StateObject` para conservar el ViewModel en la vista.
- Flujo de una interacción: vista → ViewModel → modelo → `@Published` → actualización de la vista.
- Punto de entrada con `@main` y bloques `#Preview` y `#Playground`.

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
