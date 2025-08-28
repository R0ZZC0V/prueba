<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ROZZCORP - Proyecto Ventas</title>
  <!-- Bootstrap CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />
  <!-- Font Awesome para iconos -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <style>
    .company-hero {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 60px 0;
      margin-bottom: 30px;
      border-radius: 10px;
    }
    .mission-vision-card {
      border: none;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }
    .mission-vision-card:hover {
      transform: translateY(-5px);
    }
    .company-logo {
      font-size: 3rem;
      color: #667eea;
      margin-bottom: 20px;
    }
    .feature-icon {
      font-size: 2.5rem;
      color: #667eea;
      margin-bottom: 15px;
    }
  </style>
</head>
<body>
  <div class="container mt-4">
    <h1 class="mb-4 text-center">ROZZCORP - Sistema de Ventas</h1>

    <!-- Nav tabs -->
    <ul class="nav nav-tabs" id="myTab" role="tablist">
      <li class="nav-item" role="presentation">
        <button class="nav-link active" id="access-tab" data-bs-toggle="tab" data-bs-target="#access" type="button" role="tab" aria-controls="access" aria-selected="true">
          <i class="fas fa-user-lock me-2"></i>Acceso
        </button>
      </li>
      <li class="nav-item" role="presentation">
        <button class="nav-link" id="about-tab" data-bs-toggle="tab" data-bs-target="#about" type="button" role="tab" aria-controls="about" aria-selected="false">
          <i class="fas fa-building me-2"></i>Sobre ROZZCORP
        </button>
      </li>
      <li class="nav-item" role="presentation">
        <button class="nav-link" id="products-tab" data-bs-toggle="tab" data-bs-target="#products" type="button" role="tab" aria-controls="products" aria-selected="false">
          <i class="fas fa-shopping-bag me-2"></i>Productos
        </button>
      </li>
      <li class="nav-item" role="presentation">
        <button class="nav-link" id="cart-tab" data-bs-toggle="tab" data-bs-target="#cart" type="button" role="tab" aria-controls="cart" aria-selected="false">
          <i class="fas fa-shopping-cart me-2"></i>Carrito de Compra
        </button>
      </li>
    </ul>

    <!-- Tab panes -->
    <div class="tab-content mt-4" id="myTabContent">
      <!-- Acceso (Login y Registro) -->
      <div class="tab-pane fade show active" id="access" role="tabpanel" aria-labelledby="access-tab">
        <div class="row justify-content-center">
          <div class="col-md-6">
            <ul class="nav nav-pills mb-3" id="accessTab" role="tablist">
              <li class="nav-item" role="presentation">
                <button class="nav-link active" id="login-pill" data-bs-toggle="pill" data-bs-target="#loginPane" type="button" role="tab" aria-controls="loginPane" aria-selected="true">
                  <i class="fas fa-sign-in-alt me-1"></i> Iniciar Sesión
                </button>
              </li>
              <li class="nav-item" role="presentation">
                <button class="nav-link" id="register-pill" data-bs-toggle="pill" data-bs-target="#registerPane" type="button" role="tab" aria-controls="registerPane" aria-selected="false">
                  <i class="fas fa-user-plus me-1"></i> Registrarse
                </button>
              </li>
            </ul>
            <div class="tab-content" id="accessTabContent">
              <!-- Login -->
              <div class="tab-pane fade show active" id="loginPane" role="tabpanel" aria-labelledby="login-pill">
                <div class="card shadow">
                  <div class="card-header bg-primary text-white text-center">
                    <h4 class="mb-0"><i class="fas fa-lock me-2"></i>Iniciar Sesión</h4>
                  </div>
                  <div class="card-body">
                    <form id="loginForm">
                      <div class="mb-3">
                        <label for="loginUsername" class="form-label">Usuario</label>
                        <div class="input-group">
                          <span class="input-group-text"><i class="fas fa-user"></i></span>
                          <input type="text" class="form-control" id="loginUsername" placeholder="Ingresa tu usuario" required />
                        </div>
                      </div>
                      <div class="mb-3">
                        <label for="loginPassword" class="form-label">Contraseña</label>
                        <div class="input-group">
                          <span class="input-group-text"><i class="fas fa-key"></i></span>
                          <input type="password" class="form-control" id="loginPassword" placeholder="Contraseña" required />
                        </div>
                      </div>
                      <button type="submit" class="btn btn-primary w-100">
                        <i class="fas fa-sign-in-alt me-2"></i>Iniciar Sesión
                      </button>
                    </form>
                    <div class="text-center my-3">
                      <p>O inicia sesión con:</p>
                      <a href="#" class="btn btn-danger w-100" id="googleLoginBtn">
                        <i class="fab fa-google me-2"></i> Google
                      </a>
                    </div>
                    <div id="loginMessage" class="mt-3"></div>
                  </div>
                </div>
              </div>
              <!-- Registro -->
              <div class="tab-pane fade" id="registerPane" role="tabpanel" aria-labelledby="register-pill">
                <div class="card shadow">
                  <div class="card-header bg-success text-white text-center">
                    <h4 class="mb-0"><i class="fas fa-user-plus me-2"></i>Registrarse</h4>
                  </div>
                  <div class="card-body">
                    <form id="registerForm">
                      <div class="mb-3">
                        <label for="registerUsername" class="form-label">Usuario</label>
                        <input type="text" class="form-control" id="registerUsername" placeholder="Elige un usuario" required />
                      </div>
                      <div class="mb-3">
                        <label for="registerEmail" class="form-label">Correo electrónico</label>
                        <input type="email" class="form-control" id="registerEmail" placeholder="Tu correo electrónico" />
                      </div>
                      <div class="mb-3">
                        <label for="registerPassword" class="form-label">Contraseña</label>
                        <input type="password" class="form-control" id="registerPassword" placeholder="Crea una contraseña" required />
                      </div>
                      <button type="submit" class="btn btn-success w-100">
                        <i class="fas fa-user-plus me-2"></i>Registrarse
                      </button>
                    </form>
                    <div id="registerMessage" class="mt-3"></div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Sobre ROZZCORP -->
      <div class="tab-pane fade" id="about" role="tabpanel" aria-labelledby="about-tab">
        <!-- Hero Section -->
        <div class="company-hero text-center">
          <div class="container">
            <div class="company-logo">
              <i class="fas fa-cube"></i>
            </div>
            <h2 class="display-4 fw-bold">ROZZCORP</h2>
            <p class="lead">Innovación y calidad en cada producto</p>
          </div>
        </div>

        <!-- Quiénes Somos -->
        <div class="row mb-5">
          <div class="col-lg-8 mx-auto">
            <div class="card mission-vision-card">
              <div class="card-header bg-light">
                <h3 class="card-title mb-0"><i class="fas fa-users me-2"></i>¿Quiénes Somos?</h3>
              </div>
              <div class="card-body">
                <p class="card-text">
                  ROZZCORP es una empresa líder en el sector de ventas tecnológicas, fundada en 2010 con el objetivo 
                  de proporcionar productos de alta calidad a precios accesibles. Nuestro compromiso con la innovación 
                  y la satisfacción del cliente nos ha convertido en referentes del mercado.
                </p>
                <p class="card-text">
                  Contamos con un equipo de profesionales altamente capacitados que trabajan incansablemente para 
                  ofrecer las mejores soluciones y el mejor servicio al cliente en la industria.
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Misión y Visión -->
        <div class="row">
          <div class="col-md-6 mb-4">
            <div class="card mission-vision-card h-100">
              <div class="card-header bg-info text-white">
                <h4 class="card-title mb-0"><i class="fas fa-bullseye me-2"></i>Misión</h4>
              </div>
              <div class="card-body">
                <p class="card-text">
                  Proporcionar productos tecnológicos innovadores y de alta calidad que mejoren la vida de nuestros 
                  clientes, manteniendo siempre los más altos estándares de servicio y satisfacción.
                </p>
              </div>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <div class="card mission-vision-card h-100">
              <div class="card-header bg-warning text-dark">
                <h4 class="card-title mb-0"><i class="fas fa-eye me-2"></i>Visión</h4>
              </div>
              <div class="card-body">
                <p class="card-text">
                  Ser la empresa líder en ventas tecnológicas a nivel global, reconocida por nuestra innovación, 
                  calidad y compromiso con la excelencia en el servicio al cliente.
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Valores -->
        <div class="row mt-4">
          <div class="col-12">
            <div class="card mission-vision-card">
              <div class="card-header bg-success text-white">
                <h4 class="card-title mb-0"><i class="fas fa-star me-2"></i>Nuestros Valores</h4>
              </div>
              <div class="card-body">
                <div class="row text-center">
                  <div class="col-md-3 mb-3">
                    <div class="feature-icon">
                      <i class="fas fa-lightbulb"></i>
                    </div>
                    <h5>Innovación</h5>
                    <p>Buscamos constantemente nuevas soluciones</p>
                  </div>
                  <div class="col-md-3 mb-3">
                    <div class="feature-icon">
                      <i class="fas fa-award"></i>
                    </div>
                    <h5>Calidad</h5>
                    <p>Productos que superan expectativas</p>
                  </div>
                  <div class="col-md-3 mb-3">
                    <div class="feature-icon">
                      <i class="fas fa-handshake"></i>
                    </div>
                    <h5>Confianza</h5>
                    <p>Relaciones duraderas con clientes</p>
                  </div>
                  <div class="col-md-3 mb-3">
                    <div class="feature-icon">
                      <i class="fas fa-heart"></i>
                    </div>
                    <h5>Pasión</h5>
                    <p>Amamos lo que hacemos</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Productos -->
      <div class="tab-pane fade" id="products" role="tabpanel" aria-labelledby="products-tab">
        <div class="d-flex justify-content-between align-items-center mb-4">
          <h3>Nuestros Productos</h3>
          <span class="badge bg-primary" id="productCount">3 productos</span>
        </div>
        <div id="productList" class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4">
          <!-- Productos se cargarán aquí -->
        </div>
      </div>

      <!-- Carrito -->
      <div class="tab-pane fade" id="cart" role="tabpanel" aria-labelledby="cart-tab">
        <div class="card">
          <div class="card-header bg-dark text-white">
            <h4 class="mb-0"><i class="fas fa-shopping-cart me-2"></i>Carrito de Compra</h4>
          </div>
          <div class="card-body">
            <div id="cartItems" class="mb-3">
              <!-- Ítems del carrito se mostrarán aquí -->
            </div>
            <div class="d-flex justify-content-between align-items-center mb-3">
              <h5 class="mb-0">Total: $<span id="cartTotal">0.00</span></h5>
              <span class="badge bg-info" id="cartItemsCount">0 items</span>
            </div>
            <button id="checkoutBtn" class="btn btn-success w-100" disabled>
              <i class="fas fa-check-circle me-2"></i>Finalizar Compra
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- jQuery CDN -->
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <!-- Bootstrap Bundle JS (incluye Popper) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <!-- Nuestro JS -->
  <script>
    $(document).ready(function () {
      // Datos de ejemplo de productos
      const products = [
        { 
          id: 1, 
          name: "Laptop RozzBook Pro", 
          price: 1299.99, 
          description: "Laptop ultradelgada con procesador de última generación, 16GB RAM y SSD 512GB. Perfecta para trabajo y entretenimiento.", 
          category: "Tecnología"
        },
        { 
          id: 2, 
          name: "Smartphone RozzPhone X", 
          price: 699.99, 
          description: "Smartphone con pantalla AMOLED 6.7\", cámara triple 108MP y batería de 5000mAh. Rendimiento excepcional.", 
          category: "Tecnología"
        },
        { 
          id: 3, 
          name: "Auriculares RozzSound Pro", 
          price: 199.99, 
          description: "Auriculares inalámbricos con cancelación de ruido activa, sonido surround y hasta 30 horas de batería.", 
          category: "Audio"
        },
        { 
          id: 4, 
          name: "Smartwatch RozzWatch", 
          price: 349.99, 
          description: "Reloj inteligente con monitor de salud, GPS integrado y resistencia al agua. Conectividad completa.", 
          category: "Wearables"
        },
        { 
          id: 5, 
          name: "Tablet RozzPad Air", 
          price: 499.99, 
          description: "Tablet ligera con pantalla 10.9\", compatible con lápiz digital y teclado. Ideal para creativos.", 
          category: "Tecnología"
        },
        { 
          id: 6, 
          name: "Cámara RozzCam 4K", 
          price: 899.99, 
          description: "Cámara profesional 4K con estabilización óptica y lentes intercambiables. Para creadores de contenido.", 
          category: "Fotografía"
        }
      ];

      let cart = [];

      // Función para mostrar productos
      function renderProducts() {
        $("#productList").empty();
        $("#productCount").text(products.length + " productos");
        
        products.forEach((product) => {
          const productCard = `
            <div class="col">
              <div class="card h-100 shadow-sm">
                <div class="card-header bg-light">
                  <span class="badge bg-secondary">${product.category}</span>
                </div>
                <div class="card-body d-flex flex-column">
                  <h5 class="card-title">${product.name}</h5>
                  <p class="card-text text-muted small">${product.description}</p>
                  <div class="mt-auto">
                    <p class="card-text fw-bold text-primary mb-2">$${product.price.toFixed(2)}</p>
                    <button class="btn btn-primary w-100 add-to-cart" data-id="${product.id}">
                      <i class="fas fa-cart-plus me-2"></i>Agregar al carrito
                    </button>
                  </div>
                </div>
              </div>
            </div>
          `;
          $("#productList").append(productCard);
        });
      }

      // Función para actualizar carrito
      function updateCart() {
        $("#cartItems").empty();
        let total = 0;
        let itemsCount = 0;
        
        if (cart.length === 0) {
          $("#cartItems").html(`
            <div class="text-center text-muted py-4">
              <i class="fas fa-shopping-cart fa-3x mb-3"></i>
              <p>Tu carrito está vacío</p>
            </div>
          `);
        } else {
          cart.forEach((item) => {
            total += item.price * item.quantity;
            itemsCount += item.quantity;
            $("#cartItems").append(`
              <div class="card mb-2">
                <div class="card-body">
                  <div class="d-flex justify-content-between align-items-center">
                    <div>
                      <h6 class="mb-1">${item.name}</h6>
                      <small class="text-muted">$${item.price.toFixed(2)} c/u</small>
                    </div>
                    <div class="d-flex align-items-center">
                      <button class="btn btn-sm btn-outline-secondary decrease-quantity" data-id="${item.id}">
                        <i class="fas fa-minus"></i>
                      </button>
                      <span class="mx-2 fw-bold">${item.quantity}</span>
                      <button class="btn btn-sm btn-outline-secondary increase-quantity" data-id="${item.id}">
                        <i class="fas fa-plus"></i>
                      </button>
                      <button class="btn btn-sm btn-danger ms-2 remove-item" data-id="${item.id}">
                        <i class="fas fa-trash"></i>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            `);
          });
        }
        
        $("#cartTotal").text(total.toFixed(2));
        $("#cartItemsCount").text(itemsCount + " items");
        $("#checkoutBtn").prop("disabled", cart.length === 0);
      }

      // Agregar producto al carrito
      $(document).on("click", ".add-to-cart", function () {
        const id = parseInt($(this).data("id"));
        const product = products.find((p) => p.id === id);
        const cartItem = cart.find((item) => item.id === id);
        
        if (cartItem) {
          cartItem.quantity++;
        } else {
          cart.push({ ...product, quantity: 1 });
        }
        
        updateCart();
        
        // Mostrar notificación
        const toast = `
          <div class="toast align-items-center text-white bg-success border-0 position-fixed top-0 end-0 m-3" role="alert">
            <div class="d-flex">
              <div class="toast-body">
                <i class="fas fa-check-circle me-2"></i>Se agregó ${product.name} al carrito
              </div>
              <button type="button" class="btn-close btn-close-white me-2 m-auto" data-bs-dismiss="toast"></button>
            </div>
          </div>
        `;
        $("body").append(toast);
        $(".toast").toast("show");
        
        // Auto-remover el toast después de 3 segundos
        setTimeout(() => {
          $(".toast").toast("hide");
        }, 3000);
      });

      // Disminuir cantidad
      $(document).on("click", ".decrease-quantity", function () {
        const id = parseInt($(this).data("id"));
        const cartItem = cart.find((item) => item.id === id);
        
        if (cartItem && cartItem.quantity > 1) {
          cartItem.quantity--;
        } else {
          cart = cart.filter(item => item.id !== id);
        }
        
        updateCart();
      });

      // Aumentar cantidad
      $(document).on("click", ".increase-quantity", function () {
        const id = parseInt($(this).data("id"));
        const cartItem = cart.find((item) => item.id === id);
        
        if (cartItem) {
          cartItem.quantity++;
        }
        
        updateCart();
      });

      // Remover item
      $(document).on("click", ".remove-item", function () {
        const id = parseInt($(this).data("id"));
        cart = cart.filter(item => item.id !== id);
        updateCart();
      });

      // Manejar inicio de sesión (simulado)
      $("#loginForm").submit(function (e) {
        e.preventDefault();
        const username = $("#username").val().trim();
        const password = $("#password").val().trim();

        // Simulación simple: usuario = admin, contraseña = 1234
        if (username === "admin" && password === "1234") {
          $("#loginMessage").html(`
            <div class="alert alert-success d-flex align-items-center">
              <i class="fas fa-check-circle me-2"></i>
              <div>¡Inicio de sesión exitoso! Redirigiendo...</div>
            </div>
          `);
          
          // Cambiar a pestaña productos después de 1 segundo
          setTimeout(() => {
            const tabTrigger = new bootstrap.Tab($("#products-tab"));
            tabTrigger.show();
          }, 1000);
        } else {
          $("#loginMessage").html(`
            <div class="alert alert-danger d-flex align-items-center">
              <i class="fas fa-exclamation-circle me-2"></i>
              <div>Usuario o contraseña incorrectos. Prueba con admin/1234</div>
            </div>
          `);
        }
      });

      // Finalizar compra
      $("#checkoutBtn").click(function () {
        const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
        
        Swal.fire({
          title: '¡Compra Exitosa!',
          html: `
            <div class="text-center">
              <i class="fas fa-check-circle text-success fa-4x mb-3"></i>
              <p>Tu compra por <strong>$${total.toFixed(2)}</strong> ha sido procesada exitosamente.</p>
              <p class="text-muted">¡Gracias por confiar en ROZZCORP!</p>
            </div>
          `,
          icon: 'success',
          confirmButtonText: 'Continuar comprando'
        });
        
        cart = [];
        updateCart();
        
        // Volver a pestaña productos
        const tabTrigger = new bootstrap.Tab($("#products-tab"));
        tabTrigger.show();
      });

      // Inicializar productos y carrito
      renderProducts();
      updateCart();

      // Auto-remover toasts al ocultarse
      $(document).on('hidden.bs.toast', '.toast', function() {
        $(this).remove();
      });
    });
  </script>

  <!-- SweetAlert2 para mejores alertas -->
  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
</body>
</html>

