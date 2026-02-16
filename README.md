# Automation-Tests

Proyecto de automatización de pruebas funcionales para **API** y **UI**, construido con Java y Maven.  
El objetivo es validar flujos críticos de negocio mediante una suite mantenible, escalable y fácil de ejecutar en entornos locales o de integración continua.

## Resumen del proyecto

Este repositorio está dividido en dos módulos independientes:

- **AutomationApi**: pruebas de servicios REST.
- **AutomationUI**: pruebas de interfaz web sobre escenarios funcionales.

Cada módulo mantiene su propio `pom.xml`, permitiendo ejecutar pruebas de forma aislada o conjunta según la necesidad del equipo.

## Tecnologías utilizadas

- **Java**
- **Maven**
- **JUnit Jupiter**
- **TestNG**
- **REST Assured**
- **Selenium WebDriver**

## Estructura del repositorio

```text
Automation-Tests/
├─ AutomationApi/
│  ├─ pom.xml
│  └─ src/test/java/
│     └─ UsersTest.java
└─ AutomationUI/
	├─ pom.xml
	└─ src/test/java/
		├─ CalculatoraTest.java
		├─ LoginInvalidTest.java
		├─ LogoutTest.java
		└─ TrianguloTest.java
```

## Qué valida este proyecto

### API Testing (`AutomationApi`)

- Validación de endpoints REST.
- Verificación de códigos de estado HTTP.
- Validación de contenido de respuestas.

### UI Testing (`AutomationUI`)

- Flujos de autenticación (login inválido y logout).
- Escenarios funcionales sobre calculadora.
- Escenarios funcionales de triángulos.

## Requisitos

Antes de ejecutar las pruebas, asegúrate de tener instalado:

- **JDK 17+** (recomendado)
- **Maven 3.8+**
- Navegador compatible con Selenium (por ejemplo, Chrome)
- Conexión a internet (si las pruebas consumen servicios externos)

Para validar instalaciones:

```bash
java -version
mvn -version
```

## Ejecución de pruebas

### 1) Ejecutar pruebas de API

```bash
cd AutomationApi
mvn clean test
```

### 2) Ejecutar pruebas de UI

```bash
cd AutomationUI
mvn clean test
```

## Reportes y resultados

Al finalizar, Maven genera resultados en la carpeta `target/` de cada módulo.  
Puedes revisar allí salidas de ejecución, clases compiladas y artefactos de prueba.