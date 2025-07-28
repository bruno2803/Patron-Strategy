🧠 Ejemplo del Patrón Strategy con Spring Boot

Este proyecto demuestra cómo implementar el patrón de diseño Strategy en una aplicación Spring Boot. El objetivo es seleccionar dinámicamente una estrategia (algoritmo o comportamiento) en tiempo de ejecución, eliminando estructuras condicionales como if/else.

🚀 Tecnologías utilizadas

Java 11+
Spring Boot 2.x+
Maven o Gradle

📁 Estructura del proyecto

src/
├─ strategy/              # Interfaz principal y enums
├─ strategy/impl/         # Estrategias concretas
├─ strategy/factory/      # Clase context/factory para seleccionar la estrategia
├─ controller/            # Controlador REST
└─ Application.java       # Clase principal

⚙️ Cómo ejecutar

1. Cloná el repositorio:
git clone https://github.com/yoandypv/spring-strategy-ejemplo.git
cd spring-strategy-ejemplo
3. Ejecutá la app:
mvn spring-boot:run
3. Probá la lógica desde Postman o navegador:
http://localhost:8080/<endpoint>?tipo=CSV

🧩 ¿Cómo funciona?

1. Se define una interfaz común para todas las estrategias.
2. Cada estrategia concreta implementa esa interfaz y se registra como componente.
3. Una clase factory/contexto selecciona la estrategia adecuada según un parámetro (tipo).
4. El controlador delega la lógica a la estrategia seleccionada.

➕ Cómo agregar una nueva estrategia

1. Crear una clase que implemente la interfaz y anotar con @Component.
2. Agregar el nuevo tipo al enum si es necesario.
3. ¡Listo! Spring la detectará automáticamente.

📚 Créditos
Basado en el video de SACAViX Tech y su repositorio original:
https://github.com/yoandypv/spring-strategy-ejemplo

📝 Licencia
Este proyecto es solo con fines educativos y de práctica personal.
