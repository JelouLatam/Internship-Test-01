# Prueba de Pasantía React - Dashboard de Países

## Descripción General

¡Bienvenido a la Evaluación de Pasantía React de Jelou! En esta prueba, construirás una aplicación de **Dashboard de Países** usando React y la API REST Countries. Esta evaluación está diseñada para evaluar tu comprensión de los conceptos fundamentales de React.

**Duración:** 8 horas
**Dificultad:** Nivel principiante
**Enfoque:** Frontend (React)

---

## Lo Que Construirás

Una aplicación web que muestra información sobre países de todo el mundo con las siguientes características:

![Vista Previa del Dashboard de Países](https://ibb.co/v409GL01)

### Características Principales (Obligatorias)

1. **Lista de Países**
   - Mostrar países en un diseño de cuadrícula/tarjetas
   - Cada tarjeta debe mostrar: bandera, nombre, capital, población y región

2. **Funcionalidad de Búsqueda**
   - Búsqueda/filtrado en tiempo real por nombre del país
   - La búsqueda debe ser insensible a mayúsculas/minúsculas

3. **Filtro por Región**
   - Filtrar países por continente/región (África, Américas, Asia, Europa, Oceanía)
   - Puede implementarse como menú desplegable o botones

4. **Vista Detallada del País**
   - Hacer clic en una tarjeta de país para ver información expandida
   - Mostrar: nombre nativo, idiomas, monedas, fronteras, subregión, dominio de nivel superior
   - Incluir un botón "Volver" para regresar a la lista

5. **Estados de Carga y Error**
   - Mostrar indicador de carga mientras se obtienen los datos
   - Mostrar mensajes de error amigables si la API falla
   - Incluir un botón "Reintentar" para solicitudes fallidas

---

## API REST Countries

**URL Base:** `https://restcountries.com/v3.1`

### Endpoints que Necesitarás

| Endpoint | Descripción | Ejemplo |
|----------|-------------|---------|
| `/all` | Obtener todos los países | `https://restcountries.com/v3.1/all` |
| `/name/{nombre}` | Buscar por nombre del país | `https://restcountries.com/v3.1/name/peru` |
| `/region/{region}` | Filtrar por región | `https://restcountries.com/v3.1/region/europe` |
| `/alpha/{codigo}` | Obtener país por código | `https://restcountries.com/v3.1/alpha/col` |

### Campos Útiles en la Respuesta de la API

```javascript
{
  name: {
    common: "Colombia",        // Nombre para mostrar
    official: "República de Colombia",
    nativeName: { ... }
  },
  capital: ["Bogotá"],         // Array de capitales
  population: 50882891,
  region: "Americas",
  subregion: "South America",
  flags: {
    png: "https://...",        // URL de imagen de la bandera
    svg: "https://..."
  },
  languages: {
    spa: "Spanish"             // Objeto de idiomas
  },
  currencies: {
    COP: {
      name: "Colombian peso",
      symbol: "$"
    }
  },
  borders: ["BRA", "ECU", "PAN", "PER", "VEN"],  // Códigos de países fronterizos
  tld: [".co"],                // Dominio de nivel superior
  cca3: "COL"                  // Código de país de 3 letras
}
```

### Consejos sobre la API
- No requiere autenticación
- La API es gratuita y no tiene límites de uso para uso razonable
- Usa `fetch()` o `axios` para hacer las solicitudes
- Maneja los casos donde algunos campos pueden estar ausentes (ej. algunos países no tienen capital)

---

## Requisitos Técnicos

### Debe Usar
- **React** (Create React App, Vite, o Next.js)
- **React Hooks** (`useState`, `useEffect`)
- **Componentes Funcionales**

### Estilos (Elige Uno)
- CSS simple / CSS Modules
- Tailwind CSS
- Styled Components
- Cualquier framework CSS (Bootstrap, Material UI, etc.)

### Estructura del Proyecto (Recomendada)
```
src/
├── components/
│   ├── CountryCard.jsx
│   ├── CountryList.jsx
│   ├── CountryDetail.jsx
│   ├── SearchBar.jsx
│   ├── RegionFilter.jsx
│   └── Loading.jsx
├── hooks/
│   └── useCountries.js (hook personalizado opcional)
├── App.jsx
├── App.css
└── index.js
```

---

## Primeros Pasos

### 1. Crear Tu Proyecto

```bash
# Usando Vite (Recomendado)
npm create vite@latest countries-dashboard -- --template react
cd countries-dashboard
npm install

# O usando Create React App
npx create-react-app countries-dashboard
cd countries-dashboard
```

### 2. Iniciar el Servidor de Desarrollo

```bash
npm run dev    # Vite
# O
npm start      # Create React App
```

### 3. Probar la API

```javascript
// Prueba en la consola de tu navegador o componente
fetch('https://restcountries.com/v3.1/all?fields=name')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

---

## Criterios de Evaluación

| Criterio | Peso | Qué Buscamos |
|----------|------|--------------|
| **Funcionalidad** | 35% | Todas las características funcionan correctamente |
| **Fundamentos de React** | 25% | Uso adecuado de useState, useEffect, props, composición de componentes |
| **Calidad del Código** | 20% | Código limpio, legible y bien organizado |
| **UI/UX** | 10% | Interfaz intuitiva, buen diseño visual |
| **Documentación y Video** | 10% | README claro, proceso de pensamiento explicado |

---

## Puntos Extra (+20% Máximo)

| Característica Extra | Puntos | Descripción |
|---------------------|--------|-------------|
| Diseño Responsivo | +5% | Funciona bien en móvil y tablet |
| Modo Oscuro/Claro | +3% | Alternar entre temas |
| Funcionalidad de Ordenamiento | +3% | Ordenar por nombre, población o área |
| Sistema de Favoritos | +4% | Guardar países favoritos en localStorage |
| TypeScript | +5% | Usar TypeScript en lugar de JavaScript |
| Pruebas Unitarias | +5% | Agregar pruebas para componentes o utilidades |
| Despliegue en Vivo | +3% | Desplegar en Vercel, Netlify o similar |

---

## Requisitos de Entrega

### 1. Repositorio de Código
- Sube tu código a un **repositorio público de GitHub**
- Incluye un `README.md` completo (usa la plantilla proporcionada)

### 2. El README Debe Incluir
- Instrucciones de configuración del proyecto
- Tecnologías utilizadas
- Características implementadas
- Capturas de pantalla de tu aplicación
- Cualquier desafío que enfrentaste y cómo lo resolviste

### 3. Video de Loom (3-5 minutos)
Graba un video corto que incluya:
- Breve demostración de tu aplicación
- Recorrido del código de un componente del que estés orgulloso
- Explicación de un desafío que enfrentaste y cómo lo resolviste

### 4. Formato de Entrega
Completa el `SUBMISSION_TEMPLATE_ES.md` e incluye:
- URL del repositorio de GitHub
- URL del video de Loom
- URL de la demo en vivo (si está desplegada)

---

## Cronograma

| Tiempo | Hito |
|--------|------|
| Hora 1 | Configuración del proyecto, prueba de API, planificación |
| Horas 2-3 | Visualización de lista de países, tarjetas |
| Horas 4-5 | Funcionalidad de búsqueda y filtro |
| Hora 6 | Vista detallada del país |
| Hora 7 | Estados de carga/error, pulido de estilos |
| Hora 8 | Documentación, grabación de video, entrega |

---

## Consejos para el Éxito

1. **Empieza Simple** - Haz que la lista básica funcione antes de agregar características
2. **Haz Commits Frecuentes** - Haz commits pequeños y frecuentes con mensajes claros
3. **Prueba Mientras Construyes** - No esperes hasta el final para probar tus características
4. **Lee la Respuesta de la API** - Imprime los datos en consola para entender su estructura
5. **Maneja Casos Especiales** - Algunos países tienen datos faltantes (sin capital, etc.)
6. **Mantén la Limpieza** - Código legible > código ingenioso

---

## Recursos

- [Documentación de React](https://react.dev/)
- [Documentación de REST Countries API](https://restcountries.com/)
- [MDN - Usando Fetch](https://developer.mozilla.org/es/docs/Web/API/Fetch_API/Using_Fetch)
- [Guía de React Hooks](https://react.dev/reference/react)

---

## ¿Preguntas?

Si tienes alguna pregunta sobre los requisitos o encuentras problemas técnicos con la API, por favor contacta a tu contacto en Jelou.

**¡Buena suerte! ¡Estamos emocionados de ver lo que construyas!** 🚀
