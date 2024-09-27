# 🏠 MOC

## 📝 Planificación General
- El objetivo principal de este proyecto es establecer un entorno de desarrollo estándar utilizando Docker.
- Asegurando una configuración reproducible y eficiente en Windows, Mac y Linux.
- El deploy del back-end (API) se realizará en un servidor con **Debian Linux**, garantizando estabilidad y compatibilidad con los servicios requeridos.
## 📊 Partes del Proyecto
- **Cliente**: Dependiendo del framework que utilicen en el front-end, podríamos optar por Vercel u otras plataformas como Netlify. La elección dependerá de las características específicas del framework y de las necesidades del proyecto.
- **Servidor**: Mi recomendación es dockerizar el back-end. Algunos motivos clave para dockerizar una aplicación en Java Spring Boot incluyen
	- Portabilidad: Docker garantiza que la aplicación se ejecute de la misma manera en cualquier entorno, ya sea local o en producción.
	- Aislamiento: Docker aísla la aplicación y sus dependencias, evitando conflictos con otras aplicaciones en el servidor.
	- Escalabilidad: Facilita la escalabilidad al poder crear múltiples instancias de contenedores y distribuir la carga de manera eficiente.
	- Facilidad en el Despliegue: Docker simplifica el proceso de despliegue, reduciendo los tiempos y minimizando los errores humanos.
	- Consistencia del Entorno: Asegura que todos los entornos (desarrollo, pruebas y producción) sean consistentes, lo que reduce problemas relacionados con configuraciones específicas de cada entorno.
- **GitHub Actions**: para implementar tanto la Integración Continua (CI) como el Despliegue Continuo (CD).
- **CI**: Esta parte quedará pendiente por ahora para no dilatar el desarrollo, ya que se requiere definir los tests automáticos y el flujo de integración adecuada.
- **CD**: Esta parte es crucial, ya que permitirá que, cada vez que se realice un merge en la rama de _production_, se despliegue automáticamente la aplicación. Esto asegura un flujo de trabajo eficiente y evita retrasos en el despliegue manual.

## 🏛️ Arquitectura
![Imgur](https://i.imgur.com/958uNgW.png)
## 🛠️ Todo
- ### **Cliente** (Front-end)
	- [ ] Evaluar las opciones para el despliegue del front-end:
	  - [ ] Considerar **Vercel**.
	  - [ ] Considerar **Netlify**.
	  - [ ] Elegir la plataforma de despliegue adecuada según el framework. 
- ### **Servidor** (Back-end)
	- [ ] Crear el Dockerfile para la aplicación Java Spring Boot.
	- [ ] Configurar el entorno de desarrollo local con Docker y Docker-compose.
	- [ ] Probar la portabilidad de la aplicación en entornos locales y en producción.
	- [ ] Configurar la instancias para el despliegue del back-end.
	- [ ] Automatizar el proceso de despliegue mediante Makefile.
	- [ ] Asegurar la consistencia del entorno en desarrollo, pruebas y producción.
	- [ ] Configurar una capa de seguridad para el https con Nginx.
- ### **Configuración de CI/CD**:
	- [ ] Implementar Despliegue Continuo (CD) en GitHub Actions:
	  - [ ] Configurar el workflow para que se despliegue automáticamente al hacer un merge en la rama de _production_.
	  - [ ] Asegurarse de que el despliegue sea estable al hacer un pull request.
	- [ ] Definir el pipeline para Integración Continua (CI) (pendiente):
	  - [ ] Crear los tests automáticos para validar el código antes del merge.
	  - [ ] Definir el flujo de integración con DockerHub.
- ### **Tareas Diarias**
	- [ ] Introducir al equipo en el uso de Docker y resolver dudas que surjan.
	- [ ] Asegurar que cada miembro del equipo tenga un entorno de trabajo configurado correctamente.
- ### **Tareas Semanales**
	- [ ] Revisión y mejora de la dockerización de la aplicación Java Spring Boot.
- ### **Objetivos a Largo Plazo**
	- [ ] Completar la configuración de **CI/CD** para el despliegue automatizado y las pruebas automáticas.
	- [ ] Crear un entorno de desarrollo y despliegue robusto y sostenible junto con DockerHub.
	- [ ] Asegurar la escalabilidad y estabilidad de la aplicación en producción aplicando Kubernetes.
	- [ ] Monitoreo de la aplicación.
## 🗂️ Notas
- El mínimo recomendado de RAM para usar Docker en Windows, Linux o Mac es de 8 GB pero seria genial tener 16 GB. Esto garantiza un funcionamiento fluido del entorno Docker y de las aplicaciones que se ejecuten en contenedores (Front-end).
- Para el despliegue en producción, se recomienda utilizar al menos una instancia EC2 mínima que soporte la carga esperada en desarrollo.
- Vercel es una excelente opción para el despliegue del front-end, especialmente si se utiliza un framework como React o Next.js, que están optimizados para esta plataforma.
- Se puede considerar el uso de tunneling (túneles) con ngrok para exponer localmente aplicaciones tanto del front-end como del back-end a internet, facilitando el desarrollo y las pruebas sin necesidad de realizar despliegues en producción.
## 📅 Calendario
- Del 2024-09-30
- Primera Semana: Introducción a Docker, Front-end
- Segunda Semana: Dockerizar Back-end con Docker-Compose
- Tercera Semana: GitHub Actions (CD, Setup de Instancia)
- Cuarta Semana: Testeo del flow y seguimiento del personal.
- Hasta el 2024-10-30
## 💰 Costos
- ### **Requisitos de Hardware (Local)**
	*   **RAM**: Mínimo recomendado de **16 GB**.
	*   **CPU**: Al menos **2 núcleos**.
	*   **Almacenamiento**: Al menos **50 GB** de espacio libre en disco.
- ### **Costos de Hosting (Nube)**
	**Instancia mínima** (por ejemplo, una instancia t2.micro en AWS o una Droplet básico en DigitalOcean):
    *   **AWS**: $8 - $10/mes (t2.micro con 1 GB de RAM).
    *   **DigitalOcean**: $5/mes (Droplet básico con 1 GB de RAM).

- ### **Vercel**
	*   Plan gratuito disponible con límites, ideal para proyectos pequeños.
	*   Plan Pro: aproximadamente **$20/mes** por equipo, ideal para proyectos en producción.
- ### **Costos del Desarrollo**
	*  DevOps: 3 horas diarias (8:00 AM - 11:00 AM) en 4 semanas a $ 10.00 USD/Hora = $ 600.00 USD
	
- ### **Resumen de Costos Mínimos Estimados**
| Concepto                       | Dev. Aprox. | Prod. Aprox  |
| ------------------------------ | ----------- | ------------ |
| **Instancia en la Nube** (AWS) | $ 0/mes     | $ 10/mes     |
| **Total**                      | **$ 0/mes** | $ 10/mes<br> |
| DevOps (01 mes)                | $ 600.00    |              |
