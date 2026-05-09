<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yanet Mendocina - Sistema de Distribución v3.0</title>
    
    <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>

    <style>
        :root {
            --primary: #1a3c5e;
            --secondary: #2e6fa8;
            --success: #27ae60;
            --warning: #f39c12;
            --danger: #e74c3c;
            --light: #f8f9fa;
            --dark: #2c3e50;
            --white: #ffffff;
            --border: #ddd;
            --shadow: 0 2px 15px rgba(0,0,0,0.1);
            --radius: 12px;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            background: linear-gradient(135deg, #e8f0fe 0%, #f5f7fa 50%, #e8f0fe 100%);
            color: var(--dark);
            min-height: 100vh;
            line-height: 1.6;
        }

        .header {
            background: linear-gradient(135deg, #0d2137, #1a3c5e, #2e6fa8);
            color: white;
            padding: 1rem;
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .header h1 { font-size: clamp(1.2rem, 3vw, 1.8rem); }
        .header .user-info { font-size: 0.85rem; opacity: 0.9; margin-top: 0.3rem; }

        .btn-logout {
            background: rgba(255,255,255,0.15);
            border: 1px solid rgba(255,255,255,0.3);
            color: white;
            padding: 0.4rem 1rem;
            border-radius: 20px;
            cursor: pointer;
            font-size: 0.8rem;
            margin-top: 0.5rem;
            transition: all 0.3s;
        }
        .btn-logout:hover { background: rgba(255,255,255,0.25); }

        .container { max-width: 1300px; margin: 0 auto; padding: 1rem; }

        /* LOGIN */
        .login-container {
            max-width: 420px;
            margin: 60px auto;
            background: white;
            padding: 2.5rem 2rem;
            border-radius: var(--radius);
            box-shadow: 0 10px 40px rgba(0,0,0,0.15);
            text-align: center;
        }
        .login-container .logo { font-size: 4rem; margin-bottom: 0.5rem; }
        .login-container h2 { color: var(--primary); font-size: 1.6rem; }
        .login-container input {
            width: 100%;
            padding: 0.9rem;
            margin: 0.5rem 0;
            border: 2px solid var(--border);
            border-radius: 8px;
            font-size: 1rem;
        }
        .login-container input:focus { outline: none; border-color: var(--secondary); }
        .btn-login {
            width: 100%;
            padding: 0.9rem;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            margin-top: 0.8rem;
        }
        .btn-login:hover { background: #0d2137; }
        .login-error { color: var(--danger); margin-top: 0.8rem; font-size: 0.9rem; display: none; }

        /* TABS */
        .tabs {
            display: flex;
            flex-wrap: wrap;
            gap: 0.3rem;
            margin-bottom: 1.2rem;
            background: white;
            border-radius: var(--radius);
            padding: 0.4rem;
            box-shadow: var(--shadow);
        }
        .tab-btn {
            flex: 1;
            min-width: 85px;
            padding: 0.7rem 0.4rem;
            border: none;
            background: transparent;
            cursor: pointer;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.78rem;
            transition: all 0.3s;
            color: #666;
        }
        .tab-btn.active { background: var(--primary); color: white; }
        .tab-btn:hover:not(.active) { background: #e8f0fe; }

        .tab-content {
            display: none;
            background: white;
            border-radius: var(--radius);
            padding: 1.5rem;
            box-shadow: var(--shadow);
            animation: fadeIn 0.4s ease;
        }
        .tab-content.active { display: block; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-title {
            color: var(--primary);
            border-bottom: 3px solid var(--secondary);
            padding-bottom: 0.5rem;
            margin-bottom: 1.2rem;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        fieldset {
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            padding: 1.2rem;
            margin-bottom: 1.2rem;
            background: #fafbfc;
        }
        legend {
            font-weight: 700;
            color: var(--primary);
            padding: 0 0.6rem;
            font-size: 1rem;
            background: white;
            border-radius: 5px;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
            gap: 1rem;
        }
        .form-group { display: flex; flex-direction: column; gap: 0.3rem; }
        .form-group label { font-weight: 600; font-size: 0.85rem; color: #555; }
        .form-group input, .form-group select, .form-group textarea {
            padding: 0.7rem 0.8rem;
            border: 2px solid var(--border);
            border-radius: 8px;
            font-size: 0.95rem;
            font-family: inherit;
        }
        .form-group textarea { resize: vertical; min-height: 50px; }
        .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(46,111,168,0.1);
        }

        .btn {
            padding: 0.7rem 1.4rem;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            font-size: 0.9rem;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
        }
        .btn-primary { background: var(--primary); color: white; }
        .btn-primary:hover { background: #0d2137; transform: translateY(-2px); }
        .btn-success { background: var(--success); color: white; }
        .btn-success:hover { background: #219a52; transform: translateY(-2px); }
        .btn-warning { background: var(--warning); color: white; }
        .btn-danger { background: var(--danger); color: white; }
        .btn-info { background: #17a2b8; color: white; }
        .btn-sm { padding: 0.4rem 0.8rem; font-size: 0.8rem; }
        .btn-xs { padding: 0.25rem 0.5rem; font-size: 0.7rem; }

        .table-container {
            overflow-x: auto;
            margin-top: 1rem;
            border-radius: 8px;
            border: 1px solid #e0e0e0;
            max-height: 500px;
            overflow-y: auto;
        }
        table { width: 100%; border-collapse: collapse; font-size: 0.83rem; min-width: 800px; }
        th, td { padding: 0.55rem; text-align: left; border-bottom: 1px solid #e0e0e0; }
        th { background: var(--primary); color: white; font-weight: 600; position: sticky; top: 0; z-index: 10; }
        tr:hover { background: #f5f9ff; }

        .vencido { background: #ffe0e0 !important; color: #c0392b; font-weight: 700; }
        .proximo-vencer { background: #fff9e0 !important; color: #d68910; font-weight: 600; }
        .vigente { background: #e8f8e8 !important; }
        .seleccionado-automatico { background: #e0f0ff !important; border-left: 3px solid #2e6fa8; }

        .badge {
            display: inline-block;
            padding: 0.2rem 0.5rem;
            border-radius: 10px;
            font-size: 0.7rem;
            font-weight: 700;
        }
        .badge-danger { background: #e74c3c; color: white; }
        .badge-warning { background: #f39c12; color: white; }
        .badge-success { background: #27ae60; color: white; }
        .badge-info { background: #17a2b8; color: white; }

        .stock-info-card {
            background: #f0f7ff;
            border: 1px solid #cce5ff;
            border-radius: 8px;
            padding: 0.8rem;
            margin: 0.5rem 0;
            font-size: 0.85rem;
        }
        .stock-info-card strong { color: var(--primary); }

        .totals-box {
            background: linear-gradient(135deg, #e8f0fe, #d4e6f1);
            border-radius: 10px;
            padding: 1.2rem;
            margin-top: 1.2rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1rem;
            text-align: center;
        }
        .total-item {
            background: white;
            border-radius: 8px;
            padding: 0.7rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .total-item .label { font-size: 0.75rem; color: #777; font-weight: 600; }
        .total-item .value { font-size: 1.2rem; font-weight: 700; color: var(--primary); }

        .search-box {
            display: flex;
            gap: 0.6rem;
            flex-wrap: wrap;
            margin-bottom: 1rem;
            align-items: flex-end;
        }
        .search-box input, .search-box select {
            padding: 0.6rem;
            border: 2px solid #ddd;
            border-radius: 8px;
        }
        .search-box input { flex: 1; min-width: 150px; }

        .price-panel {
            background: #fffef5;
            border: 2px solid #f0e68c;
            border-radius: var(--radius);
            padding: 1rem;
            margin-bottom: 1rem;
        }

        .editing-row { background: #fffde7 !important; }
        .loading { text-align: center; padding: 2rem; color: #888; }

        /* Categorías en stock */
        .categoria-header {
            background: #1a3c5e !important;
            color: white !important;
            font-size: 1rem;
            font-weight: 700;
            padding: 0.7rem !important;
        }
        .categoria-header td { background: #1a3c5e !important; color: white !important; }

        @media (max-width: 768px) {
            .form-grid { grid-template-columns: 1fr 1fr; }
            .tab-btn { font-size: 0.68rem; padding: 0.5rem 0.3rem; min-width: 60px; }
            .totals-box { grid-template-columns: 1fr 1fr; }
            th, td { padding: 0.4rem; font-size: 0.73rem; }
        }
        @media (max-width: 480px) {
            .form-grid { grid-template-columns: 1fr; }
            .header h1 { font-size: 1rem; }
            .container { padding: 0.5rem; }
            .tab-content { padding: 1rem 0.7rem; }
        }
    </style>
</head>
<body>

    <!-- LOGIN -->
    <div id="loginScreen" class="login-container">
        <div class="logo">🥤</div>
        <h2>Yanet Mendocina</h2>
        <p style="color:#777;margin-bottom:1rem;">Sistema de Distribución v3.0</p>
        <input type="email" id="loginEmail" placeholder="Correo electrónico" value="yanet@mendocina.bo">
        <input type="password" id="loginPassword" placeholder="Contraseña">
        <button class="btn-login" onclick="login()">🔐 Ingresar al Sistema</button>
        <p id="loginError" class="login-error"></p>
    </div>

    <!-- SISTEMA PRINCIPAL -->
    <div id="appScreen" style="display:none;">
        <div class="header">
            <h1>🥤 Yanet Mendocina - Control de Distribución v3.0</h1>
            <div class="user-info" id="userDisplay"></div>
            <button class="btn-logout" onclick="logout()">🚪 Cerrar Sesión</button>
        </div>

        <div class="container">
            <div class="tabs">
                <button class="tab-btn active" onclick="switchTab('ingreso')">📥 Ingreso</button>
                <button class="tab-btn" onclick="switchTab('stock')">📦 Stock</button>
                <button class="tab-btn" onclick="switchTab('precios')">💰 Precios</button>
                <button class="tab-btn" onclick="switchTab('salida')">🚚 Salida</button>
                <button class="tab-btn" onclick="switchTab('rendicion')">🔄 Rendición</button>
                <button class="tab-btn" onclick="switchTab('historial')">📋 Historial</button>
            </div>

            <!-- ==================== PANEL INGRESO ==================== -->
            <div id="panelIngreso" class="tab-content active">
                <div class="section-title">📥 Registro de Ingreso de Mercadería</div>
                
                <fieldset>
                    <legend>📋 Datos del Lote</legend>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>Ciudad de Origen</label>
                            <select id="ingCiudad">
                                <option value="Santa Cruz" selected>Santa Cruz</option>
                                <option value="Cochabamba">Cochabamba</option>
                                <option value="La Paz">La Paz</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Categoría</label>
                            <select id="ingCategoria" onchange="actualizarProductosIngreso()">
                                <option value="">Seleccionar...</option>
                                <option value="sodas">🥤 Sodas Mendocina</option>
                                <option value="cervezas_lata">🍺 Cervezas en Lata</option>
                                <option value="cervezas_botella">🍾 Cervezas en Botella</option>
                                <option value="energizantes">⚡ Energizantes y Maltas</option>
                                <option value="agua">💧 Agua</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Producto</label>
                            <select id="ingProducto" onchange="actualizarPresentacionesIngreso()">
                                <option value="">Seleccionar categoría primero</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Presentación</label>
                            <select id="ingPresentacion">
                                <option value="">Seleccionar presentación...</option>
                            </select>
                        </div>
                        <div class="form-group" id="saborContainerIng" style="display:none;">
                            <label>Sabor</label>
                            <select id="ingSabor">
                                <option value="">Seleccionar sabor...</option>
                                <option value="Naranja">🍊 Naranja</option><option value="Cola">🥤 Cola</option>
                                <option value="Frutilla">🍓 Frutilla</option><option value="Pomelo">🍊 Pomelo</option>
                                <option value="Guaraná">🌿 Guaraná</option><option value="Limón">🍋 Limón</option>
                                <option value="Uva">🍇 Uva</option><option value="Piña">🍍 Piña</option>
                                <option value="Papaya">🍈 Papaya</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Paquetes Totales</label>
                            <input type="number" id="ingPaquetes" min="1" value="1" onchange="calcularUnidadesIngreso()">
                        </div>
                        <div class="form-group">
                            <label>Unidades por Paquete</label>
                            <input type="number" id="ingUniPorPaquete" min="1" value="6" onchange="calcularUnidadesIngreso()">
                        </div>
                        <div class="form-group">
                            <label>Total Unidades</label>
                            <input type="number" id="ingTotalUnidades" readonly style="background:#f0f0f0;font-weight:700;">
                        </div>
                        <div class="form-group">
                            <label>Fecha de Vencimiento ⚠️</label>
                            <input type="date" id="ingVencimiento" required>
                        </div>
                    </div>
                </fieldset>

                <fieldset>
                    <legend>⚠️ Control de Daños</legend>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>Paquetes Dañados</label>
                            <input type="number" id="ingPaquetesDanados" min="0" value="0" onchange="calcularDanos()">
                        </div>
                        <div class="form-group">
                            <label>Unidades Dañadas</label>
                            <input type="number" id="ingUnidadesDanadas" min="0" value="0" onchange="calcularDanos()">
                        </div>
                        <div class="form-group">
                            <label>Stock Disponible (Paq)</label>
                            <input type="number" id="ingStockPaquetes" readonly style="background:#e8f8e8;font-weight:700;">
                        </div>
                        <div class="form-group">
                            <label>Stock Disponible (Uni)</label>
                            <input type="number" id="ingStockUnidades" readonly style="background:#e8f8e8;font-weight:700;">
                        </div>
                        <div class="form-group">
                            <label>Tipo de Daño</label>
                            <select id="ingObservacion">
                                <option value="">Sin daños</option>
                                <option value="Botellas reventadas">Botellas reventadas</option>
                                <option value="Latas perforadas">Latas perforadas</option>
                                <option value="Paquete mojado">Paquete mojado</option>
                                <option value="Producto vencido">Producto vencido</option>
                                <option value="Producto aplastado">Producto aplastado</option>
                                <option value="Fugas o pérdidas">Fugas o pérdidas</option>
                            </select>
                        </div>
                    </div>
                </fieldset>

                <button class="btn btn-primary" onclick="registrarIngreso()">✅ Registrar Ingreso</button>
                <p id="ingresoMsg" style="margin-top:0.8rem;font-weight:600;"></p>
            </div>

            <!-- ==================== PANEL STOCK (ORDENADO POR VENCIMIENTO Y CATEGORÍA) ==================== -->
            <div id="panelStock" class="tab-content">
                <div class="section-title">📦 Inventario - Ordenado por Vencimiento</div>
                <div class="search-box">
                    <input type="text" id="stockSearch" placeholder="🔍 Buscar..." oninput="cargarStock()">
                    <select id="stockFilterVencimiento" onchange="cargarStock()">
                        <option value="todos">Todos estados</option>
                        <option value="vencido">🔴 Vencidos</option>
                        <option value="proximo">🟡 Próximos (30 días)</option>
                        <option value="vigente">🟢 Vigentes</option>
                    </select>
                    <select id="stockFilterCategoria" onchange="cargarStock()">
                        <option value="todos">Todas categorías</option>
                        <option value="sodas">🥤 Sodas Mendocina</option>
                        <option value="cervezas">🍺 Todas Cervezas</option>
                        <option value="cervezas_lata">🍺 Cervezas Lata</option>
                        <option value="cervezas_botella">🍾 Cervezas Botella</option>
                        <option value="energizantes">⚡ Energizantes/Maltas</option>
                        <option value="agua">💧 Agua</option>
                    </select>
                </div>
                <div class="table-container">
                    <table id="stockTable">
                        <thead>
                            <tr>
                                <th>Vencimiento</th>
                                <th>Producto</th>
                                <th>Sabor</th>
                                <th>Presentación</th>
                                <th>Paquetes</th>
                                <th>Unidades</th>
                                <th>Estado</th>
                                <th>Acción</th>
                            </tr>
                        </thead>
                        <tbody id="stockTableBody">
                            <tr><td colspan="8" class="loading">Cargando inventario...</td></tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- ==================== PANEL DE PRECIOS ==================== -->
            <div id="panelPrecios" class="tab-content">
                <div class="section-title">💰 Configuración de Precios Generales</div>
                <div class="price-panel">
                    <h3>📌 Precios por Producto/Presentación</h3>
                    <p style="font-size:0.85rem;color:#888;">Configure el precio por paquete. Se usará automáticamente en salidas.</p>
                </div>
                <div class="table-container">
                    <table>
                        <thead>
                            <tr><th>Categoría</th><th>Producto</th><th>Presentación</th><th>Precio/Paq (Bs)</th><th>Acción</th></tr>
                        </thead>
                        <tbody id="preciosTableBody">
                            <tr><td colspan="5" class="loading">Cargando precios...</td></tr>
                        </tbody>
                    </table>
                </div>
                <p id="preciosMsg" style="margin-top:0.8rem;font-weight:600;"></p>
            </div>

            <!-- ==================== PANEL SALIDA (CON AUTO-SELECCIÓN POR VENCIMIENTO) ==================== -->
            <div id="panelSalida" class="tab-content">
                <div class="section-title">🚚 Registro de Salida de Camión</div>
                
                <fieldset>
                    <legend>👤 Datos del Chofer</legend>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>Nombre del Chofer</label>
                            <input type="text" id="salidaChofer" placeholder="Nombre completo">
                        </div>
                        <div class="form-group">
                            <label>Destino</label>
                            <input type="text" id="salidaDestino" placeholder="Ciudad o zona">
                        </div>
                        <div class="form-group">
                            <label>Observaciones del Camión</label>
                            <textarea id="salidaObservacion" placeholder="Cualquier observación relevante..." rows="2"></textarea>
                        </div>
                    </div>
                </fieldset>

                <fieldset>
                    <legend>📦 Seleccionar y Agregar Productos</legend>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>Categoría</label>
                            <select id="salCategoria" onchange="actualizarProductosSalida()">
                                <option value="">Seleccionar...</option>
                                <option value="sodas">🥤 Sodas Mendocina</option>
                                <option value="cervezas_lata">🍺 Cervezas Lata</option>
                                <option value="cervezas_botella">🍾 Cervezas Botella</option>
                                <option value="energizantes">⚡ Energizantes/Maltas</option>
                                <option value="agua">💧 Agua</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Producto</label>
                            <select id="salProducto" onchange="actualizarPresentacionesSalida()">
                                <option value="">Seleccionar categoría</option>
                            </select>
                        </div>
                        <div class="form-group" id="saborContainerSal" style="display:none;">
                            <label>Sabor</label>
                            <select id="salSabor">
                                <option value="">Seleccionar sabor...</option>
                                <option value="Naranja">🍊 Naranja</option><option value="Cola">🥤 Cola</option>
                                <option value="Frutilla">🍓 Frutilla</option><option value="Pomelo">🍊 Pomelo</option>
                                <option value="Guaraná">🌿 Guaraná</option><option value="Limón">🍋 Limón</option>
                                <option value="Uva">🍇 Uva</option><option value="Piña">🍍 Piña</option>
                                <option value="Papaya">🍈 Papaya</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Presentación</label>
                            <select id="salPresentacion" onchange="mostrarStockDisponible()">
                                <option value="">Seleccionar...</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Paquetes a Cargar</label>
                            <input type="number" id="salCantidad" min="1" value="1">
                        </div>
                    </div>
                    
                    <div id="stockDisponibleInfo" style="display:none; margin-top:1rem;">
                        <div class="stock-info-card">
                            <strong>📊 Stock Disponible (ordenado por vencimiento):</strong>
                            <div id="stockDisponibleDetalle"></div>
                        </div>
                    </div>

                    <button class="btn btn-sm btn-info" onclick="agregarProductoSalida()" style="margin-top:0.8rem;">➕ Agregar al Camión</button>
                    <small style="color:#888;margin-left:1rem;">⚠️ Se auto-seleccionan los lotes más próximos a vencer</small>
                </fieldset>

                <fieldset>
                    <legend>📋 Productos en el Camión</legend>
                    <div class="table-container">
                        <table>
                            <thead>
                                <tr><th>Producto</th><th>Sabor</th><th>Presentación</th><th>Paquetes</th><th>Precio/Paq</th><th>Subtotal</th><th>Vencimiento</th><th>Acción</th></tr>
                            </thead>
                            <tbody id="salidaTableBody">
                                <tr><td colspan="8" style="text-align:center;color:#999;">No hay productos</td></tr>
                            </tbody>
                        </table>
                    </div>
                </fieldset>

                <div class="totals-box">
                    <div class="total-item"><span class="label">Total Paquetes</span><span class="value" id="salidaTotalPaquetes">0</span></div>
                    <div class="total-item"><span class="label">Total Bs</span><span class="value" id="salidaTotalBs">0.00</span></div>
                </div>
                <button class="btn btn-success" onclick="registrarSalida()">🚛 Registrar Salida</button>
                <p id="salidaMsg" style="margin-top:0.8rem;font-weight:600;"></p>
            </div>

            <!-- ==================== PANEL RENDICIÓN ==================== -->
            <div id="panelRendicion" class="tab-content">
                <div class="section-title">🔄 Rendición y Retorno de Camión</div>
                <div class="search-box">
                    <select id="rendicionSalidaId" onchange="cargarDatosRendicion()" style="flex:1;">
                        <option value="">Seleccionar salida pendiente...</option>
                    </select>
                    <button class="btn btn-sm btn-warning" onclick="cargarSalidasPendientes()">🔄 Actualizar</button>
                </div>
                <div id="rendicionDetalle"></div>
                <p id="rendicionMsg" style="margin-top:0.8rem;font-weight:600;"></p>
            </div>

            <!-- ==================== PANEL HISTORIAL ==================== -->
            <div id="panelHistorial" class="tab-content">
                <div class="section-title">📋 Historial de Movimientos</div>
                <div class="search-box">
                    <input type="text" id="histSearch" placeholder="🔍 Buscar..." oninput="cargarHistorial()">
                    <input type="date" id="histFechaDesde" onchange="cargarHistorial()" title="Desde">
                    <input type="date" id="histFechaHasta" onchange="cargarHistorial()" title="Hasta">
                    <select id="histTipo" onchange="cargarHistorial()">
                        <option value="todos">Todos</option>
                        <option value="ingreso">Ingresos</option>
                        <option value="salida">Salidas</option>
                        <option value="rendicion">Rendiciones</option>
                    </select>
                </div>
                <div class="table-container">
                    <table>
                        <thead><tr><th>Fecha/Hora</th><th>Tipo</th><th>Detalle</th><th>Monto (Bs)</th></tr></thead>
                        <tbody id="historialTableBody">
                            <tr><td colspan="4" class="loading">Cargando...</td></tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>

        <!-- MODAL PARA EDITAR INGRESO -->
        <div id="modalEditarIngreso" style="display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.6);z-index:2000;justify-content:center;align-items:center;">
            <div style="background:white;border-radius:12px;padding:2rem;max-width:600px;width:90%;max-height:80vh;overflow-y:auto;">
                <h3 style="color:var(--primary);margin-bottom:1rem;">✏️ Editar Ingreso</h3>
                <div id="modalEditarContenido"></div>
                <div style="display:flex;gap:1rem;justify-content:flex-end;margin-top:1rem;">
                    <button class="btn btn-sm btn-danger" onclick="document.getElementById('modalEditarIngreso').style.display='none'">Cancelar</button>
                    <button class="btn btn-sm btn-primary" id="btnGuardarEdicion">💾 Guardar Cambios</button>
                </div>
            </div>
        </div>
    </div>

    <script>
        // ==================== CONFIGURACIÓN FIREBASE ====================
        const firebaseConfig = {
            apiKey: "AIzaSyBsi1frR41LGu28hvFk9nKFAojVk2vbkgs",
            authDomain: "yanet-mendocina.firebaseapp.com",
            projectId: "yanet-mendocina",
            storageBucket: "yanet-mendocina.firebasestorage.app",
            messagingSenderId: "720893524811",
            appId: "1:720893524811:web:a6aef95618bae6760986ce"
        };

        firebase.initializeApp(firebaseConfig);
        const auth = firebase.auth();
        const db = firebase.firestore();

        function logDebug(msg) { console.log('🔍', new Date().toLocaleTimeString(), msg); }

        // ==================== CATÁLOGO ====================
        const catalogoCompleto = {
            sodas: {
                categoria: "Sodas Mendocina", catGrupo: "sodas",
                producto: "Mendocina",
                sabores: ["Naranja","Cola","Frutilla","Pomelo","Guaraná","Limón","Uva","Piña","Papaya"],
                presentaciones: ["3 Litros","2 Litros","1 Litro","330 ml"]
            },
            cervezas_lata: {
                categoria: "Cervezas en Lata", catGrupo: "cervezas",
                productos: [
                    {nombre:"Sniders",presentaciones:["473 ml"]},
                    {nombre:"Capital",presentaciones:["350 ml","473 ml"]},
                    {nombre:"Amster",presentaciones:["269 ml","473 ml"]}
                ]
            },
            cervezas_botella: {
                categoria: "Cervezas en Botella", catGrupo: "cervezas",
                productos: [
                    {nombre:"Amster",presentaciones:["620 ml"]},
                    {nombre:"Real",presentaciones:["620 ml"]},
                    {nombre:"Heineken",presentaciones:["220 ml"]}
                ]
            },
            energizantes: {
                categoria: "Energizantes y Maltas", catGrupo: "energizantes",
                productos: [
                    {nombre:"Malta",presentaciones:["Lata 350 ml"]},
                    {nombre:"Bolt",presentaciones:["Lata 473 ml","Lata 275 ml","Botella 330 ml"]}
                ]
            },
            agua: {
                categoria: "Agua", catGrupo: "agua",
                producto: "Agua",
                presentaciones: ["3 Litros","2 Litros","1 Litro","620 ml"]
            }
        };

        let productosEnSalida = [];

        // ==================== AUTENTICACIÓN ====================
        function login() {
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            const errorEl = document.getElementById('loginError');
            if(!email||!password){errorEl.textContent='⚠️ Complete todos los campos';errorEl.style.display='block';return;}
            errorEl.style.display='none';
            auth.signInWithEmailAndPassword(email,password)
                .then(u=>{
                    document.getElementById('loginScreen').style.display='none';
                    document.getElementById('appScreen').style.display='block';
                    document.getElementById('userDisplay').textContent='👤 '+u.user.email;
                    inicializarApp();
                })
                .catch(e=>{errorEl.textContent='❌ '+e.message;errorEl.style.display='block';});
        }
        function logout(){auth.signOut().then(()=>{document.getElementById('appScreen').style.display='none';document.getElementById('loginScreen').style.display='block';document.getElementById('loginPassword').value='';});}
        auth.onAuthStateChanged(u=>{
            if(u){document.getElementById('loginScreen').style.display='none';document.getElementById('appScreen').style.display='block';document.getElementById('userDisplay').textContent='👤 '+u.email;inicializarApp();}
            else{document.getElementById('appScreen').style.display='none';document.getElementById('loginScreen').style.display='block';}
        });

        // ==================== NAVEGACIÓN ====================
        function switchTab(tabName){
            document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(p=>p.classList.remove('active'));
            const map={ingreso:0,stock:1,precios:2,salida:3,rendicion:4,historial:5};
            document.querySelectorAll('.tab-btn')[map[tabName]].classList.add('active');
            document.getElementById('panel'+tabName.charAt(0).toUpperCase()+tabName.slice(1)).classList.add('active');
            if(tabName==='stock')cargarStock();
            if(tabName==='precios')cargarPrecios();
            if(tabName==='rendicion')cargarSalidasPendientes();
            if(tabName==='historial')cargarHistorial();
        }
        function inicializarApp(){cargarStock();cargarSalidasPendientes();}

        // ==================== FUNCIONES CATÁLOGO ====================
        function actualizarProductosIngreso(){
            const cat=document.getElementById('ingCategoria').value;
            const ps=document.getElementById('ingProducto');
            const prs=document.getElementById('ingPresentacion');
            const sc=document.getElementById('saborContainerIng');
            ps.innerHTML='<option value="">Seleccionar...</option>';
            prs.innerHTML='<option value="">Seleccionar presentación...</option>';
            sc.style.display='none';
            if(!cat)return;
            const c=catalogoCompleto[cat];
            if(cat==='sodas'){sc.style.display='flex';ps.innerHTML='<option value="Mendocina">Mendocina</option>';ps.value='Mendocina';c.presentaciones.forEach(p=>prs.innerHTML+=`<option value="${p}">${p}</option>`);}
            else if(cat==='agua'){ps.innerHTML='<option value="Agua">Agua</option>';ps.value='Agua';c.presentaciones.forEach(p=>prs.innerHTML+=`<option value="${p}">${p}</option>`);}
            else if(c.productos){c.productos.forEach(p=>ps.innerHTML+=`<option value="${p.nombre}">${p.nombre}</option>`);ps.onchange=function(){actPresPorProd(cat,this.value,prs);};}
        }
        function actPresPorProd(cat,prod,prs){
            prs.innerHTML='<option value="">Seleccionar...</option>';
            if(!prod||!cat)return;
            const c=catalogoCompleto[cat];
            if(c.productos){const p=c.productos.find(x=>x.nombre===prod);if(p)p.presentaciones.forEach(x=>prs.innerHTML+=`<option value="${x}">${x}</option>`);}
        }
        function actualizarPresentacionesIngreso(){actPresPorProd(document.getElementById('ingCategoria').value,document.getElementById('ingProducto').value,document.getElementById('ingPresentacion'));}
        function calcularUnidadesIngreso(){const p=parseInt(document.getElementById('ingPaquetes').value)||0;const u=parseInt(document.getElementById('ingUniPorPaquete').value)||0;document.getElementById('ingTotalUnidades').value=p*u;calcularDanos();}
        function calcularDanos(){
            const p=parseInt(document.getElementById('ingPaquetes').value)||0;
            const u=parseInt(document.getElementById('ingUniPorPaquete').value)||0;
            const pd=parseInt(document.getElementById('ingPaquetesDanados').value)||0;
            const ud=parseInt(document.getElementById('ingUnidadesDanadas').value)||0;
            const tu=p*u;const td=(pd*u)+ud;
            const su=Math.max(0,tu-td);const sp=Math.floor(su/u);
            document.getElementById('ingTotalUnidades').value=tu;
            document.getElementById('ingStockPaquetes').value=sp;
            document.getElementById('ingStockUnidades').value=su;
        }

        // ==================== REGISTRAR INGRESO ====================
        function registrarIngreso(){
            const data=obtenerDatosIngreso();
            if(!data){document.getElementById('ingresoMsg').innerHTML='❌ Complete campos obligatorios';document.getElementById('ingresoMsg').style.color='red';return;}
            logDebug('Guardando ingreso');
            db.collection('inventario').add({...data,fecha:firebase.firestore.FieldValue.serverTimestamp()})
                .then(doc=>{
                    document.getElementById('ingresoMsg').innerHTML=`✅ Ingreso #${doc.id.substring(0,6)} - Stock: ${data.stockPaquetes} paq / ${data.stockUnidades} uni`;
                    document.getElementById('ingresoMsg').style.color='green';
                    limpiarFormIngreso();cargarStock();
                })
                .catch(e=>{document.getElementById('ingresoMsg').innerHTML='❌ '+e.message;document.getElementById('ingresoMsg').style.color='red';});
        }
        function obtenerDatosIngreso(){
            const c=document.getElementById('ingCategoria').value,p=document.getElementById('ingProducto').value;
            const pr=document.getElementById('ingPresentacion').value,v=document.getElementById('ingVencimiento').value;
            if(!c||!p||!pr||!v)return null;
            return{
                tipo:'ingreso',categoria:c,ciudad:document.getElementById('ingCiudad').value,
                producto:p,sabor:(document.getElementById('saborContainerIng').style.display!=='none'?document.getElementById('ingSabor').value:''),
                presentacion:pr,paquetes:parseInt(document.getElementById('ingPaquetes').value)||0,
                uniPorPaquete:parseInt(document.getElementById('ingUniPorPaquete').value)||0,
                totalUnidades:parseInt(document.getElementById('ingTotalUnidades').value)||0,
                paquetesDanados:parseInt(document.getElementById('ingPaquetesDanados').value)||0,
                unidadesDanadas:parseInt(document.getElementById('ingUnidadesDanadas').value)||0,
                stockPaquetes:parseInt(document.getElementById('ingStockPaquetes').value)||0,
                stockUnidades:parseInt(document.getElementById('ingStockUnidades').value)||0,
                vencimiento:v,danado:(parseInt(document.getElementById('ingPaquetesDanados').value)||0)>0||(parseInt(document.getElementById('ingUnidadesDanadas').value)||0)>0,
                observacion:document.getElementById('ingObservacion').value,
                fechaStr:new Date().toISOString().split('T')[0],hora:new Date().toLocaleTimeString('es-BO',{hour:'2-digit',minute:'2-digit'})
            };
        }
        function limpiarFormIngreso(){
            ['ingCategoria','ingProducto','ingPresentacion','ingSabor'].forEach(id=>{
                const el=document.getElementById(id);if(el)el.value='';
            });
            document.getElementById('ingProducto').innerHTML='<option value="">Seleccionar categoría primero</option>';
            document.getElementById('ingPresentacion').innerHTML='<option value="">Seleccionar presentación...</option>';
            document.getElementById('saborContainerIng').style.display='none';
            document.getElementById('ingPaquetes').value='1';document.getElementById('ingUniPorPaquete').value='6';
            document.getElementById('ingTotalUnidades').value='6';document.getElementById('ingVencimiento').value='';
            document.getElementById('ingPaquetesDanados').value='0';document.getElementById('ingUnidadesDanadas').value='0';
            document.getElementById('ingStockPaquetes').value='1';document.getElementById('ingStockUnidades').value='6';
            document.getElementById('ingObservacion').value='';
        }

        // ==================== EDITAR INGRESO ====================
        function editarIngreso(docId){
            db.collection('inventario').doc(docId).get().then(doc=>{
                if(!doc.exists){alert('No encontrado');return;}
                const d=doc.data();
                const modal=document.getElementById('modalEditarIngreso');
                const cont=document.getElementById('modalEditarContenido');
                cont.innerHTML=`
                    <div class="form-grid">
                        <div class="form-group"><label>Producto</label><input id="editProd" value="${d.producto}" readonly></div>
                        <div class="form-group"><label>Sabor</label><input id="editSabor" value="${d.sabor||''}"></div>
                        <div class="form-group"><label>Presentación</label><input id="editPres" value="${d.presentacion}" readonly></div>
                        <div class="form-group"><label>Paquetes</label><input type="number" id="editPaq" value="${d.paquetes||0}"></div>
                        <div class="form-group"><label>Uni/Paq</label><input type="number" id="editUniPaq" value="${d.uniPorPaquete||6}"></div>
                        <div class="form-group"><label>Paq Dañados</label><input type="number" id="editPaqDan" value="${d.paquetesDanados||0}"></div>
                        <div class="form-group"><label>Uni Dañadas</label><input type="number" id="editUniDan" value="${d.unidadesDanadas||0}"></div>
                        <div class="form-group"><label>Vencimiento</label><input type="date" id="editVenc" value="${d.vencimiento||''}"></div>
                        <div class="form-group"><label>Observación</label><input id="editObs" value="${d.observacion||''}"></div>
                    </div>`;
                modal.style.display='flex';
                document.getElementById('btnGuardarEdicion').onclick=function(){
                    const np=parseInt(document.getElementById('editPaq').value)||0;
                    const nu=parseInt(document.getElementById('editUniPaq').value)||0;
                    const npd=parseInt(document.getElementById('editPaqDan').value)||0;
                    const nud=parseInt(document.getElementById('editUniDan').value)||0;
                    const tu=np*nu;const td=(npd*nu)+nud;
                    const su=Math.max(0,tu-td);const sp=Math.floor(su/nu);
                    db.collection('inventario').doc(docId).update({
                        sabor:document.getElementById('editSabor').value,
                        paquetes:np,uniPorPaquete:nu,totalUnidades:tu,
                        paquetesDanados:npd,unidadesDanadas:nud,
                        stockPaquetes:sp,stockUnidades:su,
                        vencimiento:document.getElementById('editVenc').value,
                        observacion:document.getElementById('editObs').value,
                        danado:(npd>0||nud>0)
                    }).then(()=>{modal.style.display='none';cargarStock();alert('✅ Actualizado');})
                    .catch(e=>alert('❌ '+e.message));
                };
            });
        }

        // ==================== CARGAR STOCK (ORDENADO POR VENCIMIENTO Y AGRUPADO POR CATEGORÍA) ====================
        function cargarStock(){
            const tbody=document.getElementById('stockTableBody');
            tbody.innerHTML='<tr><td colspan="8" class="loading">Cargando...</td></tr>';

            db.collection('inventario').get().then(snap=>{
                const todos=[];
                snap.forEach(doc=>{const d=doc.data();todos.push({id:doc.id,...d});});

                const search=(document.getElementById('stockSearch')?.value||'').toLowerCase();
                const fVenc=document.getElementById('stockFilterVencimiento')?.value||'todos';
                const fCat=document.getElementById('stockFilterCategoria')?.value||'todos';
                const hoy=new Date();hoy.setHours(0,0,0,0);
                const lim=new Date(hoy);lim.setDate(lim.getDate()+30);

                // Filtrar
                let filtrados=todos.filter(d=>{
                    if(search&&!d.producto.toLowerCase().includes(search)&&!(d.sabor||'').toLowerCase().includes(search)&&!d.presentacion.toLowerCase().includes(search))return false;
                    if(fCat!=='todos'){
                        const cat=d.categoria||'';
                        if(fCat==='cervezas'){if(!cat.includes('cervezas'))return false;}
                        else if(cat!==fCat)return false;
                    }
                    if(fVenc==='todos')return true;
                    const fv=d.vencimiento?new Date(d.vencimiento+'T00:00:00'):null;
                    if(fVenc==='vencido')return fv&&fv<hoy;
                    if(fVenc==='proximo')return fv&&fv>=hoy&&fv<=lim;
                    if(fVenc==='vigente')return!fv||fv>lim;
                    return true;
                });

                // ORDENAR por vencimiento (más cercano primero)
                filtrados.sort((a,b)=>{
                    const fa=a.vencimiento?new Date(a.vencimiento+'T00:00:00'):new Date('2099-01-01');
                    const fb=b.vencimiento?new Date(b.vencimiento+'T00:00:00'):new Date('2099-01-01');
                    return fa-fb;
                });

                // Agrupar por categoría
                const categorias={};
                filtrados.forEach(d=>{
                    const cat=d.categoria||'Sin categoría';
                    if(!categorias[cat])categorias[cat]=[];
                    categorias[cat].push(d);
                });

                // Orden de categorías deseado
                const ordenCat=['Sodas Mendocina','Cervezas en Lata','Cervezas en Botella','Energizantes y Maltas','Agua'];

                let rows='';
                ordenCat.forEach(catNombre=>{
                    if(categorias[catNombre]&&categorias[catNombre].length>0){
                        rows+=`<tr class="categoria-header"><td colspan="8">📂 ${catNombre} (${categorias[catNombre].length} lotes)</td></tr>`;
                        categorias[catNombre].forEach(d=>{
                            const fv=d.vencimiento?new Date(d.vencimiento+'T00:00:00'):null;
                            let clase='',badge='';
                            if(fv){
                                if(fv<hoy){clase='vencido';badge='<span class="badge badge-danger">VENCIDO</span>';}
                                else if(fv<=lim){clase='proximo-vencer';badge='<span class="badge badge-warning">PRÓXIMO</span>';}
                                else{clase='vigente';badge='<span class="badge badge-success">VIGENTE</span>';}
                            }
                            rows+=`<tr class="${clase}">
                                <td>${fv?fv.toLocaleDateString('es-BO'):'-'} ${badge}</td>
                                <td>${d.producto}</td><td>${d.sabor||'-'}</td><td>${d.presentacion}</td>
                                <td><strong>${d.stockPaquetes||0}</strong></td><td>${d.stockUnidades||0}</td>
                                <td>${clase.replace('-',' ').toUpperCase()}</td>
                                <td><button class="btn btn-xs btn-warning" onclick="editarIngreso('${d.id}')">✏️</button></td>
                            </tr>`;
                        });
                    }
                });

                // Categorías restantes
                Object.keys(categorias).forEach(cat=>{
                    if(!ordenCat.includes(cat)&&categorias[cat].length>0){
                        rows+=`<tr class="categoria-header"><td colspan="8">📂 ${cat} (${categorias[cat].length} lotes)</td></tr>`;
                        categorias[cat].forEach(d=>{
                            rows+=`<tr><td>${d.vencimiento||'-'}</td><td>${d.producto}</td><td>${d.sabor||'-'}</td><td>${d.presentacion}</td><td>${d.stockPaquetes||0}</td><td>${d.stockUnidades||0}</td><td></td><td><button class="btn btn-xs btn-warning" onclick="editarIngreso('${d.id}')">✏️</button></td></tr>`;
                        });
                    }
                });

                tbody.innerHTML=rows||'<tr><td colspan="8" style="text-align:center;">Sin productos</td></tr>';
            }).catch(e=>{tbody.innerHTML=`<tr><td colspan="8" style="color:red;">Error: ${e.message}</td></tr>`;});
        }

        // ==================== PRECIOS ====================
        function cargarPrecios(){
            const tbody=document.getElementById('preciosTableBody');
            tbody.innerHTML='<tr><td colspan="5" class="loading">Cargando...</td></tr>';
            const lista=[];
            Object.entries(catalogoCompleto).forEach(([k,cat])=>{
                if(cat.producto)cat.presentaciones.forEach(pr=>lista.push({cat:cat.categoria,prod:cat.producto,pres:pr}));
                else if(cat.productos)cat.productos.forEach(p=>p.presentaciones.forEach(pr=>lista.push({cat:cat.categoria,prod:p.nombre,pres:pr})));
            });
            db.collection('precios').get().then(snap=>{
                const precios={};snap.forEach(d=>{const x=d.data();precios[`${x.producto}|${x.presentacion}`]=x.precio;});
                tbody.innerHTML=lista.map(p=>{
                    const k=`${p.prod}|${p.pres}`;const v=precios[k]||0;
                    const id=`precio_${k.replace(/[^a-zA-Z0-9]/g,'_')}`;
                    return `<tr><td>${p.cat}</td><td>${p.prod}</td><td>${p.pres}</td>
                        <td><input type="number" id="${id}" value="${v}" min="0" step="0.01" style="width:100px;"></td>
                        <td><button class="btn btn-xs btn-primary" onclick="guardarPrecio('${p.prod}','${p.pres}','${id}')">💾</button></td></tr>`;
                }).join('');
            });
        }
        function guardarPrecio(prod,pres,inputId){
            const precio=parseFloat(document.getElementById(inputId).value)||0;
            const msg=document.getElementById('preciosMsg');
            db.collection('precios').where('producto','==',prod).where('presentacion','==',pres).get().then(snap=>{
                if(snap.empty)return db.collection('precios').add({producto:prod,presentacion:pres,precio});
                else{const b=db.batch();snap.forEach(d=>b.update(d.ref,{precio}));return b.commit();}
            }).then(()=>{msg.innerHTML=`✅ ${prod} ${pres}: ${precio.toFixed(2)} Bs`;msg.style.color='green';})
            .catch(e=>{msg.innerHTML='❌ '+e.message;msg.style.color='red';});
        }

        // ==================== SALIDA (CON AUTO-SELECCIÓN POR VENCIMIENTO) ====================
        function actualizarProductosSalida(){
            const cat=document.getElementById('salCategoria').value;
            const ps=document.getElementById('salProducto');
            const prs=document.getElementById('salPresentacion');
            const sc=document.getElementById('saborContainerSal');
            ps.innerHTML='<option value="">Seleccionar...</option>';
            prs.innerHTML='<option value="">Seleccionar...</option>';
            sc.style.display='none';
            document.getElementById('stockDisponibleInfo').style.display='none';
            if(!cat)return;
            const c=catalogoCompleto[cat];
            if(cat==='sodas'){sc.style.display='flex';ps.innerHTML='<option value="Mendocina">Mendocina</option>';ps.value='Mendocina';c.presentaciones.forEach(p=>prs.innerHTML+=`<option value="${p}">${p}</option>`);}
            else if(cat==='agua'){ps.innerHTML='<option value="Agua">Agua</option>';ps.value='Agua';c.presentaciones.forEach(p=>prs.innerHTML+=`<option value="${p}">${p}</option>`);}
            else if(c.productos){c.productos.forEach(p=>ps.innerHTML+=`<option value="${p.nombre}">${p.nombre}</option>`);ps.onchange=function(){actPresPorProd(cat,this.value,prs);};}
        }
        function actualizarPresentacionesSalida(){actPresPorProd(document.getElementById('salCategoria').value,document.getElementById('salProducto').value,document.getElementById('salPresentacion'));}

        function mostrarStockDisponible(){
            const prod=document.getElementById('salProducto').value;
            const pres=document.getElementById('salPresentacion').value;
            const saborEl=document.getElementById('salSabor');
            const sabor=saborEl&&document.getElementById('saborContainerSal').style.display!=='none'?saborEl.value:'';
            const infoDiv=document.getElementById('stockDisponibleInfo');
            const detalleDiv=document.getElementById('stockDisponibleDetalle');
            if(!prod||!pres){infoDiv.style.display='none';return;}

            let query=db.collection('inventario').where('producto','==',prod).where('presentacion','==',pres);
            if(sabor)query=query.where('sabor','==',sabor);

            query.get().then(snap=>{
                const lotes=[];
                snap.forEach(doc=>{const d=doc.data();if((d.stockPaquetes||0)>0||(d.stockUnidades||0)>0)lotes.push({id:doc.id,...d});});
                // Ordenar por vencimiento más cercano
                lotes.sort((a,b)=>new Date(a.vencimiento+'T00:00:00')-new Date(b.vencimiento+'T00:00:00'));
                
                if(lotes.length===0){
                    detalleDiv.innerHTML='<span style="color:red;">⚠️ Sin stock disponible</span>';
                }else{
                    const hoy=new Date();hoy.setHours(0,0,0,0);
                    let html='<table style="width:100%;font-size:0.8rem;"><thead><tr><th>Vencimiento</th><th>Paq Disp</th><th>Uni Disp</th><th>Estado</th></tr></thead><tbody>';
                    lotes.forEach(l=>{
                        const fv=new Date(l.vencimiento+'T00:00:00');
                        let icono='🟢';if(fv<hoy)icono='🔴';else if(fv<=new Date(hoy.getTime()+30*86400000))icono='🟡';
                        html+=`<tr><td>${icono} ${l.vencimiento}</td><td><strong>${l.stockPaquetes||0}</strong></td><td>${l.stockUnidades||0}</td><td>${fv<hoy?'VENCIDO':fv<=new Date(hoy.getTime()+30*86400000)?'PRÓXIMO':'VIGENTE'}</td></tr>`;
                    });
                    html+='</tbody></table>';
                    html+='<p style="margin-top:0.5rem;font-size:0.8rem;color:#666;">⚠️ Al agregar, se tomarán primero los lotes más próximos a vencer</p>';
                    detalleDiv.innerHTML=html;
                }
                infoDiv.style.display='block';
            });
        }

        function agregarProductoSalida(){
            const prod=document.getElementById('salProducto').value;
            const pres=document.getElementById('salPresentacion').value;
            const cantSolicitada=parseInt(document.getElementById('salCantidad').value)||0;
            const saborEl=document.getElementById('salSabor');
            const sabor=saborEl&&document.getElementById('saborContainerSal').style.display!=='none'?saborEl.value:'';

            if(!prod||!pres||cantSolicitada<=0){alert('Complete producto, presentación y cantidad');return;}

            // AUTO-SELECCIÓN por vencimiento
            let query=db.collection('inventario').where('producto','==',prod).where('presentacion','==',pres);
            if(sabor)query=query.where('sabor','==',sabor);

            query.get().then(snap=>{
                const lotes=[];
                snap.forEach(doc=>{const d=doc.data();if((d.stockPaquetes||0)>0)lotes.push({id:doc.id,...d});});
                lotes.sort((a,b)=>new Date(a.vencimiento+'T00:00:00')-new Date(b.vencimiento+'T00:00:00'));

                let restante=cantSolicitada;
                const seleccionados=[];
                for(const l of lotes){
                    if(restante<=0)break;
                    const tomar=Math.min(l.stockPaquetes||0,restante);
                    if(tomar>0){
                        seleccionados.push({...l,tomados:tomar});
                        restante-=tomar;
                    }
                }

                if(restante>0){
                    alert(`⚠️ Solo hay ${cantSolicitada-restante} paquetes disponibles. Faltan ${restante} paquetes.`);
                }

                // Obtener precio
                db.collection('precios').where('producto','==',prod).where('presentacion','==',pres).get().then(psnap=>{
                    let precio=0;
                    if(!psnap.empty)precio=psnap.docs[0].data().precio||0;

                    seleccionados.forEach(s=>{
                        const existente=productosEnSalida.find(x=>x.producto===prod&&x.sabor===sabor&&x.presentacion===pres&&x.vencimiento===s.vencimiento);
                        if(existente){
                            existente.cantidad+=s.tomados;
                            existente.subtotal=existente.cantidad*existente.precio;
                        }else{
                            productosEnSalida.push({
                                producto:prod,sabor, presentacion:pres,
                                cantidad:s.tomados,precio,
                                subtotal:s.tomados*precio,
                                vencimiento:s.vencimiento,
                                loteIds:[s.id]
                            });
                        }
                    });

                    renderizarTablaSalida();
                    document.getElementById('salCantidad').value='1';
                });
            });
        }

        function renderizarTablaSalida(){
            const tbody=document.getElementById('salidaTableBody');
            let tp=0,tb=0;
            if(productosEnSalida.length===0){
                tbody.innerHTML='<tr><td colspan="8" style="text-align:center;color:#999;">No hay productos</td></tr>';
            }else{
                tbody.innerHTML=productosEnSalida.map((p,i)=>{
                    tp+=p.cantidad;tb+=p.subtotal;
                    return `<tr>
                        <td>${p.producto}</td><td>${p.sabor||'-'}</td><td>${p.presentacion}</td>
                        <td>${p.cantidad}</td><td>${p.precio.toFixed(2)}</td><td><strong>${p.subtotal.toFixed(2)}</strong></td>
                        <td>${p.vencimiento||'-'}</td>
                        <td><button class="btn btn-xs btn-danger" onclick="eliminarProdSalida(${i})">🗑️</button></td>
                    </tr>`;
                }).join('');
            }
            document.getElementById('salidaTotalPaquetes').textContent=tp;
            document.getElementById('salidaTotalBs').textContent=tb.toFixed(2);
        }

        function eliminarProdSalida(i){productosEnSalida.splice(i,1);renderizarTablaSalida();}

        function registrarSalida(){
            const chofer=document.getElementById('salidaChofer').value.trim();
            const destino=document.getElementById('salidaDestino').value.trim();
            const observacion=document.getElementById('salidaObservacion').value.trim();
            const msg=document.getElementById('salidaMsg');
            if(!chofer){msg.innerHTML='❌ Ingrese el chofer';msg.style.color='red';return;}
            if(productosEnSalida.length===0){msg.innerHTML='❌ Agregue productos';msg.style.color='red';return;}

            const totalBs=productosEnSalida.reduce((s,p)=>s+p.subtotal,0);
            const totalPaq=productosEnSalida.reduce((s,p)=>s+p.cantidad,0);

            const salidaData={
                tipo:'salida',chofer,destino:destino||'No especificado',
                observacion:observacion||'',
                productos:productosEnSalida,totalBs,totalPaquetes:totalPaq,
                estado:'pendiente',
                fecha:firebase.firestore.FieldValue.serverTimestamp(),
                fechaStr:new Date().toISOString().split('T')[0],
                hora:new Date().toLocaleTimeString('es-BO',{hour:'2-digit',minute:'2-digit'})
            };

            // Descontar stock
            const batch=db.batch();
            const ref=db.collection('salidas').doc();
            batch.set(ref,salidaData);
            productosEnSalida.forEach(p=>{
                // Buscar el lote en inventario y descontar
                db.collection('inventario').where('producto','==',p.producto)
                    .where('presentacion','==',p.presentacion)
                    .where('vencimiento','==',p.vencimiento).limit(1).get()
                    .then(snap=>{
                        snap.forEach(doc=>{
                            const actual=doc.data().stockPaquetes||0;
                            batch.update(doc.ref,{stockPaquetes:Math.max(0,actual-p.cantidad)});
                        });
                    });
            });

            batch.commit().then(()=>{
                msg.innerHTML=`✅ Salida registrada - ${totalPaq} paq - ${totalBs.toFixed(2)} Bs`;
                msg.style.color='green';
                document.getElementById('salidaChofer').value='';document.getElementById('salidaDestino').value='';
                document.getElementById('salidaObservacion').value='';
                productosEnSalida=[];renderizarTablaSalida();
                cargarStock();cargarSalidasPendientes();
            }).catch(e=>{msg.innerHTML='❌ '+e.message;msg.style.color='red';});
        }

        // ==================== RENDICIÓN ====================
        function cargarSalidasPendientes(){
            const select=document.getElementById('rendicionSalidaId');
            select.innerHTML='<option value="">Cargando...</option>';
            db.collection('salidas').get().then(snap=>{
                const pendientes=[];
                snap.forEach(doc=>{const d=doc.data();if(d.estado==='pendiente')pendientes.push({id:doc.id,...d});});
                pendientes.sort((a,b)=>b.fechaStr.localeCompare(a.fechaStr));
                select.innerHTML='<option value="">Seleccionar salida pendiente...</option>';
                if(pendientes.length===0)select.innerHTML+='<option value="" disabled>No hay pendientes</option>';
                else pendientes.forEach(d=>select.innerHTML+=`<option value="${d.id}">${d.chofer} - ${d.fechaStr} ${d.hora} - ${d.totalBs?.toFixed(2)||'0'} Bs</option>`);
            }).catch(e=>{select.innerHTML=`<option value="">Error: ${e.message}</option>`;});
        }

        function cargarDatosRendicion(){
            const id=document.getElementById('rendicionSalidaId').value;
            const div=document.getElementById('rendicionDetalle');
            div.innerHTML='';if(!id)return;
            db.collection('salidas').doc(id).get().then(doc=>{
                if(!doc.exists){div.innerHTML='<p style="color:red;">No encontrada</p>';return;}
                const d=doc.data();
                let html=`<fieldset><legend>📋 Salida: ${d.chofer}</legend>
                    <p><strong>Fecha:</strong> ${d.fechaStr} ${d.hora} | <strong>Destino:</strong> ${d.destino||'-'}</p>
                    <p><strong>Observación:</strong> ${d.observacion||'Ninguna'}</p>
                    <p><strong>Total:</strong> ${d.totalBs.toFixed(2)} Bs | <strong>Paquetes:</strong> ${d.totalPaquetes}</p></fieldset>
                    <fieldset><legend>🔄 Registrar Retorno</legend>
                    <div class="table-container"><table>
                        <thead><tr><th>Producto</th><th>Sabor</th><th>Presentación</th><th>Salió</th><th>Devuelto</th><th>Dañado</th></tr></thead><tbody>`;
                d.productos.forEach((p,i)=>{
                    html+=`<tr><td>${p.producto}</td><td>${p.sabor||'-'}</td><td>${p.presentacion}</td><td>${p.cantidad}</td>
                        <td><input type="number" id="retDev_${i}" min="0" max="${p.cantidad}" value="0" onchange="calcRend(${d.totalBs})"></td>
                        <td><input type="number" id="retDan_${i}" min="0" max="${p.cantidad}" value="0" onchange="calcRend(${d.totalBs})"></td></tr>`;
                });
                html+=`</tbody></table></div>
                    <div class="totals-box"><div class="total-item"><span class="label">Total Devuelto</span><span class="value" id="rendDevuelto">0.00 Bs</span></div>
                    <div class="total-item"><span class="label">A Rendir</span><span class="value" id="rendRendir">${d.totalBs.toFixed(2)} Bs</span></div></div>
                    <button class="btn btn-success" onclick="confirmarRendicion('${id}',${d.totalBs})">✅ Confirmar Rendición</button></fieldset>`;
                div.innerHTML=html;
                window._rendProd=d.productos;
            });
        }

        function calcRend(totalSalida){
            const prods=window._rendProd||[];let td=0;
            prods.forEach((p,i)=>{const dev=parseInt(document.getElementById('retDev_'+i)?.value)||0;const dan=parseInt(document.getElementById('retDan_'+i)?.value)||0;td+=(dev+dan)*p.precio;});
            document.getElementById('rendDevuelto').textContent=td.toFixed(2)+' Bs';
            document.getElementById('rendRendir').textContent=(totalSalida-td).toFixed(2)+' Bs';
        }

        function confirmarRendicion(salidaId,totalSalida){
            const prods=window._rendProd||[];let td=0;const ret=[];
            prods.forEach((p,i)=>{
                const dev=parseInt(document.getElementById('retDev_'+i)?.value)||0;
                const dan=parseInt(document.getElementById('retDan_'+i)?.value)||0;
                const vendido=p.cantidad-dev-dan;td+=(dev+dan)*p.precio;
                ret.push({...p,devuelto:dev,danado:dan,vendido});
            });
            const data={tipo:'rendicion',salidaId,totalSalida,totalDevuelto:td,totalRendir:totalSalida-td,productos:ret,
                fecha:firebase.firestore.FieldValue.serverTimestamp(),
                fechaStr:new Date().toISOString().split('T')[0],hora:new Date().toLocaleTimeString('es-BO',{hour:'2-digit',minute:'2-digit'})};
            const batch=db.batch();
            batch.set(db.collection('rendiciones').doc(),data);
            batch.update(db.collection('salidas').doc(salidaId),{estado:'rendido',retorno:ret,totalDevuelto:td,totalRendido:totalSalida-td});
            batch.commit().then(()=>{
                document.getElementById('rendicionMsg').innerHTML=`✅ Rendición - A rendir: ${(totalSalida-td).toFixed(2)} Bs`;
                document.getElementById('rendicionMsg').style.color='green';
                document.getElementById('rendicionDetalle').innerHTML='';
                document.getElementById('rendicionSalidaId').value='';
                cargarSalidasPendientes();cargarStock();
            }).catch(e=>{document.getElementById('rendicionMsg').innerHTML='❌ '+e.message;document.getElementById('rendicionMsg').style.color='red';});
        }

        // ==================== HISTORIAL (MÁS NUEVO PRIMERO, CON FILTRO DE FECHAS) ====================
        function cargarHistorial(){
            const tbody=document.getElementById('historialTableBody');
            tbody.innerHTML='<tr><td colspan="4" class="loading">Cargando...</td></tr>';
            Promise.all([
                db.collection('inventario').where('tipo','==','ingreso').get(),
                db.collection('salidas').get(),
                db.collection('rendiciones').get()
            ]).then(([ing,sal,ren])=>{
                let todos=[];
                ing.forEach(d=>{const dt=d.data();todos.push({f:dt.fechaStr+' '+dt.hora,t:'INGRESO',det:`📥 ${dt.producto} ${dt.sabor||''} ${dt.presentacion} - ${dt.stockPaquetes||dt.paquetes||0} paq`,m:(dt.stockPaquetes||dt.paquetes||0)*(dt.precio||0),fechaStr:dt.fechaStr});});
                sal.forEach(d=>{const dt=d.data();todos.push({f:dt.fechaStr+' '+dt.hora,t:'SALIDA',det:`🚚 ${dt.chofer} → ${dt.destino||'-'} - ${dt.totalPaquetes||0} paq${dt.observacion?' | Obs: '+dt.observacion:''}`,m:dt.totalBs||0,fechaStr:dt.fechaStr});});
                ren.forEach(d=>{const dt=d.data();todos.push({f:dt.fechaStr+' '+dt.hora,t:'RENDICIÓN',det:`🔄 Rendido: ${dt.totalRendir?.toFixed(2)||0} Bs`,m:dt.totalRendir||0,fechaStr:dt.fechaStr});});
                // Ordenar más nuevo primero
                todos.sort((a,b)=>b.f.compare(a.f));
                
                const search=(document.getElementById('histSearch')?.value||'').toLowerCase();
                const tipoF=document.getElementById('histTipo')?.value||'todos';
                const desde=document.getElementById('histFechaDesde')?.value||'';
                const hasta=document.getElementById('histFechaHasta')?.value||'';
                
                const filtrados=todos.filter(t=>{
                    if(tipoF!=='todos'&&t.t.toLowerCase()!==tipoF)return false;
                    if(search&&!t.det.toLowerCase().includes(search))return false;
                    if(desde&&t.fechaStr<desde)return false;
                    if(hasta&&t.fechaStr>hasta)return false;
                    return true;
                });
                
                tbody.innerHTML=filtrados.map(t=>`<tr><td>${t.f}</td><td>${t.t}</td><td>${t.det}</td><td><strong>${t.m.toFixed(2)} Bs</strong></td></tr>`).join('')||'<tr><td colspan="4" style="text-align:center;">Sin registros</td></tr>';
            }).catch(e=>{tbody.innerHTML=`<tr><td colspan="4" style="color:red;">Error: ${e.message}</td></tr>`;});
        }

        // ==================== INICIALIZAR ====================
        document.addEventListener('DOMContentLoaded',()=>{renderizarTablaSalida();});
        document.getElementById('loginPassword').addEventListener('keypress',function(e){if(e.key==='Enter')login();});
        logDebug('🚀 Sistema v3.0 listo');
    </script>
</body>
</html>
