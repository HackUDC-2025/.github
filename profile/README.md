# ArtLens - Guía Interactiva de Museos basada en IA

**Proyecto desarrollado para la HackUDC 2025**

ArtLens es una aplicación móvil diseñada para transformar la experiencia de los visitantes en museos, ofreciendo una guía interactiva y personalizada basada en el contexto del usuario. Utilizando técnicas avanzadas de Inteligencia Artificial, como el reconocimiento de obras de arte y la generación de descripciones enriquecidas, ArtLens se centra en el Museo del Prado, aunque su arquitectura permite su adaptación a otros museos.

## ¿Qué es ArtLens?

ArtLens es una aplicación móvil que actúa como una guía de museo interactiva y personalizada. Su nombre refleja su propósito: ser una "lente" que amplía y enriquece la experiencia del usuario en el museo, utilizando tecnología de inteligencia artificial.

## ¿Qué hace ArtLens? ¿Qué problema resuelve?

ArtLens resuelve el problema de visitar un museo sin una guía o audioguía, ofreciendo una experiencia enriquecida y adaptada al contexto del usuario. Muchas veces, los visitantes no tienen acceso a guías especializadas o no pueden aprovechar al máximo su visita debido a la falta de información contextualizada. ArtLens soluciona esto proporcionando:

- **Descripciones detalladas y personalizadas**: Generadas en tiempo real utilizando IA, adaptadas al contexto del usuario.
- **Audioguías automáticas**: Convierte las descripciones en audio utilizando **gTTS**, ideal para quienes prefieren escuchar en lugar de leer.
- **Recomendaciones personalizadas**: Basadas en las obras que más te interesan, gracias a la búsqueda de embeddings con **Milvus**.

ArtLens no solo te informa sobre las obras de arte, sino que lo hace de una manera adaptada a tus intereses y necesidades, enriqueciendo tu experiencia en el museo.

## ¿De qué depende ArtLens? ¿Qué necesito para instalarlo y usarlo?

Para instalar y ejecutar ArtLens, sigue los siguientes pasos:

1. **Clona los repositorios**:
   - Frontend: [https://github.com/HackUDC-2025/Frontend](https://github.com/HackUDC-2025/Frontend)
   - Backend: [https://github.com/HackUDC-2025/Backend](https://github.com/HackUDC-2025/Backend)

2. **Levanta los servicios con Docker**:
   - Asegúrate de tener Docker y Docker Compose instalados.
   - Ejecuta los siguientes comandos para levantar los servicios de **Ollama** y **Milvus**:
     ```bash
     docker-compose up -d
     ```

3. **Configura y ejecuta el frontend y backend**:
   - Sigue las instrucciones detalladas en los respectivos repositorios para configurar y ejecutar tanto el frontend como el backend.

## ¿Cómo funciona ArtLens?

ArtLens utiliza una combinación de tecnologías de IA para ofrecer una experiencia única:

1. **Reconocimiento de obras de arte**: Usamos el modelo **CLIP** para identificar obras de arte en tiempo real a través de la cámara del dispositivo móvil.
2. **Generación de descripciones**: Empleamos el modelo abierto **LLama 3.2** (con licencia Apache 2.0 modificada) para generar descripciones contextualizadas y enriquecidas de las obras.
3. **Retrieval de embeddings**: Con **Milvus**, realizamos búsquedas eficientes de embeddings para encontrar obras similares basadas en tus intereses.
4. **Text-to-Speech**: Integramos **gTTS** para convertir las descripciones en audio, permitiendo la creación de audioguías personalizadas.

## ¿Qué funciona y qué no funciona?

### Lo que funciona:
- Todas las funcionalidades principales están implementadas y funcionan correctamente:
  - Reconocimiento de obras de arte.
  - Generación de descripciones contextualizadas.
  - Conversión de texto a audio para audioguías.
  - Mantenimiento de búsquedas históricas.

### Lo que no funciona (o tiene limitaciones):
- **Cobertura limitada de obras**: Actualmente, ArtLens no incluye todas las obras del Museo del Prado. Esto se debe a la falta de un conjunto de datos oficial, por lo que hemos utilizado técnicas de web scraping para recopilar información sobre una pequeña parte de las obras. Estamos trabajando para ampliar esta cobertura en futuras versiones.

## ¿Dónde puedo preguntar si encuentro un problema o tengo dudas?

Si encuentras algún problema o tienes preguntas, puedes:
- Abrir una **issue** en el repositorio correspondiente (Frontend o Backend).
- Enviar un correo electrónico a los creadores del proyecto:
  - Alejandro Dopico: alejandro.dopico2@udc.es
  - Mario Diez: mario.diez@udc.es
  - Antón Canzobre: antoncanzobremar@gmail.com

## ¿Cómo puedo contribuir?

¡Nos encantaría que contribuyas a ArtLens! Para hacerlo, sigue estos pasos:
1. Haz un fork del repositorio.
2. Crea una nueva rama con el nombre de tu funcionalidad (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -am 'Añade nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un **Pull Request** para que revisemos tus cambios.

También puedes contactar directamente con los creadores del proyecto para discutir ideas o colaboraciones.

## ¿Quién ha contribuido?

ArtLens ha sido desarrollado por los tres miembros del equipo durante el evento de la HackUDC 2025:
- Alejandro Dopico
- Mario Diez
- Antón Canzobre

## ¿Qué licencia tiene ArtLens?

ArtLens está bajo la licencia **MIT**. Elegimos la licencia MIT porque es simple, permisiva y ampliamente aceptada en la comunidad open source. Permite que otros usen, modifiquen y distribuyan nuestro código sin restricciones, lo que fomenta la adopción y colaboración. Además, es compatible con las licencias de nuestras dependencias, como Milvus (Apache 2.0) y Angular (MIT). Aunque consideramos Apache 2.0 y GPL, la MIT se alinea mejor con nuestros objetivos de maximizar la adopción y mantener la simplicidad del proyecto.

## Agradecimientos

Agradecemos a todos los colaboradores, patrocinadores y a la organización de la HackUDC 2025 por hacer posible este proyecto.
