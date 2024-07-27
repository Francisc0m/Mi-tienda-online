<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Tienda Online</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Mi Tienda Online</h1>
        <nav>
            <ul>
                <li><a href="#">Inicio</a></li>
                <li><a href="#">Productos</a></li>
                <li><a href="#">Carrito</a></li>
                <li><a href="#">Contacto</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section>
            <h2>Bienvenidos a Mi Tienda Online</h2>
            <p>Encuentra los mejores productos al mejor precio.</p>
        </section>
        <section id="productos">
            <!-- Aquí se cargarán los productos -->
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Mi Tienda Online</p>
    </footer>
    <script>
        document.addEventListener("DOMContentLoaded", () => {
            const productos = [
                { id: 1, nombre: "Producto 1", precio: 10.99 },
                { id: 2, nombre: "Producto 2", precio: 20.99 },
                { id: 3, nombre: "Producto 3", precio: 15.99 },
                { id: 4, nombre: "Producto 4", precio: 25.99 }
            ];

            const productosSection = document.getElementById("productos");
            
            productos.forEach(producto => {
                const productoDiv = document.createElement("div");
                productoDiv.className = "producto";
                productoDiv.innerHTML = `
                    <h3>${producto.nombre}</h3>
                    <p>Precio: $${producto.precio.toFixed(2)}</p>
                    <button>Añadir al carrito</button>
                `;
                productosSection.appendChild(productoDiv);
            });
        });
    </script>
</body>
</html> 

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

nav ul {
    list-style-type: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 10px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

main {
    padding: 20px;
}

main h2 {
    text-align: center;
}

#productos {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.producto {
    background-color: white;
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 10px;
    margin: 10px;
    width: 200px;
    text-align: center;
}

.producto h3 {
    margin: 0 0 10px;
}

.producto p {
    margin: 0 0 10px;
    color: #333;
}

.producto button {
    background-color: #28a745;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    border-radius: 4px;
}

.producto button:hover {
    background-color: #218838;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}
