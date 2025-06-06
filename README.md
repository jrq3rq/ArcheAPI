```markdown
ArcheAPI/
├── src/
│   ├── config/
│   │   ├── firebaseConfig.js       # Firebase Admin SDK setup
│   │   └── winston.js             # Logger configuration
│   ├── controllers/
│   │   └── archetypeController.js # Handles archetype endpoints
│   ├── data/
│   │   ├── archetypes.json        # Static archetype data
│   │   └── educational/           # Curated datasets for paid academic use
│   │       ├── psychology.json
│   │       └── storytelling.json
│   ├── middleware/
│   │   ├── rateLimit.js           # Tiered rate limiting
│   │   ├── auth.js                # Firebase Authentication
│   │   ├── apiKey.js              # API key validation
│   │   └── validation.js          # Input validation
│   ├── models/
│   │   └── archetypeModel.js      # Archetype data schema and methods
│   ├── routes/
│   │   ├── archetypes.js          # Archetype endpoints (free/premium)
│   │   └── educational.js         # Educational dataset endpoints
│   ├── utils/
│   │   └── helpers.js             # Reusable utilities
│   ├── functions/
│   │   └── subscription.js        # Stripe payment functions
│   └── app.js                     # Express app setup
├── public/
│   ├── frontend/                  # User onboarding (signup, subscriptions)
│   │   └── index.html
│   ├── swagger-ui/                # Swagger UI static files
│   ├── docs/
│   │   ├── swagger.yaml           # API documentation
│   │   └── user-guide.md          # Guide for non-technical users
│   └── educational/
│       └── LICENSE-CC-BY-SA-4.0.txt # License for educational datasets
├── scripts/
│   └── generateDatasets.py        # Script to create educational datasets
├── tests/
│   ├── archetypes.test.js         # Unit tests for archetype endpoints
│   ├── educational.test.js        # Unit tests for educational endpoints
│   └── middleware.test.js         # Unit tests for middleware
├── .gitignore                     # Ignore node_modules, .env
├── firebase.json                  # Firebase configuration
├── .firebaserc                    # Firebase project settings
├── package.json                   # Dependencies and scripts
├── LICENSE.md                     # Proprietary license for API
├── README.md                      # Project overview
└── .env                           # Environment variables
```
# ArcheAPI

## Project/Product Overview
- **Name of Project/Product**: ArcheAPI
- **Brief Description**: A powerful API for character development in storytelling, gaming, and psychological analysis, leveraging Carl Jung’s archetypal theory to create rich, archetypal characters like the Rebel, Hero, and Sage.
- **Target Market**: Writers crafting narratives, game developers designing immersive characters, psychologists exploring behavioral patterns, educators teaching Jungian theory, and enthusiasts of psychology and storytelling.
- **Key Objectives**:
  - Provide a scalable platform to access and customize Jungian archetypes for creating dynamic characters and analyzing human behaviors.
  - Offer tiered access (free and paid) to support diverse users, from hobbyists to professionals.
  - Enable educational use with curated datasets for academic settings.

### Key Features for Users
- **Free Tier**: Access basic archetype data (e.g., name, motto, traits) at `/archetypes/basic` with a 100 requests/day limit.
- **Premium Tiers**:
  - Basic ($5/month): Full archetype data (e.g., scores, historical examples) at `/archetypes/advanced`, 5,000 requests/day.
  - Pro ($15/month): Create custom archetypes at `/archetypes/custom`, 10,000 requests/day.
- **API Licensing**:
  - Basic ($100/month): 50,000 requests/month, bulk data access at `/archetypes/batch`.
  - Pro ($500/month): 1,000,000 requests/month, custom archetype support.
- **Educational Packages**:
  - Single Course ($50): Access curated datasets (e.g., psychology-focused archetypes) at `/educational/datasets`.
  - Department ($200): Multiple datasets for broader academic use.
- **Documentation**:
  - Developer-friendly Swagger UI at `/swagger-ui`.
  - Non-technical user guide at `/docs/user-guide` for writers and educators.
- **Onboarding**: Sign up and manage subscriptions via a user-friendly frontend at `/frontend`.

### Why Use ArcheAPI?
- Create compelling characters for stories or games using archetypes like the Rebel or Hero.
- Explore psychological insights through Jungian theory for education or analysis.
- Scale effortlessly with Firebase-backed infrastructure for global access.
- Start free, upgrade as needed, and integrate easily with clear documentation.