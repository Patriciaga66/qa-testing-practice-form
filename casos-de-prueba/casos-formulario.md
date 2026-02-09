# 🧪 Casos de Prueba - Formulario de Registro DemoQA

## Información del Documento
- **Proyecto:** Testing Manual - DemoQA Practice Form
- **Módulo:** Formulario de Registro Estudiantil
- **Fecha:** 8 de Febrero 2025
- **Tester:** Paty Dixon
- **Total de casos:** 12

---

## TC-001: Envío exitoso con todos los campos completos

**Prioridad:** Alta | **Severidad:** Crítica

**Objetivo:** Verificar que el formulario se envía correctamente con todos los datos válidos

**Precondiciones:**
- Navegador Chrome abierto
- Conexión a internet activa
- Página del formulario cargada

**Datos de Prueba:**
- First Name: Juan
- Last Name: Pérez
- Email: juan.perez@test.com
- Gender: Male
- Mobile: 3001234567
- Date of Birth: 15 Jan 1995
- Subjects: Maths
- Hobbies: Sports
- Current Address: Calle 123 #45-67
- State: NCR
- City: Delhi

**Pasos:**
1. Navegar a https://demoqa.com/automation-practice-form
2. Ingresar "Juan" en campo First Name
3. Ingresar "Pérez" en campo Last Name
4. Ingresar "juan.perez@test.com" en campo Email
5. Seleccionar radio button "Male"
6. Ingresar "3001234567" en campo Mobile
7. Hacer clic en Date of Birth y seleccionar "15 Jan 1995"
8. En Subjects, escribir "Maths" y seleccionar de la lista
9. Marcar checkbox "Sports"
10. Ingresar "Calle 123 #45-67" en Current Address
11. En dropdown State, seleccionar "NCR"
12. En dropdown City, seleccionar "Delhi"
13. Hacer clic en botón "Submit"

**Resultado Esperado:**
- Aparece modal de confirmación "Thanks for submitting the form"
- Modal muestra tabla con todos los datos ingresados correctamente
- No hay mensajes de error
- Todos los campos se muestran con la información correcta

**Estado:** ⏳ Pendiente de ejecución

---

## TC-002: Validación de campo obligatorio - First Name vacío

**Prioridad:** Alta | **Severidad:** Alta

**Objetivo:** Verificar que el sistema valida campo obligatorio First Name

**Precondiciones:**
- Página del formulario cargada

**Pasos:**
1. Navegar al formulario
2. Dejar First Name vacío
3. Completar todos los demás campos obligatorios
4. Hacer clic en Submit

**Resultado Esperado:**
- Sistema NO envía el formulario
- Campo First Name se marca con borde rojo o mensaje de error
- Aparece indicación de que el campo es obligatorio
- Usuario permanece en la página del formulario

**Estado:** ⏳ Pendiente

---

## TC-003: Validación de formato de Email - Sin @

**Prioridad:** Alta | **Severidad:** Media

**Objetivo:** Verificar validación de formato de email

**Datos de Prueba:**
- Email inválido: "correosinformato.com" (sin @)

**Pasos:**
1. Completar formulario con datos válidos
2. Ingresar email SIN símbolo @ en campo Email
3. Completar campos restantes
4. Hacer clic en Submit

**Resultado Esperado:**
- Sistema valida formato de email
- Muestra mensaje de error en campo Email
- No permite enviar el formulario
- Campo Email se marca como inválido

**Estado:** ⏳ Pendiente

---

## TC-004: Validación de Mobile - Menos de 10 dígitos

**Prioridad:** Alta | **Severidad:** Alta

**Objetivo:** Verificar validación de longitud de número móvil

**Datos de Prueba:**
- Mobile: 12345 (solo 5 dígitos)

**Pasos:**
1. Completar formulario con datos válidos
2. Ingresar solo 5 dígitos en campo Mobile
3. Hacer clic en Submit

**Resultado Esperado:**
- Sistema rechaza el envío
- Muestra mensaje indicando que Mobile debe tener 10 dígitos
- Campo Mobile se marca como inválido

**Estado:** ⏳ Pendiente

---

## TC-005: Validación de Mobile - Más de 10 dígitos

**Prioridad:** Alta | **Severidad:** Alta

**Objetivo:** Verificar que el sistema rechaza números con más de 10 dígitos

**Datos de Prueba:**
- Mobile: 30012345678901 (14 dígitos)

**Pasos:**
1. Completar formulario
2. Ingresar 14 dígitos en Mobile
3. Intentar enviar

**Resultado Esperado:**
- Sistema limita entrada a 10 dígitos
- O muestra mensaje de error si permite ingresar más
- No permite envío con longitud incorrecta

