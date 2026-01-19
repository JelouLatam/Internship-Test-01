# React Internship Test - Countries Dashboard

## Overview

Welcome to the Jelou React Internship Assessment! In this test, you will build a **Countries Dashboard** application using React and the REST Countries API. This assessment is designed to evaluate your understanding of fundamental React concepts.

**Duration:** 8 hours
**Difficulty:** Beginner-friendly
**Focus:** Frontend (React)

---

## What You'll Build

A web application that displays information about countries around the world with the following features:

![Countries Dashboard Mockup](https://via.placeholder.com/800x400?text=Countries+Dashboard+Preview)

### Core Features (Required)

1. **Country List Display**
   - Display countries in a grid/card layout
   - Each card should show: flag, name, capital, population, and region

2. **Search Functionality**
   - Real-time search/filtering by country name
   - Search should be case-insensitive

3. **Region Filter**
   - Filter countries by continent/region (Africa, Americas, Asia, Europe, Oceania)
   - Can be implemented as dropdown or buttons

4. **Country Detail View**
   - Click on a country card to see expanded information
   - Show: native name, languages, currencies, borders, subregion, top-level domain
   - Include a "Back" button to return to the list

5. **Loading & Error States**
   - Show loading indicator while fetching data
   - Display user-friendly error messages if API fails
   - Include a "Retry" button for failed requests

---

## REST Countries API

**Base URL:** `https://restcountries.com/v3.1`

### Endpoints You'll Need

| Endpoint | Description | Example |
|----------|-------------|---------|
| `/all` | Get all countries | `https://restcountries.com/v3.1/all?fields=name` |
| `/name/{name}` | Search by country name | `https://restcountries.com/v3.1/name/peru` |
| `/region/{region}` | Filter by region | `https://restcountries.com/v3.1/region/europe` |
| `/alpha/{code}` | Get country by code | `https://restcountries.com/v3.1/alpha/col` |

### Useful Fields in API Response

```javascript
{
  name: {
    common: "Colombia",        // Display name
    official: "Republic of Colombia",
    nativeName: { ... }
  },
  capital: ["Bogotá"],         // Array of capitals
  population: 50882891,
  region: "Americas",
  subregion: "South America",
  flags: {
    png: "https://...",        // Flag image URL
    svg: "https://..."
  },
  languages: {
    spa: "Spanish"             // Object of languages
  },
  currencies: {
    COP: {
      name: "Colombian peso",
      symbol: "$"
    }
  },
  borders: ["BRA", "ECU", "PAN", "PER", "VEN"],  // Border country codes
  tld: [".co"],                // Top-level domain
  cca3: "COL"                  // 3-letter country code
}
```

### API Tips
- No authentication required
- The API is free and has no rate limits for reasonable use
- Use `fetch()` or `axios` to make requests
- Handle cases where some fields might be missing (e.g., some countries have no capital)

---

## Technical Requirements

### Must Use
- **React** (Create React App, Vite, or Next.js)
- **React Hooks** (`useState`, `useEffect`)
- **Functional Components**

### Styling (Choose One)
- Plain CSS / CSS Modules
- Tailwind CSS
- Styled Components
- Any CSS framework (Bootstrap, Material UI, etc.)

### Project Structure (Recommended)
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
│   └── useCountries.js (optional custom hook)
├── App.jsx
├── App.css
└── index.js
```

---

## Getting Started

### 1. Create Your Project

```bash
# Using Vite (Recommended)
npm create vite@latest countries-dashboard -- --template react
cd countries-dashboard
npm install

# OR using Create React App
npx create-react-app countries-dashboard
cd countries-dashboard
```

### 2. Start Development Server

```bash
npm run dev    # Vite
# OR
npm start      # Create React App
```

### 3. Test the API

```javascript
// Test in your browser console or component
fetch('https://restcountries.com/v3.1/all')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

---

## Evaluation Criteria

| Criterion | Weight | What We're Looking For |
|-----------|--------|------------------------|
| **Functionality** | 35% | All features work correctly |
| **React Fundamentals** | 25% | Proper use of useState, useEffect, props, component composition |
| **Code Quality** | 20% | Clean, readable, well-organized code |
| **UI/UX** | 10% | Intuitive interface, good visual design |
| **Documentation & Video** | 10% | Clear README, explained thought process |

---

## Bonus Points (+20% Maximum)

| Bonus Feature | Points | Description |
|---------------|--------|-------------|
| Responsive Design | +5% | Works well on mobile and tablet |
| Dark/Light Mode | +3% | Toggle between themes |
| Sort Functionality | +3% | Sort by name, population, or area |
| Favorites System | +4% | Save favorite countries to localStorage |
| TypeScript | +5% | Use TypeScript instead of JavaScript |
| Unit Tests | +5% | Add tests for components or utilities |
| Live Deployment | +3% | Deploy to Vercel, Netlify, or similar |

---

## Submission Requirements

### 1. Code Repository
- Push your code to a **public GitHub repository**
- Include a complete `README.md` (use the provided template)

### 2. README Must Include
- Project setup instructions
- Technologies used
- Features implemented
- Screenshots of your application
- Any challenges you faced and how you solved them

### 3. Loom Video (3-5 minutes)
Record a short video that includes:
- Brief demo of your application
- Code walkthrough of one component you're proud of
- Explanation of a challenge you faced and how you solved it

### 4. Submission Format
Fill out the `SUBMISSION_TEMPLATE.md` and include:
- GitHub repository URL
- Loom video URL
- Live demo URL (if deployed)

---

## Timeline

| Time | Milestone |
|------|-----------|
| Hour 1 | Project setup, API testing, planning |
| Hours 2-3 | Country list display, cards |
| Hours 4-5 | Search and filter functionality |
| Hour 6 | Country detail view |
| Hour 7 | Loading/error states, styling polish |
| Hour 8 | Documentation, video recording, submission |

---

## Tips for Success

1. **Start Simple** - Get the basic list working before adding features
2. **Commit Often** - Make small, frequent commits with clear messages
3. **Test as You Build** - Don't wait until the end to test your features
4. **Read the API Response** - Log the data to understand its structure
5. **Handle Edge Cases** - Some countries have missing data (no capital, etc.)
6. **Keep It Clean** - Readable code > clever code

---

## Resources

- [React Documentation](https://react.dev/)
- [REST Countries API Documentation](https://restcountries.com/)
- [MDN - Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
- [React Hooks Guide](https://react.dev/reference/react)

---

## Questions?

If you have any questions about the requirements or encounter technical issues with the API, please reach out to your contact at Jelou.

**Good luck! We're excited to see what you build!** 🚀
