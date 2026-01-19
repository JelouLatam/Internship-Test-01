# Evaluation Rubric - Countries Dashboard

> **Internal Document:** For evaluators only. Do not share with candidates.

---

## Scoring Overview

| Category | Weight | Max Points |
|----------|--------|------------|
| Functionality | 35% | 35 |
| React Fundamentals | 25% | 25 |
| Code Quality | 20% | 20 |
| UI/UX | 10% | 10 |
| Documentation & Video | 10% | 10 |
| **Base Total** | **100%** | **100** |
| Bonus Features | +20% | +20 |
| **Maximum Possible** | **120%** | **120** |

---

## Detailed Scoring Criteria

### 1. Functionality (35 points)

#### Country List Display (8 points)
| Score | Criteria |
|-------|----------|
| 8 | All countries display correctly with flag, name, capital, population, region |
| 6 | Most information displays, minor issues with some fields |
| 4 | Basic list works but missing several data points |
| 2 | List displays but significant data issues |
| 0 | Does not display country list |

#### Search Functionality (7 points)
| Score | Criteria |
|-------|----------|
| 7 | Real-time search works perfectly, case-insensitive |
| 5 | Search works but has minor issues (case-sensitive, delay) |
| 3 | Basic search works but buggy |
| 1 | Search attempted but doesn't work properly |
| 0 | No search functionality |

#### Region Filter (7 points)
| Score | Criteria |
|-------|----------|
| 7 | Filter by all regions works correctly, clear UI |
| 5 | Filter works for most regions, minor issues |
| 3 | Basic filtering works but incomplete |
| 1 | Filter attempted but buggy |
| 0 | No region filter |

#### Country Detail View (7 points)
| Score | Criteria |
|-------|----------|
| 7 | Full detail view with all required info, back button works |
| 5 | Detail view works, missing some information |
| 3 | Basic detail view, significant missing data |
| 1 | Detail view attempted but broken |
| 0 | No detail view |

#### Loading & Error States (6 points)
| Score | Criteria |
|-------|----------|
| 6 | Loading indicator present, errors handled gracefully with retry |
| 4 | Loading OR error handling present, not both |
| 2 | Basic loading state, poor error handling |
| 0 | No loading/error handling |

---

### 2. React Fundamentals (25 points)

#### useState Usage (8 points)
| Score | Criteria |
|-------|----------|
| 8 | Appropriate state management, no unnecessary state |
| 6 | Good state management with minor inefficiencies |
| 4 | State works but poorly organized or redundant |
| 2 | State management attempted but incorrect |
| 0 | No understanding of useState |

#### useEffect Usage (8 points)
| Score | Criteria |
|-------|----------|
| 8 | Correct usage for data fetching, proper dependencies, cleanup if needed |
| 6 | useEffect works but minor issues (missing dependencies, no cleanup) |
| 4 | Basic useEffect usage with issues |
| 2 | useEffect attempted but incorrect implementation |
| 0 | No understanding of useEffect |

#### Props & Component Composition (9 points)
| Score | Criteria |
|-------|----------|
| 9 | Excellent component breakdown, proper props usage, reusable components |
| 7 | Good component structure, mostly proper props |
| 5 | Adequate components, some prop drilling issues |
| 3 | Poor component structure, everything in App.js |
| 0 | No component separation |

---

### 3. Code Quality (20 points)

#### Code Organization (7 points)
| Score | Criteria |
|-------|----------|
| 7 | Well-organized file structure, logical grouping |
| 5 | Adequate organization with minor issues |
| 3 | Disorganized but functional |
| 1 | Very disorganized |
| 0 | Single file or extremely poor organization |

#### Readability (7 points)
| Score | Criteria |
|-------|----------|
| 7 | Clean, readable code, meaningful variable names, consistent style |
| 5 | Generally readable with some inconsistencies |
| 3 | Difficult to read in places |
| 1 | Hard to follow |
| 0 | Unreadable |

#### Best Practices (6 points)
| Score | Criteria |
|-------|----------|
| 6 | Follows React best practices, no console errors |
| 4 | Minor deviations from best practices |
| 2 | Several bad practices |
| 0 | Ignores best practices entirely |

---

### 4. UI/UX (10 points)

#### Visual Design (5 points)
| Score | Criteria |
|-------|----------|
| 5 | Polished, professional appearance |
| 4 | Good design with minor improvements needed |
| 3 | Adequate, functional design |
| 2 | Basic design, needs work |
| 1 | Poor visual design |
| 0 | No styling |

