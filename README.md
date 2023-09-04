# Proyecto de Interacción con Modelo de Chat

Este proyecto consiste en una aplicación Flask que permite a los usuarios interactuar con un modelo de chat basado en GPT-3.5. El código importa las librerías necesarias y establece una instancia de Flask con dos rutas principales: una que renderiza la plantilla principal y otra que gestiona las interacciones del usuario con el modelo.

## Configuración

Antes de ejecutar la aplicación, es necesario configurar la API key de OpenAI como una variable de entorno para evitar exponer la clave. Asegúrate de establecer la variable de entorno `OPENAI_API_KEY` con tu API key de OpenAI.

## Dependencias

Asegúrate de tener instaladas las siguientes dependencias:

- Flask
- OpenAI Python
- Python 3.x

Puedes instalar estas dependencias usando pip:

```
pip install flask openai
```

## Ejecución

Para ejecutar la aplicación, utiliza el siguiente comando en tu terminal:

```
python app.py
```

Esto iniciará el servidor Flask en el puerto 5000.

## Uso

La aplicación tiene las siguientes rutas:

### Ruta principal ("/")

Esta ruta renderiza la plantilla principal, donde los usuarios pueden interactuar con el modelo de chat.

### Ruta de interacción ("/gpt")

Esta ruta permite a los usuarios enviar sus interacciones con el modelo de chat. La ruta acepta solicitudes POST y GET.

- **Solicitud GET**: Los usuarios pueden enviar sus interacciones con el modelo proporcionando el parámetro `user_input` en la URL. Por ejemplo: `/gpt?user_input=Hola, ¿cómo estás?`. El modelo responderá con la respuesta generada.

- **Solicitud POST**: Los usuarios pueden enviar sus interacciones con el modelo enviando un formulario con el campo `user_input`. El modelo responderá con la respuesta generada.

## Limitaciones

El servidor puede experimentar límites de tasa de solicitud (rate limits) debido al alto volumen de peticiones. En caso de que el servidor esté experimentando un alto volumen de tráfico, se mostrará el mensaje "El servidor está experimentando un alto volumen de peticiones. Vuelva a intentarlo más tarde."

## Licencia

Este proyecto está licenciado bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.