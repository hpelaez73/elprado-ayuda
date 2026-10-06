# Documentar pantalla Delphi

## Objetivo

Crear o actualizar la ayuda de usuario de una pantalla de El Prado a partir de su implementación Delphi.

## Fuentes

Para documentar un formulario:

1. Leer el archivo `.pas`.
2. Leer el archivo `.dfm`.
3. Identificar la clase base.
4. Seguir código adicional solamente cuando sea necesario para comprender una acción visible al usuario.
5. Buscar documentación existente antes de crear o modificar la página.

## Qué documentar

Describir únicamente comportamiento relevante para el usuario:

- propósito de la pantalla;
- campos y filtros;
- información mostrada;
- botones y acciones;
- validaciones;
- restricciones;
- consecuencias relevantes de una operación.

No documentar detalles de implementación como nombres de clases, datasets, SQL, componentes Delphi o nombres internos de campos.

## Evidencia

No inventar comportamiento. Si algo no puede determinarse a partir del código o de documentación existente, indicarlo para revisión en lugar de asumirlo.

## Ayuda contextual

Todo formulario documentable que herede de `TFormSimple` utiliza su `ClassName` como identificador de ayuda.

Para una clase `TFormConsultaNotificaciones`, crear o actualizar:

```text
docs/pantallas/TFormConsultaNotificaciones.md
```

El nombre del archivo debe coincidir exactamente con el `ClassName`.

## Tipos de documentación

Seleccionar el template según la función de la pantalla, no solamente según su clase base Delphi.

Tipos iniciales: consulta, ABM, diálogo y proceso.

Los templates son orientativos. Se pueden omitir secciones que no aporten información útil.

## Estilo

La ayuda está dirigida al usuario final.

- Usar frases directas y breves.
- Priorizar instrucciones como **Seleccione**, **Ingrese** y **Presione**.
- Explicar qué hace la pantalla y cómo utilizarla.
- Evitar explicar cómo está programada.

## Prioridad de evidencia

Para describir textos visibles al usuario, usar esta prioridad:

1. Caption, Label, encabezados y textos definidos en el DFM.
2. Mensajes y comportamiento definidos en el PAS.
3. SQL y datasets solamente para comprender la lógica funcional.

No exponer nombres internos de campos si existe una etiqueta visible equivalente.

## Interpretación de consultas

Cuando el comportamiento se deduzca de SQL complejo:

- describir el resultado en términos funcionales;
- no explicar la consulta técnica;
- evitar afirmar más de lo que el código permite demostrar;
- si existe ambigüedad, usar una redacción conservadora.