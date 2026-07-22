<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Documentación M3.4 · INO</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: #0d1117;
            color: #c9d1d9;
            padding: 2rem;
            display: flex;
            justify-content: center;
        }
        .container {
            max-width: 900px;
            width: 100%;
            background: #161b22;
            padding: 2.5rem;
            border-radius: 16px;
            border: 1px solid #30363d;
        }
        h1 { font-size: 2.2rem; color: #f0f6fc; border-bottom: 2px solid #17375E; padding-bottom: 0.5rem; }
        h2 { color: #f0f6fc; margin: 1.5rem 0 0.8rem 0; font-size: 1.4rem; }
        h3 { color: #8b949e; font-weight: 400; margin-bottom: 0.5rem; }
        .badge { display: inline-block; padding: 0.3rem 0.8rem; border-radius: 20px; font-size: 0.75rem; font-weight: 600; margin: 0.2rem; }
        .badge-blue { background: #17375E; color: white; }
        .badge-light { background: #2E75B6; color: white; }
        .badge-green { background: #1f8b4c; color: white; }
        .badge-gray { background: #30363d; color: #c9d1d9; }
        table { width: 100%; border-collapse: collapse; margin: 0.8rem 0; }
        th { background: #17375E; color: white; padding: 0.6rem; text-align: left; font-weight: 600; }
        td { padding: 0.6rem; border-bottom: 1px solid #30363d; }
        tr:hover { background: #1c2333; }
        a { color: #58a6ff; text-decoration: none; }
        a:hover { text-decoration: underline; }
        .btn { display: inline-block; padding: 0.4rem 1rem; border-radius: 6px; font-weight: 600; font-size: 0.85rem; margin: 0.2rem; }
        .btn-pdf { background: #17375E; color: white; }
        .btn-red { background: #da3633; color: white; }
        .btn-word { background: #2B579A; color: white; }
        .footer { margin-top: 2rem; padding-top: 1rem; border-top: 1px solid #30363d; text-align: center; color: #8b949e; }
        .quote { font-style: italic; color: #8b949e; padding: 0.8rem 0; border-left: 3px solid #17375E; padding-left: 1rem; margin: 1rem 0; }
        details { margin: 0.5rem 0; }
        summary { cursor: pointer; color: #58a6ff; font-weight: 600; }
        .pdf-container { background: #0d1117; padding: 0.5rem; border-radius: 8px; margin-top: 0.5rem; }
        .pdf-container object { width: 100%; height: 500px; border-radius: 6px; }
        .center { text-align: center; }
        .badge-group { display: flex; flex-wrap: wrap; gap: 0.3rem; margin: 0.5rem 0; }
        .table-wrap { overflow-x: auto; }
    </style>
</head>
<body>
    <div class="container">

        <!-- TÍTULO -->
        <h1>📘 Documentación de Sistemas</h1>
        <h3>Módulo 3.4 · INO · 2026</h3>

        <!-- BADGES -->
        <div class="badge-group">
            <span class="badge badge-blue">📌 Módulo 3.4</span>
            <span class="badge badge-light">📋 ISO-IEC 26514</span>
            <span class="badge badge-blue">📋 IEEE 829</span>
            <span class="badge badge-green">✅ Entregado</span>
            <span class="badge badge-gray">📅 2026</span>
        </div>

        <p><strong>Instituto Nacional de Osicala</strong><br/>
        <em>Bachillerato Técnico en Desarrollo de Software</em></p>

        <p>👨‍🏫 Prof. Juan Francisco Hernández · 📚 Sección "A"</p>

        <div class="quote">
            "Definir la estrategia documental antes de escribir una sola línea"
        </div>

        <hr style="border-color: #30363d; margin: 1.5rem 0;" />

        <!-- DOCUMENTO -->
        <h2>📄 Documento</h2>

        <div class="table-wrap">
            <table>
                <tr>
                    <th style="text-align:center;">📖 Ver en línea</th>
                    <th style="text-align:center;" colspan="2">📥 Descargar</th>
                </tr>
                <tr>
                    <td style="text-align:center;">
                        <a href="https://github.com/19791179-coder/juan-documentacion/blob/main/etapa_decidir_1_2_3_4.pdf" class="btn btn-pdf">📄 Abrir PDF</a>
                    </td>
                    <td style="text-align:center;">
                        <a href="https://raw.githubusercontent.com/19791179-coder/juan-documentacion/main/etapa_decidir_1_2_3_4.pdf" class="btn btn-red">📄 PDF</a>
                    </td>
                    <td style="text-align:center;">
                        <a href="https://raw.githubusercontent.com/19791179-coder/juan-documentacion/main/etapa_decidir_1_2_3_4.docx" class="btn btn-word">📝 Word</a>
                    </td>
                </tr>
            </table>
        </div>

        <!-- VISTA PREVIA PDF -->
        <details>
            <summary><b>📑 Vista previa del PDF</b></summary>
            <div class="pdf-container">
                <object data="https://raw.githubusercontent.com/19791179-coder/juan-documentacion/main/etapa_decidir_1_2_3_4.pdf" type="application/pdf">
                    <p>⚠️ No se puede mostrar. <a href="https://github.com/19791179-coder/juan-documentacion/blob/main/etapa_decidir_1_2_3_4.pdf">Abrir PDF</a></p>
                </object>
            </div>
        </details>

        <hr style="border-color: #30363d; margin: 1.5rem 0;" />

        <!-- PRODUCTOS -->
        <h2>📦 Productos</h2>

        <div class="table-wrap">
            <table>
                <tr><th>#</th><th>Producto</th><th>Estado</th></tr>
                <tr><td style="text-align:center;">①</td><td>Investigación de Normas</td><td style="text-align:center;">✅</td></tr>
                <tr><td style="text-align:center;">②</td><td>Análisis de Manuales</td><td style="text-align:center;">✅</td></tr>
                <tr><td style="text-align:center;">③</td><td>Benchmarking de Herramientas</td><td style="text-align:center;">✅</td></tr>
                <tr><td style="text-align:center;">④</td><td>Matriz de Diseño</td><td style="text-align:center;">✅</td></tr>
                <tr><td style="text-align:center;">⑤</td><td>Borrador del Manual</td><td style="text-align:center;">✅</td></tr>
            </table>
        </div>

        <hr style="border-color: #30363d; margin: 1.5rem 0;" />

        <!-- HERRAMIENTAS -->
        <h2>🛠️ Herramientas</h2>

        <div class="table-wrap">
            <table>
                <tr><th>Categoría</th><th>Herramienta</th><th style="text-align:center;">🏆</th></tr>
                <tr><td>📸 Capturador</td><td>ShareX</td><td style="text-align:center;">⭐</td></tr>
                <tr><td>📝 Procesador</td><td>Microsoft Word</td><td style="text-align:center;">⭐</td></tr>
                <tr><td>🎬 Video</td><td>OBS Studio</td><td style="text-align:center;">⭐</td></tr>
                <tr><td>🎨 Diseño</td><td>GIMP</td><td style="text-align:center;">⭐</td></tr>
            </table>
        </div>

        <hr style="border-color: #30363d; margin: 1.5rem 0;" />

        <!-- EQUIPO -->
        <h2>👥 Equipo</h2>

        <div class="table-wrap">
            <table>
                <tr><th>Rol</th><th>Nombre</th></tr>
                <tr><td>👨‍🏫 Docente</td><td>Prof. Juan Francisco Hernández</td></tr>
                <tr><td>🏫 Institución</td><td>Instituto Nacional de Osicala</td></tr>
                <tr><td>📘 Módulo</td><td>3.4 - Elaboración de Documentación de Sistemas</td></tr>
            </table>
        </div>

        <hr style="border-color: #30363d; margin: 1.5rem 0;" />

        <!-- FOOTER -->
        <div class="footer">
            <p><strong>📘 "La buena documentación no se escribe, se diseña"</strong></p>
            <p style="margin-top:0.8rem;">
                <a href="https://github.com/19791179-coder" style="color:#58a6ff;">🐙 GitHub: 19791179-coder</a> ·
                <a href="#" style="color:#58a6ff;">🏫 INO - Instituto Nacional de Osicala</a>
            </p>
            <p style="font-size:0.8rem; color:#8b949e;">Hecho con 🧠 en El Salvador</p>
        </div>

    </div>
</body>
</html>
