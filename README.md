# 🍕 Sistema de Gestión de Pizzería

La **pizzería** necesita un sistema para gestionar:

- **Productos:** Pizzas, panzarottis, bebidas, postres, adiciones.
- **Combos, ingredientes, pedidos** y **clientes**.

---

## 🚀 Actividades del Reto

### 1. 🔍 **Investigación** 

#### ¿Qué es una **base de datos NoSQL**?
> Una base de datos NoSQL es una base de datos que no sigue un esquema en especial y tiene como características su: flexibilidad, consistencia, disponibilidad, y escalabilidad, es decir, es más flexible al momento de agregar o editar datos dentro de una base de datos lo que le permite un alto rendimiento.

#### ¿Qué es **MongoDB**?
> Es un sistema de bases de datos escrito en C++ orientado a documentos donde se guarda informacion de tipo clave/valor, es decir, se usa un formato JSON y al ser No Relacional permite que este maneje un esquema libre.

#### ¿Qué diferencia hay entre una **base de datos relacional** (como MySQL) y una **base de datos documental** como MongoDB?
> Las bases de datos Relacionales como MySQL usan tablas que se relacionan entre ellas mediante claves foráneas y son utilizadas en aplicaciones rígidas y relaciones complejas entre tablas, mientras que las bases de datos No Relacionales como MongoDB no utiliza este esquema de relación entre tablas sino que usa colecciones y se usan en aplicaciones web modernas.

#### ¿Qué son **documentos** y **colecciones** en MongoDB?
> Los documentos en MongoDB son la unidad básica de datos y amplían el concepto de base de datos, el cual esta organizado en grupos que se denominan COLECCIONES, estas colecciones son las encargadas de almacenar la información mediante las clave/valor y usa un formato JSON, es decir, un documento MongoDB es el objeto JSON y las colecciones contienen la información que se guarda de tipo clave/valor.

---

### 2. 📝 **Diseñar su propuesta**

**Colecciones**.

#### ¿Qué información tendría un documento de pedido? ¿Y un producto?
> - Productos contienen información del tipo del producto, sus ingredientes, cantidad, precio.
> - Pedidos contiene información del producto como sus ingredientes, tipo de producto, combos, y adicionales. Y  contiene el documento Clientes. 
> - Clientes contiene la información del cliente como ID, nombre, telefono y dirección.

#### Estructura de un documento de pedido
> - **Campos dentro del documento**: ID del cliente, fecha, lista de productos.
> - **Referencias**: Se usan ID como identificador tanto para cliente como para pedidos y productos, Y se referencia el documento clientes para el documento pedidos.

#### Estructura de un documento de producto

> - **Campos dentro del documento**: Nombre, precio, lista de ingredientes y adicionales.
> - **Referencias**:Los ingredientes serían un array de nombres en los que se definen dentro del documento del pedido.

#### Campos: Listas, objetos o documentos incrustados

> - **Listas**Lista de adiciones en un pedido, ingedientes, combos.
> - **Objetos** El cliente dentro de un pedido.
> - **Documentos incrustados** Los pedidos que contienen los productos, los productos que contiene los ingredientes y los clientes que contiene los datos del cliente.

📎 ![Diseño Documentos y Colecciones](/multimedia/Captura%20desde%202025-08-01%2008-18-31.png)

---

### 3. 🧩 **Ejemplos de documentos JSON**

#### pizza con ingredientes
```json
{
  "nombre": "Pizza Campesina",
  "precio": 15.500,
  "ingredientes": ["queso", "maíz dulce", "base tomate", "salchicha"]
}
```
---

 #### pizza con combo
```json
{
  "nombre": "X2 Master Delicia",
  "precio": 24.000,
  "combo": "2 pizzas hawaiana + 2 gaseosas",
  "ingredientes": ["piña", "queso", "base tomate", "salchicha", "jamon"],
  "adicionales": ["gaseosas  postobon"]
}
```

 #### pizza personalizada
```json
{
  "nombre": "Personaliza el antojo",
  "precio": 56.900,
  "combo": "pizza familiar champiñones + 5 gaseosas",
  "ingredientes": ["champiñones", "queso", "base tomate", "salchicha", "jamon"],
  "adicionales": ["gaseosas  postobon","salsas"],
  "personalizado":["Intercambio de ingredientes", "quitar ingredientes","elección sabores","cantidad de cierto ingrediente"]
}
```
## 📌 Reflexión 
#### ¿Qué fue lo más difícil de imaginar sin tablas?
> Lo más díficil de imaginar sin tablas es la desorientación en el momento de querer relacionar datos de un documento con otro o escoger que pertenece a listas, objetos y documentos. Además de la falta de práctica para realizar una base de datos No Relacional. No conocer como diseñar la base de datos.

#### ¿Qué les gustó del enfoque con documentos?
> Su flexibilidad ya que la implementación de datos es más sencilla y no hay necesidad de relacionar continuamente tablas.

#### ¿Qué dudas les surgieron al pensar en este nuevo tipo de base de datos?
> - ¿Cómo se relacionan los documentos?
> - ¿Cómo se generan los objetos dentro de los documentos? 
> - ¿Cómo se organizan las listas?
> - ¿Cómo es el proceso gráfico de diseño?

--- 
## 🤝 Participantes

- **Valentina Delgado**
- **Camila Florez** 
---

## 📜 Contacto GitHub
- https://github.com/ValentinaDelgadoRincon
- https://github.com/CamilaFlorez12