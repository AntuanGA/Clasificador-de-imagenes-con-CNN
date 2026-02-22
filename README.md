# 🐱 [Cats-vs-Dogs]: ¿Es una máquina más lista que un humano (o que yo)?

¿Sabías que este dataset nació para crear esos CAPTCHAS que tanto odiamos? Sí, esos que te preguntan "señala dónde hay un perro" para demostrar que no eres un robot.
Se suponía que una máquina tenía una posibilidad entre 54.000 de resolverlo. Spoiler: He intentado que mi modelo sea ese "uno" entre 54.000 y casi pierdo la cordura en el proceso 😅.

🧠 El Concepto: El fin de los CAPTCHAS
En 2007, un estudio dijo que los humanos resuelven esto el 99,6% de las veces. Yo empecé pensando que sería pan comido, pero cuando te enfrentas a 25.000 imágenes y tu RAM empieza a sudar, la cosa cambia.
Este proyecto no es solo clasificar fotos; es entender cómo una Red Neuronal Convolucional (CNN) empieza a distinguir orejas, bigotes y colas donde antes solo veía píxeles.

🛠️ Mi Stack Tecnológico
- Lenguajes: Python (Pandas, Numpy para la limpieza).
- Deep Learning: TensorFlow & Keras (el corazón del proyecto).
- Procesamiento de imagen: PIL y ImageDataGenerator (mi mejor amigo para no fundir el ordenador). 💻

  🚀 El Flujo de Trabajo (Lo que me hizo trasnochar)
1. La batalla contra la RAM 📉
Si tienes 12GB de RAM, eres el rey. Si no, como yo, tienes que usar trucos. Aprendí a usar flow_from_directory para que Keras lea las imágenes "poquito a poco" desde el disco duro en vez de intentar cargarlas todas de golpe.

2. Poniendo orden en el caos 🧹
Las fotos venían todas mezcladas en una carpeta. Tuve que crear un script para:

 1. Crear carpetas separadas para Entrenamiento y Test.
 2.Mover cada perro y cada gato a su "casita" correspondiente.

3. La Red Neuronal (CNN) 🤖
No quería un modelo "ladrillo" que tardara tres días en entrenar. Diseñé un modelo simplificado que logré ajustar para que fuera eficiente y preciso.

🔍 El "Mapa" de la Red Neuronal: ¿Cómo ve mi IA?

![Mapa de la Red Neuronal](img/mapa-red.png)


💡 Lo que he aprendido
- La organización es el 80% del éxito: Si tus carpetas están mal, tu modelo es ciego. ☕
- Menos es más: A veces, un modelo simplificado con un buen EarlyStopping (parar cuando ya no mejora) es mejor que una red gigante que se sobrecalienta. 🧠
- No te fíes de la primera descarga: Me tocó corregir rutas y lidiar con archivos comprimidos rebeldes. La persistencia es una habilidad técnica. 🚀


📂 Contenido del Repositorio
- dogs-vs-cats.ipynb: El cuaderno donde ocurrió la magia (y los errores).
- data/organized_dataset/: La estructura que Keras necesita para trabajar.
- models/best_simplified_model.keras: Mi modelo ya entrenado y listo para usar.  
