<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>INO · Documentación de Software</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet"/>
    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #f5f7fb;
            color: #1e1e2f;
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: white;
            border-radius: 32px;
            box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.15);
            padding: 2.5rem 2rem;
            transition: 0.3s;
        }

        /* ===== HEADER ===== */
        .header {
            border-bottom: 3px solid #17375E;
            padding-bottom: 1.5rem;
            margin-bottom: 2rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: flex-end;
        }

        .header h1 {
            font-size: 2.2rem;
            font-weight: 700;
            color: #17375E;
            letter-spacing: -0.5px;
        }

        .header h1 span {
            background: #2E75B6;
            color: white;
            font-size: 1rem;
            font-weight: 600;
            padding: 0.2rem 0.8rem;
            border-radius: 40px;
            margin-left: 12px;
            display: inline-block;
            vertical-align: middle;
        }

        .header .sub {
            font-size: 1rem;
            color: #404040;
            font-weight: 400;
        }

        .badge {
            background: #eef3fa;
            padding: 0.5rem 1rem;
            border-radius: 60px;
            font-size: 0.9rem;
            font-weight: 600;
            color: #17375E;
            border: 1px solid #cbd6e3;
        }

        /* ===== SECCIONES ===== */
        section {
            margin-bottom: 2.8rem;
        }

        h2 {
            font-size: 1.6rem;
            font-weight: 700;
            color: #17375E;
            border-left: 6px solid #2E75B6;
            padding-left: 0.9rem;
            margin-bottom: 1.2rem;
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .card {
            background: #f9fafc;
            border-radius: 20px;
            padding: 1.5rem 1.2rem;
            border: 1px solid #e6ecf3;
            transition: 0.2s;
        }

        .card:hover {
            border-color: #2E75B6;
            box-shadow: 0 8px 18px rgba(46, 117, 182, 0.08);
        }

        .card h3 {
            font-size: 1.1rem;
            font-weight: 700;
            color: #17375E;
            margin-bottom: 0.3rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
        }

        .card .tag {
            font-size: 0.7rem;
            background: #2E75B6;
            color: white;
            padding: 0.1rem 0.6rem;
            border-radius: 20px;
            font-weight: 600;
            letter-spacing: 0.3px;
        }

        .card p {
            color: #404040;
            font-size: 0.95rem;
            margin-top: 0.3rem;
        }

        .card ul {
            list-style: none;
            margin-top: 0.5rem;
        }

        .card ul li {
            font-size: 0.9rem;
            padding: 0.2rem 0;
            border-bottom: 1px dashed #e0e6ef;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .card ul li::before {
            content: "▹";
            color: #2E75B6;
            font-weight: 700;
        }

        .badge-blue {
            background: #17375E;
            color: white;
            font-size: 0.7rem;
            font-weight: 600;
            padding: 0.2rem 0.7rem;
            border-radius: 30px;
            display: inline-block;
        }

        .tool-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 0.7rem;
        }

        .tool-item {
            background: white;
            border: 1px solid #dce3ec;
            padding: 0.2rem 0.9rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
            color: #17375E;
        }

        /* ===== TABLA DE NORMAS ===== */
        .norma-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.9rem;
        }

        .norma-table th {
            background: #17375E;
            color: white;
            padding: 0.7rem 0.8rem;
            text-align: left;
            font-weight: 600;
        }

        .norma-table td {
            padding: 0.7rem 0.8rem;
            border-bottom: 1px solid #e6ecf3;
            vertical-align: top;
        }

        .norma-table tr:last-child td {
            border-bottom: none;
        }

        .check {
            color: #1f8b4c;
            font-weight: 700;
        }

        .cross {
            color: #b33;
            font-weight: 700;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 700px) {
            .container {
                padding: 1.5rem 1rem;
            }
            .grid-2 {
                grid-template-columns: 1fr;
            }
            .header {
                flex-direction: column;
                align-items: flex-start;
                gap: 0.5rem;
            }
            .header h1 {
                font-size: 1.8rem;
            }
        }

        .footer {
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 2px solid #e6ecf3;
            text-align: center;
            font-size: 0.85rem;
            color: #404040;
        }

        .footer a {
            color: #17375E;
            font-weight: 600;
            text-decoration: none;
        }

        .footer a:hover {
            text-decoration: underline;
        }

        .highlight {
            background: #e5edf7;
            padding: 0.2rem 0.4rem;
            border-radius: 6px;
            font-weight: 500;
        }
    </style>
