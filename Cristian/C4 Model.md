# ¿Qué es?
1. Un conjunto de [abstracciones jerárquicas](https://c4model.com/abstractions) (sistemas de software, contenedores, componentes y código).
2. Un conjunto de [diagramas jerárquicos](https://c4model.com/diagrams) (contexto del sistema, contenedores, componentes y código).
> [!note] C4 es una historia que debes contar de la manera correcta.
### Contenedores 
Son aplicaciones o almacenes de datos, es decir, algo que necesita deployarse en algún lado.
Por ejemplo: una aplicación como Facebook dentro de un celular.
Se engloba en contenedores el frontend, el backend, otros sistemas que deben **deployarse** y las líneas son la comunicación entre estos contenedores. 
Se contempla la tecnología.
### Componentes
Dentro de los contenedores encontramos a los componentes. 
Es un grupo de cosas que se relacionan entre si de manera armónica 

Refleja la arquitectura de como esta distribuido nuestro código pero a un nivel alto (Como directorios, modulos, COMPONENTES xd).

### Code
Dentro de estos componentes encontramos las clases en codigo

Segun el creador del libro dice que no es recomendable hacer un diagrama de clases al menos de que sea algun componente muy complicado de ver. Estos solo se automatizan a traves de los IDEs

## Notación en C4 
- Titulos: Pequeños y significativos para cada nivel, detalla en pocas palabras que es.
- Layaout: Para indicarte que es cada cosa, aqui tambien van los colores.
- Consistencia visual: como armas las relaciones, como se interactua con lo de afuera y como esto se ve representado.
- Acronimos: tener cuidado ya que algunos no se pueden entender por otros desarrolladores que lean el diagrama, en especial si no estan relacionados con el negocio.
- Elementos (boxes): Todo luce igual, sin embargo, la especificacion debajo de cada cosa (definir un rol, contenedor, componente, sistema) es lo realmente importante. Debajo de esto va una descripcion corta de que hace cada cosa.
![[Pasted image 20250603190142.png]]

- Líneas: deben ser unidireccional y solo muestran la dependencia mas importante entre elementos. Por ejemplo: "La cosa A depende de la cosa B" o "La cosa A llama a la cosa C". Solamente se debe mostrar algo bi direccional cuando la intención es diferente.
![[Pasted image 20250603190515.png]]
![[Pasted image 20250603190745.png]]

- Elementos en general: debes especificar un key legend diciendo que es cada cosa, colores, formas, etc. Ten en cuenta que se pueden usar figuras, pero estas figuras deben dar mas información o reafirmar lo que leo, no complicarme (poner iconos de tecnologías que no sé).
> [!note] Cualquier narrativa que quieras decir de tu diagrama, debe complementarlo más que explicar el que es cada cosa