#### User Experience (5 points)
| Score | Criteria |
|-------|----------|
| 5 | Intuitive navigation, clear feedback, smooth interactions |
| 4 | Good UX with minor friction points |
| 3 | Functional but not intuitive |
| 2 | Confusing navigation or feedback |
| 1 | Poor user experience |
| 0 | Unusable |

---

### 5. Documentation & Video (10 points)

#### README Quality (5 points)
| Score | Criteria |
|-------|----------|
| 5 | Complete README with setup instructions, screenshots, explanations |
| 4 | Good README, minor omissions |
| 3 | Adequate README, missing some sections |
| 2 | Basic README, missing key information |
| 1 | Minimal README |
| 0 | No README |

#### Loom Video (5 points)
| Score | Criteria |
|-------|----------|
| 5 | Clear demo, good code explanation, articulates challenges well |
| 4 | Good video, minor improvements needed |
| 3 | Adequate video, missing some required elements |
| 2 | Poor quality video or missing key components |
| 1 | Video present but unhelpful |
| 0 | No video |

---

## Bonus Points (+20 max)

| Feature | Points | Verification |
|---------|--------|--------------|
| Responsive Design | +5 | Test on mobile viewport in DevTools |
| Dark/Light Mode | +3 | Toggle works, persists preference |
| Sort Functionality | +3 | Sort by at least 2 criteria (name, population) |
| Favorites (localStorage) | +4 | Add/remove favorites, persists on refresh |
| TypeScript | +5 | Proper types, no `any` abuse |
| Unit Tests | +5 | At least 3 meaningful tests pass |
| Live Deployment | +3 | Working deployed URL |

---

## Scoring Sheet Template

```
Candidate: _______________________
Evaluator: _______________________
Date: ___________________________

FUNCTIONALITY (35 points)
├── Country List Display:     ___ / 8
├── Search Functionality:     ___ / 7
├── Region Filter:            ___ / 7
├── Country Detail View:      ___ / 7
└── Loading & Error States:   ___ / 6
                              ________
                     Subtotal: ___ / 35

REACT FUNDAMENTALS (25 points)
├── useState Usage:           ___ / 8
├── useEffect Usage:          ___ / 8
└── Props & Components:       ___ / 9
                              ________
                     Subtotal: ___ / 25

CODE QUALITY (20 points)
├── Code Organization:        ___ / 7
├── Readability:              ___ / 7
└── Best Practices:           ___ / 6
                              ________
                     Subtotal: ___ / 20

UI/UX (10 points)
├── Visual Design:            ___ / 5
└── User Experience:          ___ / 5
                              ________
                     Subtotal: ___ / 10

DOCUMENTATION & VIDEO (10 points)
├── README Quality:           ___ / 5
└── Loom Video:               ___ / 5
                              ________
                     Subtotal: ___ / 10

BASE TOTAL:                   ___ / 100

BONUS POINTS (+20 max)
├── Responsive Design:        ___ / 5
├── Dark/Light Mode:          ___ / 3
├── Sort Functionality:       ___ / 3
├── Favorites (localStorage): ___ / 4
├── TypeScript:               ___ / 5
├── Unit Tests:               ___ / 5
└── Live Deployment:          ___ / 3
                              ________
                Bonus Total:  ___ / 20

═══════════════════════════════════════
FINAL SCORE:                  ___ / 120
═══════════════════════════════════════
```

---

## Scoring Thresholds

| Score Range | Result | Recommendation |
|-------------|--------|----------------|
| 90+ | Excellent | Strong hire recommendation |
| 75-89 | Good | Hire recommendation |
| 60-74 | Satisfactory | Consider with reservations |
| 45-59 | Below Expectations | Additional assessment needed |
| Below 45 | Unsatisfactory | Do not proceed |

---

## Red Flags to Watch For

- [ ] Code clearly copied from tutorial without understanding
- [ ] Unable to explain their own code in video
- [ ] Git history shows single commit (possible code copy)
- [ ] No error handling whatsoever
- [ ] Console full of errors/warnings
- [ ] Video doesn't match submitted code
- [ ] Plagiarism from other candidates

---

## Green Flags (Positive Indicators)

- [ ] Clean commit history showing progression
- [ ] Handles edge cases (empty states, missing data)
- [ ] Creative UI beyond basic requirements
- [ ] Well-articulated problem-solving in video
- [ ] Good questions asked during the test
- [ ] Code comments where genuinely helpful
- [ ] Performance considerations (debouncing search, etc.)

---

## Notes Section

```
Additional observations:
_________________________________________________
_________________________________________________
_________________________________________________
_________________________________________________

Strengths:
_________________________________________________
_________________________________________________

Areas for improvement:
_________________________________________________
_________________________________________________

Final recommendation:
_________________________________________________
_________________________________________________
```
