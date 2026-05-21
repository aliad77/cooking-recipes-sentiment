# 🍳 Cooking Recipes Rating Based on Sentiment Analysis


A web-based recipe platform that uses Natural Language Processing (NLP) and sentiment analysis to evaluate user comments and generate reliable, sentiment-based recipe ratings. The system improves trust in recipe reviews by detecting fake reviews, translating multilingual comments, and flagging harmful content.

**Key Features:**
- Sentiment analysis of user comments
- Fake review detection (ERF model)
- Multilingual support
- Ingredient safety detection
- Admin moderation dashboard
---

## Team Members

| Name | Student ID |
|---|---|
| Hala Mohammad | 202220383 |
| Alia Dallal | 202310432 |
| Shahed Mousa | 202311068 |
| Noor Elhilo | 202310724 |

---

## System Architecture

The system consists of four main layers:

- **Frontend** — Web interface for users and admins (desktop Windows browsers)
- **Backend** — .NET services handling business logic and API requests
- **NLP Module** — Python-based sentiment analysis and fake review detection engine
- **Database** — SQL Server storing users, recipes, comments, and ratings

---

## How It Works

1. User submits a comment on a recipe
2. NLP module analyzes the comment and classifies sentiment
3. Fake review detection model (ERF) evaluates authenticity
4. System updates the recipe's sentiment-based rating
5. Admin dashboard displays insights and flagged content

---

## Project Structure

```
cooking-recipes-sentiment/
│
├── docs/                   # Project documentation
│   ├── proposal.pdf        # Phase 1 - Project Proposal
│   ├── phase2.docx         # Phase 2 - User Stories, Use Cases & Functional Specs
│   └── requirements.md     # Full functional requirements (FR1–FR12)
│
├── src/                    # Source code
│   ├── backend/            # .NET backend & SQL database logic
│   ├── frontend/           # Web UI for users and admins
│   └── nlp/                # Sentiment analysis & ERF modules (Python)
│
├── tests/                  # Unit, integration, and system tests
│
├── .gitignore
└── README.md
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | .NET Framework |
| Database | Microsoft SQL Server 2008 |
| Frontend | Web UI (Desktop, Windows browsers) |
| NLP | NLTK, TextBlob (Python) |
| Fake Review Detection | Enhanced Random Forest (ERF) |
| Translation | Google Translate API |
| IDE | Visual Studio 2010 |

---

##  Getting Started

### Prerequisites

- Windows OS (desktop browser required)
- Visual Studio 2010
- Microsoft SQL Server 2008
- Python (for NLP modules)
- Internet connection (for Google Translate API)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/cooking-recipes-sentiment.git
   cd cooking-recipes-sentiment
   ```

2. **Set up the database**
   - Open SQL Server 2008
   - Run the schema script at `src/backend/db/schema.sql`

3. **Configure the backend**
   - Open the solution in Visual Studio 2010
   - Update the connection string in `Web.config` to match your SQL Server instance

4. **Install Python dependencies**
   ```bash
   pip install nltk textblob
   ```

5. **Run the application**
   - Press `F5` in Visual Studio or host via IIS
   - Open `http://localhost:[port]` in your desktop browser

---

## User Roles

**Regular User:**
- Register, login, and manage profile
- Submit recipes and comments
- View sentiment-based ratings
- Search and filter recipes
- Report inappropriate content

**Administrator:**
- Manage users and content
- Moderate flagged comments
- Monitor fake reviews and system analytics

---


## External Integrations

- **Google Translate API** — processes non-English comments for multilingual support
- **Python NLP Module** — integrated with the .NET backend for sentiment scoring

---

## Testing

Tests are located in the `tests/` directory:

```bash
# Run NLP module tests
python -m pytest tests/nlp/
```

System testing is conducted manually through the web interface covering unit, integration, and end-to-end scenarios.

---

## Constraints

- Mobile devices are not supported (desktop Windows only)
- Internet connection required for the translation API
- Sentiment accuracy depends on the quality of user input

---

## License

This project is developed for academic purposes as part of a software documentation course.
