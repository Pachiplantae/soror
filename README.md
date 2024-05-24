# soror
Red mundial de mujeres 
my-website/
│
├── index.html
├── styles.css
└── script.js
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Página Web</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Inicio</a></li>
                <li><a href="#about">Sobre Nosotros</a></li>
                <li><a href="#services">Servicios</a></li>
                <li><a href="#contact">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section id="home">
            <h1>Bienvenidos a Mi Página Web</h1>
            <p>Este es un sitio web de ejemplo.</p>
        </section>
        
        <section id="about">
            <h2>Sobre Nosotros</h2>
            <p>Aquí puedes escribir información sobre tu empresa o proyecto.</p>
        </section>
        
        <section id="services">
            <h2>Servicios</h2>
            <p>Descripción de los servicios que ofreces.</p>
        </section>
        
        <section id="contact">
            <h2>Contacto</h2>
            <form id="contact-form">
                <label for="name">Nombre:</label>
                <input type="text" id="name" name="name" required>
                
                <label for="email">Correo Electrónico:</label>
                <input type="email" id="email" name="email" required>
                
                <label for="message">Mensaje:</label>
                <textarea id="message" name="message" required></textarea>
                
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2024 Mi Página Web. Todos los derechos reservados.</p>
    </footer>
    
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #333;
    color: white;
    padding: 1rem;
}

nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: space-around;
}

nav ul li {
    display: inline;
}

nav ul li a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
}

nav ul li a:hover {
    background-color: #575757;
}

main {
    padding: 2rem;
}

section {
    margin-bottom: 2rem;
}

form {
    display: flex;
    flex-direction: column;
}

form label {
    margin: 0.5rem 0 0.2rem 0;
}

form input, form textarea {
    padding: 0.5rem;
    margin-bottom: 1rem;
    border: 1px solid #ccc;
    border-radius: 4px;
}

form button {
    padding: 0.7rem;
    background-color: #333;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

form button:hover {
    background-color: #575757;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem;
    position: fixed;
    bottom: 0;
    width: 100%;
}
document.addEventListener('DOMContentLoaded', () => {
    const form = document.getElementById('contact-form');
    
    form.addEventListener('submit', (e) => {
        e.preventDefault();
        
        const name = document.getElementById('name').value;
        const email = document.getElementById('email').value;
        const message = document.getElementById('message').value;
        
        console.log('Nombre:', name);
        console.log('Correo Electrónico:', email);
        console.log('Mensaje:', message);
        
        // Aquí puedes agregar el código para enviar los datos del formulario a un servidor
        alert('Formulario enviado');
    });
});