</head>
<body>

<div class="container">

    <!-- ========== HEADER ========== -->
    <div class="header">
        <div>
            <h1>
                📘 Documentación de Sistemas
                <span>M3.4</span>
            </h1>
            <div class="sub">
                INO · Bachillerato Técnico en Desarrollo de Software
            </div>
        </div>
        <div class="badge">
            👨‍🏫 Prof. Juan Francisco Hernández · 2026
        </div>
    </div>

    <!-- ========== INTRO ========== -->
    <section>
        <p style="font-size: 1.1rem; color: #1e1e2f; max-width: 800px;">
            <strong>Etapa 1 – Decidir</strong> · Estrategia documental,
            benchmarking de herramientas, matriz de diseño y borrador del manual.
            Proyecto basado en <span class="highlight">ISO/IEC 26514</span> e
            <span class="highlight">IEEE 829</span>.
        </p>
    </section>

    <!-- ========== PRODUCTOS ========== -->
    <section>
        <h2>📦 Productos Entregables</h2>
        <div class="grid-2">
            <div class="card">
                <h3>🔍 Investigación de Normas</h3>
                <p>IEEE 829 e ISO/IEC 26514 · 5 puntos clave cada una.</p>
                <ul>
                    <li>Documentación de pruebas clara y trazable</li>
                    <li>Manual accesible para usuario final</li>
                    <li>Estructura lógica y ejemplos visuales</li>
                </ul>
            </div>
            <div class="card">
                <h3>📊 Análisis de Manuales</h3>
                <p>Microsoft Word 365 (ejemplar) vs README traducido (deficiente).</p>
                <ul>
                    <li>✔ Estructura, lenguaje claro, capturas</li>
                    <li>✘ Traducción literal, sin índice, errores</li>
                </ul>
            </div>
            <div class="card">
                <h3>⚙️ Benchmarking de Herramientas</h3>
                <p>Capturadores, procesadores, editores de video y diseño.</p>
                <div class="tool-list">
                    <span class="tool-item">ShareX</span>
                    <span class="tool-item">Lightshot</span>
                    <span class="tool-item">OBS Studio</span>
                    <span class="tool-item">Word</span>
                    <span class="tool-item">GIMP</span>
                    <span class="tool-item">Canva</span>
                </div>
                <p style="margin-top: 0.5rem; font-size: 0.85rem;">
                    ✅ Elección final: ShareX · Word · OBS · GIMP
                </p>
            </div>
            <div class="card">
                <h3>🎨 Matriz de Diseño</h3>
                <p>Identidad visual, estilos, cajas de advertencia y reglas de captura.</p>
                <ul>
                    <li>Tipografía: <strong>Montserrat</strong> + <strong>Calibri</strong></li>
                    <li>Colores: #17375E · #2E75B6 · #404040</li>
                    <li>Plantilla <code>Plantilla_Maestra_M3.4.dotx</code></li>
                </ul>
            </div>
        </div>
    </section>

    <!-- ========== TABLA NORMAS ========== -->
    <section>
        <h2>📋 Cumplimiento de Normas</h2>
        <table class="norma-table">
            <thead>
                <tr>
                    <th>Aspecto</th>
                    <th>Microsoft Word 365</th>
                    <th>README traducido</th>
                </tr>
            </thead>
            <tbody>
                <tr><td>Organización</td><td><span class="check">✔</span> Excelente</td><td><span class="cross">✘</span> Desordenado</td></tr>
                <tr><td>Claridad del lenguaje</td><td><span class="check">✔</span> Accesible</td><td><span class="cross">✘</span> Confuso</td></tr>
                <tr><td>Capturas de pantalla</td><td><span class="check">✔</span> Con anotaciones</td><td><span class="cross">✘</span> Sin contexto</td></tr>
                <tr><td>Manejo de errores</td><td><span class="check">✔</span> Sección dedicada</td><td><span class="cross">✘</span> Ausente</td></tr>
                <tr><td>Cumple ISO/IEC 26514</td><td><span class="check">✔</span> Sí</td><td><span class="cross">✘</span> No</td></tr>
            </tbody>
        </table>
    </section>

    <!-- ========== GLOSARIO ========== -->
    <section>
        <h2>📖 Glosario (usuario final)</h2>
        <div class="grid-2">
            <div class="card">
                <h3>🔹 Términos técnicos → lenguaje claro</h3>
                <ul>
                    <li><strong>Trigger</strong> → Regla automática</li>
                    <li><strong>Foreign Key</strong> → Enlace entre listas</li>
                    <li><strong>Query</strong> → Pregunta al sistema</li>
                    <li><strong>Deploy</strong> → Abrir tienda renovada</li>
                    <li><strong>Rollback</strong> → Botón deshacer</li>
                </ul>
            </div>
            <div class="card">
                <h3>🔸 Ejemplo de simplificación</h3>
                <p style="font-style: italic; background: #eef3fa; padding: 0.5rem; border-radius: 12px;">
                    “El trigger de la FK disparó una violación de constraint…”
                </p>
                <p style="font-weight: 600; color: #17375E;">
                    ✅ “El sistema no pudo guardar la información porque detectó un dato incorrecto.”
                </p>
            </div>
        </div>
    </section>

    <!-- ========== HERRAMIENTAS ========== -->
    <section>
        <h2>🛠️ Herramientas Seleccionadas</h2>
        <div class="grid-2">
            <div class="card">
                <h3>📸 Capturadores</h3>
                <p><span class="badge-blue">Principal</span> <strong>ShareX</strong> – anotaciones avanzadas</p>
                <p><span class="badge-blue">Alternativa</span> Lightshot – capturas rápidas</p>
            </div>
            <div class="card">
                <h3>📝 Procesadores</h3>
                <p><span class="badge-blue">Principal</span> <strong>Microsoft Word</strong> – fidelidad al PDF</p>
                <p><span class="badge-blue">Respaldo</span> Google Docs – colaborativo</p>
            </div>
            <div class="card">
                <h3>🎬 Edición de video</h3>
                <p><span class="badge-blue">Principal</span> <strong>OBS Studio</strong> – grabación gratuita</p>
                <p><span class="badge-blue">Futuro</span> CapCut / Clipchamp</p>
            </div>
            <div class="card">
                <h3>🎨 Diseño / Anotación</h3>
                <p><span class="badge-blue">Principal</span> <strong>GIMP</strong> – precisión multiplataforma</p>
                <p><span class="badge-blue">Descartado</span> Canva · Paint.NET</p>
            </div>
        </div>
    </section>

    <!-- ========== EVIDENCIA ========== -->
    <section>
        <h2>🖼️ Evidencia de Capturas</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 1rem; justify-content: center;">
            <div style="background: #f0f4fa; border-radius: 20px; padding: 0.8rem; text-align: center; flex: 1 1 150px;">
                <div style="font-size: 3rem;">🖥️</div>
                <p style="font-size: 0.8rem; color: #404040;">ShareX · región</p>
            </div>
            <div style="background: #f0f4fa; border-radius: 20px; padding: 0.8rem; text-align: center; flex: 1 1 150px;">
                <div style="font-size: 3rem;">⚡</div>
                <p style="font-size: 0.8rem; color: #404040;">Lightshot · selección</p>
            </div>
            <div style="background: #f0f4fa; border-radius: 20px; padding: 0.8rem; text-align: center; flex: 1 1 150px;">
                <div style="font-size: 3rem;">🎥</div>
                <p style="font-size: 0.8rem; color: #404040;">OBS · grabación 30s</p>
            </div>
            <div style="background: #f0f4fa; border-radius: 20px; padding: 0.8rem; text-align: center; flex: 1 1 150px;">
                <div style="font-size: 3rem;">✏️</div>
                <p style="font-size: 0.8rem; color: #404040;">GIMP · anotación</p>
            </div>
        </div>
        <p style="text-align: center; margin-top: 0.8rem; font-size: 0.9rem; color: #404040;">
            Todas las capturas siguen el estándar: <strong>1280×720 · PNG · flechas rojas · recuadros amarillos</strong>
        </p>
    </section>

    <!-- ========== FOOTER ========== -->
    <div class="footer">
        <p>
            📂 <strong>Repositorio de Documentación</strong> · Módulo 3.4 ·
            Instituto Nacional de Osicala (INO) · 2026
        </p>
        <p style="margin-top: 0.3rem;">
            <a href="#">📄 Ver plantilla .dotx</a> ·
            <a href="#">📊 Ver matriz de diseño</a> ·
            <a href="#">📖 Ver glosario completo</a>
        </p>
        <p style="margin-top: 0.8rem; font-size: 0.75rem; color: #808080;">
            Basado en estándares ISO/IEC 26514 e IEEE 829 · Prof. Juan Francisco Hernández
        </p>
    </div>

</div>
<!-- /container -->

</body>
</html>
