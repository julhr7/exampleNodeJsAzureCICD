# ☁️ Node.js + Azure CI/CD Pipeline Example

Este repositorio contiene una aplicación de ejemplo desarrollada en **Node.js** configurada con un flujo completo de **Integración Continua (CI)** y **Despliegue Continuo (CD)** hacia **Microsoft Azure**. El objetivo del proyecto es servir como plantilla y demostración práctica de cómo automatizar el ciclo de vida del desarrollo de software utilizando prácticas modernas de DevOps.

---

## 🎯 Objetivo del Proyecto

* **Automatización:** Eliminar los despliegues manuales mediante pipelines automatizados.
* **Calidad de Código:** Asegurar que cada cambio en el código pase por pruebas automatizadas antes de llegar a producción.
* **Infraestructura Cloud:** Demostrar el despliegue fluido de una aplicación web en los servicios de Azure (ej. Azure App Service).

---

## ⚙️ Flujo de CI/CD (Pipeline)

El ciclo de vida automatizado configurado en este repositorio sigue los siguientes pasos cada vez que se realiza un *push* o *pull request* a la rama principal (`main`):

1. **Integración Continua (CI):**
   * Descarga del código fuente.
   * Instalación de dependencias de Node.js (`npm install`).
   * Ejecución de pruebas unitarias/integración (`npm test`).
   * Construcción del artefacto de despliegue.

2. **Despliegue Continuo (CD):**
   * Si la fase de CI es exitosa, el artefacto se empaqueta de forma segura.
   * Autenticación automatizada con Microsoft Azure.
   * Despliegue de la nueva versión en el entorno de producción (Azure App Service / Azure Container Apps).

---

## 🚀 Instrucciones de Ejecución Local

Si deseas probar o modificar la aplicación en tu entorno local antes de que el pipeline la despliegue, sigue estos pasos:

### 📋 Requisitos previos
* [Node.js](https://nodejs.org/) (Versión recomendada: LTS)
* [Git](https://git-scm.com/)

### 💻 Pasos para ejecutar

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/julhr7/exampleNodeJsAzureCICD.git](https://github.com/julhr7/exampleNodeJsAzureCICD.git)
   ```

2. **Navegar a la carpeta del proyecto:**
   ```bash
   cd exampleNodeJsAzureCICD
   ```

3. **Instalar dependencias:**
   ```bash
   npm install
   ```

4. **Ejecutar la aplicación en modo desarrollo:**
   ```bash
   npm start
   ```
   *La aplicación estará disponible típicamente en `http://localhost:3000` (o el puerto configurado en tus variables de entorno).*

5. **Ejecutar las pruebas locales:**
   ```bash
   npm test
   ```

---

## ☁️ Configuración de Azure (Despliegue)

*(Nota para el evaluador o usuario que desee replicar el entorno)*
Para que el pipeline de GitHub Actions (o Azure Pipelines) funcione correctamente hacia tu propia cuenta de Azure, necesitas configurar los siguientes secretos en la configuración del repositorio:

* `AZURE_CREDENTIALS`: Credenciales del Service Principal para autenticación.
* `AZURE_WEBAPP_NAME`: Nombre del recurso de App Service en Azure.

---

## 🛠️ Stack Tecnológico y Herramientas

* **Lenguaje:** Node.js / JavaScript (o TypeScript)
* **Framework Web:** Express.js *(Ajustar si usaste otro, como NestJS o Fastify)*
* **Cloud Provider:** Microsoft Azure
* **CI/CD:** GitHub Actions / Azure DevOps Pipelines *(Ajustar según la herramienta utilizada)*
