# 🏦 KonradBank - Cajero Automático

<div align="center">

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Swing](https://img.shields.io/badge/Swing-GUI-blue?style=for-the-badge)

**Sistema de Cajero Automático desarrollado como proyecto académico**

*Fundación Universitaria Konrad Lorenz*

</div>

---

## 📋 Descripción

KonradBank es una aplicación de escritorio que simula el funcionamiento de un cajero automático (ATM). Desarrollada en Java con interfaz gráfica Swing, permite a los usuarios realizar operaciones bancarias básicas como depósitos y retiros de dinero.

## ✨ Características

- 🔐 **Autenticación segura**: Validación de tarjeta mediante algoritmo de Luhn y PIN
- 💰 **Depósitos**: Permite agregar fondos a la cuenta
- 💸 **Retiros**: Permite extraer fondos de la cuenta con validación de saldo
- 📊 **Recibo de transacción**: Muestra resumen detallado de cada operación
- 🎨 **Interfaz intuitiva**: GUI amigable y fácil de usar
- 🏦 **Tipos de cuenta**: Soporte para cuentas de ahorro y corriente

## 🏗️ Arquitectura

El proyecto sigue el patrón de diseño **MVC (Modelo-Vista-Controlador)**:

```
src/
└── co/edu/konradlorenz/
    ├── controller/          # Controladores
    │   ├── AplMain.java     # Punto de entrada de la aplicación
    │   └── Controlador.java # Lógica de negocio principal
    ├── model/               # Modelos de datos
    │   ├── Cliente.java     # Datos del cliente
    │   ├── Cuenta.java      # Clase abstracta de cuenta
    │   ├── Ahorro.java      # Cuenta de ahorro
    │   ├── Corriente.java   # Cuenta corriente
    │   ├── Cajero.java      # Lógica del cajero
    │   └── Tarjeta.java     # Interfaz de validación de tarjeta
    └── view/gui/            # Interfaz gráfica
        └── KonradBank.java  # Ventana principal con Swing
```

## 📦 Requisitos

- **Java JDK 11** o superior
- Soporte para `java.desktop` module (incluido en JDK estándar)

## 🚀 Instalación y Ejecución

### Opción 1: Desde línea de comandos

```bash
# Clonar el repositorio
git clone https://github.com/13rianVargas/KonradBank.git
cd KonradBank

# Crear directorio de salida
mkdir -p bin

# Compilar (Linux/macOS)
find src -name "*.java" | xargs javac -d bin

# Compilar (Windows PowerShell)
# Get-ChildItem -Recurse -Filter *.java src | ForEach-Object { javac -d bin $_.FullName }

# Ejecutar
java -cp bin co.edu.konradlorenz.controller.AplMain
```

### Opción 2: Desde un IDE

1. Importa el proyecto en tu IDE preferido (Eclipse, IntelliJ IDEA, NetBeans)
2. Ejecuta la clase `AplMain.java` ubicada en `src/co/edu/konradlorenz/controller/`

## 🧪 Credenciales de Prueba

El sistema incluye datos de prueba precargados. Puedes usar las siguientes credenciales:

| Nombre | Número de Tarjeta | PIN | Saldo Inicial | Tipo de Cuenta |
|--------|------------------|-----|---------------|----------------|
| Pepito Pérez | 4539 1488 0343 6467 | 1234 | $10,000,000 | Ahorro |
| Ana Torres | 6011 1111 1111 1117 | 4567 | $500,000 | Ahorro |
| Luis Fernández | 5105 1051 0510 5100 | 8910 | $1,000,000 | Corriente |
| Mariana Gómez | 4111 1111 1111 1111 | 2468 | $300 | Corriente |
| Isolda Tristán | 3782 822463 10005 | 9102 | $50,000,000 | Corriente |

> ⚠️ **Nota**: Las tarjetas utilizan el algoritmo de Luhn para validación. Los números de tarjeta inválidos serán rechazados.

## 🛠️ Tecnologías Utilizadas

- **Lenguaje**: Java 11+
- **GUI**: Java Swing
- **Arquitectura**: MVC (Model-View-Controller)
- **Validación**: Algoritmo de Luhn para tarjetas de crédito

## 📸 Vista Previa

La aplicación presenta una interfaz de cajero automático con:
- Pantalla de inicio de sesión
- Menú principal con opciones de depósito y retiro
- Pantalla de transacción con confirmación
- Recibo digital con detalles de la operación

## 👥 Contribuidores

Desarrollado como proyecto académico por estudiantes de la **Fundación Universitaria Konrad Lorenz**.

## 📄 Licencia

Este proyecto es de uso académico y educativo.

---

<div align="center">

**⭐ Si te fue útil este proyecto, no olvides darle una estrella ⭐**

</div>