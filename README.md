
# E-Commerce con React JS - De Ascentiis Maximiliano para CODERHOUSE 2022

 [Sitio Web] 
  Este sitio es un proyecto que esta basado en un E-commerce hecho con React JS. Orientado a una tienda de prendas y accesorios deportivos.



• Incluye los siguientes componentes:

- _NavBar_ : Este mismo nos otorga la navegabilidad de nuestro sitio, logrando representar nuestro cátalogo con nuestros productos, por su marca y por el tipo de articulo(zapatilla,accesorio,remera,campera) como tambien nos permite navegar a nuestro carrito de compras.
- _Brand_: Es una representacion del logo de nuestra E-commerce, en todo momento es visible y gracias a este podemos dirigirnos al home de nuestro sitio.
- _ItemListContainer_: Es un componente contenedor y su funcion es contener a todos nuestros productos que estan dentro de _ItemList_(explicado mas adelante)
- _ItemList_: Este componente es uno contenedor, pero a diferencia de _ItemListContainer_ este tiene una logica incorporada que nos permite mostrar nuestros productos a traves del componente _Item_ dependiendo la categoria asignada(marca o tipo de articulo) Y si no hay ninguna, entonces representa todos nuestros productos sin filtrar.
Este componente contiene a _Item_ y a _Loader_(Como su nombre lo indica su funcion es representar un Loader) . _Loader_ Solo aparace mientras nuestro array de productos carga.
-_Item_: Componente presentacional que se dedica a mostrar un producto.
-_ItemDetailContainer_: Componente contenedor que filtra nuestro array de productos segun el parametro(id del producto) recibido. Contiene a _ItemDetail_ que va a representar el producto filtrado.
- _ItemDetail_: Se encarga de representar el detalle de nuestro producto filtrado anteriormente por _ItemDetailContainer_. Contiene a su vez dos componentes: _ItemCount_ y _Sizes_: Componente creado con la finalidad de quitarle tarea extra a nuestro componente _ItemDetail_. Este mismo mapea nuestro array de talles del producto.
- _ItemCount_: Gracias a este componente el usuario puede seleccionar la cantidad de productos que desea. Este mismo recibe como prop una funcion que al ejecutarse cambia el estado de su padre(_ItemDetail_) provocando dejar de hacer visible a _ItemCount_ y a su vez añade el producto al carrito.
- _CartList_: Este componente representa nuestro carrito de compras , mostrando cada producto a traves de _CartItem_. Teniendo funcionalidades como mostrar el total de nuestro carrito y el total de cada producto, asi como tambien nos permite eliminar por producto o vaciar nuestro carrito, todo esto gracias a nuestro _useCartContext_(Se explica mas adelante). Una vez que el usuario decida terminar su compra entonces se hará visible nuestro componente _Form_.
- _CartItem_: Componente dedicado a representar los datos del producto dentro del carrito.
- _Form_: Componente que ademas de contener un formulario, gracias a su logica logra crear validaciones para cada input correspondiente, ayudado por un Hook(_useForm_) que contiene las funciones de los input segun sus eventos. 
- _CartContext_: Esto no es un componente, Es un Contexto que nos ayuda a proveer las funciones para modificar el arrray de productos de nuestro carrito, editando el contenido de nuestro carrito desde cualquier parte de nuestra _App_(En este caso) En este caso usado en _CarList_ y _ItemDetail_.


• Tech
En este proyecto de React js se utiliaron las siguientes librerias


-react : utilizada para crear interfaces de usuario con el objetivo de facilitar el desarrollo de aplicaciones en una sola página a traves de componentes.

-firebase: Se utiliza junto con Firestore para proveerle a nuestro sitio una base de datos, pudiendo administrar nuestros productos y ordenes de nuestros clientes sin necesariamente utilizar tecnologica BackEnd.

-react-router-dom: Utilizada para el enrutamiento de nuestro sitio, haciendolo navegable🚀.

-react-icons: Utilizada para proveer iconos a nuestro proyecto



   [Sitio Web]: https://codersport.netlify.app/
   [react]: https://reactjs.org/
   [firebase]: https://firebase.google.com/
   [react-router-dom]: https://reactrouter.com/
   [react-icons]: https://react-icons.github.io/react-icons/
   [firestore]: https://cloud.google.com/firestore?hl=es
   [react-dom]: https://es.reactjs.org/docs/react-dom.html