**Estado:** ⏳ Pendiente

---

## TC-006: Selección múltiple de Hobbies

**Prioridad:** Media | **Severidad:** Baja

**Objetivo:** Verificar que se pueden seleccionar múltiples hobbies

**Pasos:**
1. Completar formulario con datos válidos
2. Marcar checkbox "Sports"
3. Marcar checkbox "Reading"
4. Marcar checkbox "Music"
5. Enviar formulario

**Resultado Esperado:**
- Todos los hobbies marcados aparecen en la confirmación
- Sistema acepta múltiples selecciones
- Modal muestra: "Sports, Reading, Music"

**Estado:** ⏳ Pendiente

---

## TC-007: Dependencia State → City

**Prioridad:** Alta | **Severidad:** Media

**Objetivo:** Verificar que City solo se habilita después de seleccionar State

**Pasos:**
1. Cargar formulario
2. Observar campo City (debe estar deshabilitado)
3. Seleccionar un State (ej: "NCR")
4. Observar campo City

**Resultado Esperado:**
- Inicialmente City está deshabilitado/gris
- Al seleccionar State, City se habilita
- City muestra opciones correspondientes al State seleccionado
- Para NCR muestra: Delhi, Gurgaon, Noida

**Estado:** ⏳ Pendiente

---

## TC-008: Envío con solo campos obligatorios

**Prioridad:** Alta | **Severidad:** Media

**Objetivo:** Verificar que el formulario se envía con solo campos obligatorios

**Datos mínimos:**
- First Name: Ana
- Last Name: García
- Gender: Female
- Mobile: 3109876543
- State: Haryana
- City: Karnal

**Pasos:**
1. Completar SOLO campos obligatorios
2. Dejar campos opcionales vacíos
3. Hacer clic en Submit

**Resultado Esperado:**
- Formulario se envía exitosamente
- Modal muestra solo datos ingresados
- Campos opcionales vacíos no causan error

**Estado:** ⏳ Pendiente

---

## TC-009: Caracteres especiales en First Name

**Prioridad:** Media | **Severidad:** Baja

**Objetivo:** Verificar comportamiento con caracteres especiales

**Datos de Prueba:**
- First Name: "Juan@#$"

**Pasos:**
1. Ingresar nombre con caracteres especiales
2. Completar formulario
3. Intentar enviar

**Resultado Esperado:**
- Sistema acepta o rechaza caracteres especiales consistentemente
- Si acepta: muestra en confirmación
- Si rechaza: muestra mensaje de validación

**Estado:** ⏳ Pendiente

---

## TC-010: Fecha de nacimiento futura

**Prioridad:** Baja | **Severidad:** Baja

**Objetivo:** Verificar validación de fecha lógica

**Datos de Prueba:**
- Date of Birth: 15 Jan 2030 (fecha futura)

**Pasos:**
1. Completar formulario
2. Seleccionar fecha futura en Date of Birth
3. Enviar formulario

**Resultado Esperado:**
- Sistema valida que la fecha no puede ser futura
- O acepta cualquier fecha y muestra en confirmación
- Comportamiento debe ser consistente

**Estado:** ⏳ Pendiente

---

## TC-011: Mobile con letras

**Prioridad:** Alta | **Severidad:** Alta

**Objetivo:** Verificar que Mobile solo acepta números

**Datos de Prueba:**
- Mobile: "ABC1234567"

**Pasos:**
1. Intentar ingresar letras en campo Mobile
2. Observar comportamiento

**Resultado Esperado:**
- Campo no permite ingresar letras
- Solo acepta dígitos numéricos
- Muestra mensaje si se intenta ingresar texto

**Estado:** ⏳ Pendiente

---

## TC-012: Email con formato válido pero dominio inusual

**Prioridad:** Baja | **Severidad:** Baja

**Objetivo:** Verificar aceptación de emails con dominios válidos

**Datos de Prueba:**
- Email: "test@ejemplo.co.uk"

**Pasos:**
1. Ingresar email con dominio de múltiples niveles
2. Completar formulario
3. Enviar

**Resultado Esperado:**
- Sistema acepta email con formato técnicamente válido
- Email aparece correctamente en confirmación

**Estado:** ⏳ Pendiente

---

## 📊 Resumen de Casos de Prueba

| Prioridad | Cantidad |
|-----------|----------|
| Alta | 8 |
| Media | 3 |
| Baja | 3 |
| **Total** | **12** |

| Estado | Cantidad |
|--------|----------|
| Diseñados | 12 |
| Ejecutados | 0 |
| Pasados | 0 |
| Fallados | 0 |

---

**Nota:** Estos casos serán ejecutados en Chrome y Firefox para validar compatibilidad cross-browser.