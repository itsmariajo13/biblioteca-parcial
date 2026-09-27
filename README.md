# Parcial I - Programación II: Sistema de Gestión de Biblioteca

## Integrantes
* María José Peña Montaño
* juan Alejandro Narvaez 

---

### 1. Situaciones en las que no se podría realizar la herencia

#### Situación A: Clases declaradas como `final`
* **Fragmento de código de falla:**
  ```java
  public final class Libro {
      // Atributos y métodos base
  }
  
  // Al intentar heredar:
  public class Novela extends Libro { 
      // Error de compilación: Cannot inherit from final Libro
  }

  ### 2. Nuevos atributos y método adicional propuestos

* **Nuevos Atributos:**
  1. `isbn` (Tipo `String`): Código identificador único internacional del libro.
  2. `ubicacionEstante` (Tipo `String`): Ubicación física exacta del libro en la biblioteca.

* **Método Adicional:**
  ```java
  public boolean verificarDisponibilidad() {
      return this.ejemplaresPrestados < this.totalEjemplares;
  }
