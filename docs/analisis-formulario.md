# 📋 Análisis del Formulario - DemoQA Practice Form

## Información General
- **URL:** https://demoqa.com/automation-practice-form
- **Tipo:** Formulario de registro estudiantil
- **Fecha de análisis:** 8 de Febrero 2025
- **Analista:** Paty Dixon

## Objetivo del Formulario
Capturar información de estudiantes incluyendo datos personales, contacto, educación y preferencias.

## Elementos Identificados

### 1. Campos de Texto Obligatorios
| Campo | Tipo | Validación | Obligatorio |
|-------|------|------------|-------------|
| First Name | Text input | Alfanumérico | Sí |
| Last Name | Text input | Alfanumérico | Sí |
| Email | Email input | Formato email válido | Sí |
| Mobile Number | Number input | 10 dígitos numéricos | Sí |

### 2. Campos de Selección
| Campo | Tipo | Opciones | Obligatorio |
|-------|------|----------|-------------|
| Gender | Radio buttons | Male, Female, Other | Sí |
| Date of Birth | Date picker | Calendario | No |
| Subjects | Multi-select autocomplete | Lista de materias | No |
| Hobbies | Checkboxes | Sports, Reading, Music | No |

### 3. Campos de Texto Opcionales
| Campo | Tipo | Validación | Obligatorio |
|-------|------|------------|-------------|
| Current Address | Text area | Texto libre | No |

### 4. Campos Dependientes
| Campo | Tipo | Dependencia | Obligatorio |
|-------|------|-------------|-------------|
| State | Dropdown | Independiente | Sí |
| City | Dropdown | Depende de State seleccionado | Sí |

### 5. Otros Elementos
- **Picture:** Upload de imagen (opcional)
- **Submit:** Botón de envío del formulario

## Validaciones Observadas

### ✅ Validaciones que SÍ funcionan:
- Campos obligatorios marcados con asterisco (*)
- Email debe tener formato válido (incluir @)
- Mobile debe ser exactamente 10 dígitos
- City se habilita solo después de seleccionar State

### ⚠️ Posibles áreas de testing:
- Validación de caracteres especiales en nombres
- Límite máximo de caracteres en campos de texto
- Comportamiento con fechas futuras/pasadas
- Validación de formato de imagen en Picture upload
- Comportamiento al enviar con campos opcionales vacíos

## Flujo de Usuario Esperado

1. Usuario completa campos obligatorios (First Name, Last Name, Email, Gender, Mobile)
2. Usuario completa campos opcionales según necesidad
3. Usuario selecciona State (esto habilita City)
4. Usuario selecciona City
5. Usuario hace clic en Submit
6. Sistema valida datos
7. Sistema muestra modal de confirmación con datos ingresados

## Casos de Borde Identificados

- ✅ Todos los campos obligatorios completos
- ❌ Campos obligatorios vacíos
- ❌ Email sin formato válido
- ❌ Mobile con menos/más de 10 dígitos
- ⚠️ Caracteres especiales en nombres
- ⚠️ Fechas de nacimiento no realistas (ej: año 1800 o futuro)
- ⚠️ Seleccionar City sin seleccionar State primero

## Consideraciones de Testing

### Browsers a Probar:
- Chrome (última versión)
- Firefox (última versión)
- Edge (última versión)

### Tipos de Prueba Aplicables:
- ✅ Functional Testing
- ✅ Validation Testing
- ✅ UI/UX Testing
- ✅ Cross-browser Testing
- ✅ Negative Testing

## Riesgos Identificados
1. Dependencia entre State y City puede causar confusión
2. No hay indicación visual clara de campos obligatorios completados
3. Modal de confirmación puede no ser accesible en algunos navegadores

## Conclusiones del Análisis
El formulario presenta una buena estructura con validaciones básicas implementadas. Existen múltiples escenarios de prueba tanto positivos como negativos que permitirán validar la robustez de la aplicación.

**Total de elementos a probar:** 11 campos + 1 botón = 12 elementos
**Casos de prueba estimados:** Mínimo 15 casos