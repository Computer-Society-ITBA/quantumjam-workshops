# Quantum Jam 2026

Notebooks del curso de introducción a la computación cuántica con Qiskit, dictado en el marco de la Quantum Jam 2026 y el Qiskit Fall Fest 2026 en el ITBA.

Cuatro clases con ejercicios en Qiskit, dos notebooks de soluciones y dos anexos.

## Contenido

| Notebook | Tema |
|---|---|
| `Clase_1,_Parte_1_Computación_Cuántica.ipynb` | Fundamentos: kets, bras, operadores |
| `Clase_1,_Parte_2_Computación_Cuántica.ipynb` | Fundamentos (continuación) |
| `Soluciones_Clase_1.ipynb` | Soluciones de la clase 1 |

## Cómo correr los notebooks

Tres opciones. Si no sabés cuál elegir, arrancá con Google Colab.

### Google Colab (recomendado)

1. Abrí Google Colab: https://colab.research.google.com/
2. `Archivo` > `Subir cuaderno` > seleccioná el `.ipynb`.
3. Corré la primera celda (instala Qiskit en el runtime de Colab).
4. Para guardar tu progreso: `Archivo` > `Guardar una copia en Drive`.

En cada sesión nueva de Colab hay que volver a correr la celda de instalación (el runtime se apaga por inactividad).

### Local

Requiere Python 3.10, 3.11 o 3.12.

```bash
python -m venv qiskit-class
```

Activar el entorno:

Windows PowerShell:
```powershell
qiskit-class\Scripts\Activate.ps1
```

Mac / Linux:
```bash
source qiskit-class/bin/activate
```

Instalar dependencias:

```bash
pip install jupyter qiskit[visualization] qiskit-ibm-runtime qiskit-aer qiskit_qasm3_import
```

Levantar Jupyter:

```bash
jupyter notebook
```

En las clases siguientes solo hay que activar el entorno y correr `jupyter notebook` otra vez. No hay que reinstalar nada.

### qBraid

Todo lo que sigue queda en el tier gratis. Los notebooks solo usan simuladores locales (`AerSimulator`, `FakeVigoV2`), así que no gastan créditos.

1. Crear cuenta en https://account.qbraid.com (no pide tarjeta).
2. Elegir la imagen `Free` (2 vCPU, 4 GB RAM) y `Launch Lab`.
3. En la pestaña `ENVIRONMENTS` (izquierda), buscar `Qiskit` e instalarlo. Ya trae `qiskit`, `qiskit-aer` y `qiskit-ibm-runtime`; se puede saltear el `!pip install` del notebook. Si falta `qiskit_qasm3_import`, correr solo esa línea:
   ```
   !pip install qiskit_qasm3_import
   ```
4. Subir el `.ipynb` desde la pestaña `FILES` (ícono de subir o arrastrar).
5. Abrir el notebook y arriba a la derecha cambiar el kernel al entorno Qiskit del paso 3. Sin este paso, `import qiskit` falla aunque el entorno esté instalado.

Autoguarda, pero conviene hacer `Ctrl+S` (`Cmd+S` en Mac) al terminar cada sección. El Lab se apaga solo por inactividad.

## Problemas comunes

| Problema | Dónde | Solución |
|---|---|---|
| `python: command not found` | Local | Reinstalar Python; en Windows, tildar "Add to PATH" en el instalador |
| `No module named 'qiskit'` | Local | Activar el entorno virtual antes de `jupyter notebook` |
| `No module named 'qiskit'` | qBraid | Cambiar el kernel al entorno Qiskit |
| `pip install` muy lento | qBraid | Usar el entorno pre-armado, no reinstalar |
| No se ven los gráficos | Ambos | Instalar con `qiskit[visualization]`, no solo `qiskit` |
| Lab no arranca | qBraid | Esperar unos minutos; si sigue, refrescar la página |
