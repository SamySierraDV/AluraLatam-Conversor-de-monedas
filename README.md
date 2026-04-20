
 💱 Conversor de Monedas

![Java](https://img.shields.io/badge/Java-17+-orange?style=flat-square&logo=java)
![JSON](https://img.shields.io/badge/Storage-JSON-blue?style=flat-square)
![API](https://img.shields.io/badge/API-ExchangeRate-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> Aplicación de consola en Java que consume una API de tasas de cambio en tiempo real,
> permite convertir entre divisas populares y persiste los resultados en formato JSON.

---

## ✨ Funcionalidades

| Conversión | Dirección |
|---|---|
| 🇺🇸 USD ↔ 🇦🇷 ARS | Dólar ↔ Peso Argentino |
| 🇺🇸 USD ↔ 🇧🇷 BRL | Dólar ↔ Real Brasileño |
| 🇺🇸 USD ↔ 🇨🇴 COP | Dólar ↔ Peso Colombiano |

- 🔄 Tasas de cambio actualizadas en tiempo real vía API externa
- 🖥️ Resultados mostrados en consola de forma clara
- 💾 Historial de conversiones exportado a archivo `.json`
- 🚪 Cierre automático tras guardar resultados

---

## 🏗️ Arquitectura del Proyecto
conversor-monedas/
│
├── src/
│   
├── Main.java               # Punto de entrada, menú interactivo y flujo principal
│   
├── ConsultaApi.java        # Conexión HTTP a la API de divisas
│   
├── ResultadoDelCambio.java # Record: almacena tasa y monto convertido
│   └── GeneradorDeJson.java    # Serialización y escritura del historial JSON
│
└── README.md

### 📦 Clases principales

**`Main.java`**
Coordina la interacción con el usuario: solicita monedas, monto y delega
la lógica a `ConsultaApi`. Gestiona el menú con 7 opciones.

**`ConsultaApi.java`**
Realiza la petición HTTP a la API externa con moneda base y objetivo.
Retorna un objeto `ResultadoDelCambio` con los datos de la conversión.

**`GeneradorDeJson.java`**
Gestiona la escritura del historial de conversiones en un archivo `.json`
estructurado y legible.

**`ResultadoDelCambio.java`** *(record)*
Almacena tasa de cambio y monto resultante. Expone los métodos:
- `mostrarResultado()` → imprime en consola
- `almacenarResultado()` → agrega a la lista de historial

---

## ⚙️ Requisitos

- ☕ **Java 17** o superior
- 🔑 **API Key** válida de un proveedor de tasas de cambio
  (ej. [ExchangeRate-API](https://www.exchangerate-api.com/))
- 📦 `HttpClient` nativo de Java (sin dependencias externas)

---

## 🚀 Instalación y uso

```bash
# 1. Clona el repositorio
git clone https://github.com/SamySierraDV/AluraLatam-Conversor-de-monedas.git

# 2. Abre el proyecto en IntelliJ IDEA

# 3. Ejecuta Main.java

# 4. Ingresa tu API Key cuando se solicite

# 5. Selecciona una opción del menú (1–7)
#    → Opción 7: guarda el historial en JSON y cierra el programa
```

---

## 🤝 Créditos

Desarrollado por **Samy Sierra Suarez** como parte del challenge
**Oracle Next Education (ONE) G9 – Back End** con Alura Latam. [[3](https://github.com/FARNIKS/Conversor-de-moneda)]

---

## 📄 Licencia

Este proyecto es de uso educativo y libre distribución.
