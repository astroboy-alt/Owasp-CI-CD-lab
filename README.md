# OWASP CI/CD Lab

## Descripción

Este repositorio contiene una instancia de la aplicación vulnerable **OWASP Juice Shop**, utilizada como entorno de pruebas para actividades de análisis de vulnerabilidades, remediación de dependencias y automatización de controles de seguridad dentro de un pipeline de CI/CD.

La aplicación fue tomada como base del proyecto OWASP Juice Shop y adaptada para su uso en este laboratorio académico.

---

## Requisitos Previos

Antes de ejecutar la aplicación, asegúrese de contar con los siguientes componentes instalados:

### Git

Permite clonar el repositorio desde GitHub.

Verificar instalación:

```bash
git --version
```

### Docker

Docker será utilizado para desplegar la aplicación dentro de un contenedor aislado.

Verificar instalación:

```bash
docker --version
```

### Docker Compose (Opcional)

Verificar instalación:

```bash
docker compose version
```
Si requiere instalar docker puede consultar la guia en el siguiente enlace: https://www.docker.com/
---

## Clonar el Repositorio

Clonar el repositorio localmente:

```bash
git clone https://github.com/astroboy-alt/Owasp-CI-CD-lab.git
```

Ingresar al directorio del proyecto:

```bash
cd Owasp-CI-CD-lab
```

---

## Levantar la Aplicación Utilizando Docker

### Opción 1: Construir la imagen localmente

Desde la raíz del proyecto ejecutar:

```bash
docker build -t owasp-ci-cd-lab .
```

Una vez finalizada la construcción:

```bash
docker run --rm -p 3000:3000 owasp-ci-cd-lab
```

### Opción 2: Utilizando Docker Compose

Si el proyecto incluye un archivo `docker-compose.yml`, ejecutar:

```bash
docker compose up -d
```

Verificar que el contenedor se encuentre en ejecución:

```bash
docker ps
```

---

## Acceso a la Aplicación

Una vez desplegada correctamente, abrir un navegador web y acceder a:

```text
http://localhost:3000
```

Si la aplicación se encuentra ejecutándose en una máquina virtual o entorno remoto, sustituir `localhost` por la dirección IP correspondiente.

---

## Verificación del Despliegue

Para comprobar que el contenedor se encuentra activo:

```bash
docker ps
```

Debería observarse un contenedor asociado a la aplicación ejecutándose y exponiendo el puerto 3000.

Para consultar los registros:

```bash
docker logs <container-id>
```

---

## Detener la Aplicación

Si se ejecutó mediante Docker:

```bash
docker stop <container-id>
```

Si se ejecutó mediante Docker Compose:

```bash
docker compose down
```

---

## Objetivo del Laboratorio

Este repositorio se utiliza para realizar actividades relacionadas con:

* Análisis de vulnerabilidades en dependencias.
* Gestión de CVE.
* Automatización de controles de seguridad.
* Integración continua (CI).
* Entrega continua (CD).
* Pruebas de herramientas DevSecOps.
* Remediación de vulnerabilidades mediante actualización de componentes.

---

## Referencias

* OWASP Juice Shop: https://owasp.org/www-project-juice-shop/
* Docker: https://www.docker.com/
* GitHub: https://github.com/

---

## Autor

Repositorio utilizado para fines académicos dentro del laboratorio de CI/CD y DevSecOps.
