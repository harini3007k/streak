# 🔥 StreakForce

### Build Consistency. Track Progress. Achieve More.

StreakForce is an intelligent cross-platform consistency and progress tracking system designed to help individuals build productive habits, monitor coding activities, manage personal goals, and measure their consistency over time.

It combines productivity tracking, data analytics, and machine learning to provide meaningful insights into user activities and progress.

## 📌 Overview

Maintaining consistency across coding platforms, learning activities, and personal goals can be challenging.

StreakForce brings these activities together in one platform, allowing users to track their progress, analyze productivity patterns, and understand their consistency through explainable scoring and machine learning-based classification.

## ✨ Key Features

- **Unified Dashboard:** Monitor activities, streaks, goals, and progress in one place.
- **Coding Platform Tracking:** Track activities from LeetCode, CodeChef, Codeforces, and AtCoder.
- **Custom Activities:** Create recurring activities and maintain completion history.
- **Goal Management:** Set measurable goals, deadlines, priorities, and track progress.
- **Project Management:** Organize projects, tasks, deadlines, and completion history.
- **Consistency Analysis:** Calculate weighted consistency scores based on user activity.
- **Machine Learning Classification:** Classify consistency patterns into five meaningful categories.
- **AI Coach:** Get explanations and recommendations based on stored activity and progress data.
- **Interactive Analytics:** Understand activity trends and historical progress.
- **Secure Authentication:** User registration, login, session management, and account recovery.

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js, Express.js |
| Database | SQLite, PostgreSQL |
| SQLite Driver | better-sqlite3 |
| PostgreSQL Driver | pg |
| Machine Learning | K-Means Clustering |
| Testing | Node.js Test Runner |
| Version Control | Git, GitHub |

## 🧠 Machine Learning Implementation

StreakForce incorporates an explainable consistency analysis system.

### 1. Consistency Score

A weighted scoring mechanism calculates a score between 0 and 100 using four factors:

| Factor | Weight |
|---|---:|
| Recent Activity | 35% |
| Scheduled Session Completion | 25% |
| Activity Rhythm | 20% |
| Goal Progress | 20% |

The system evaluates historical activity data and provides component-level explanations for the calculated score.

### 2. K-Means Clustering

The consistency classification system uses deterministic K-Means clustering with three clusters.

It performs feature engineering using eight rolling weekly observations and considers:

- Active-day rate
- Planned-session completion rate
- Longest streak density
- Activity-source diversity

The current week's feature vector is assigned to its nearest cluster.

### 3. Consistency Classification

The system maps clustering results and recent activity patterns into five categories:

| Classification | Description |
|---|---|
| Highly Consistent | Strong and stable activity patterns |
| Consistent | Positive consistency patterns |
| Irregular | Unstable activity patterns |
| At Risk | Declining activity patterns |
| Inactive | Very low recent activity |

### 4. Cold-Start Handling

To avoid unreliable classifications for new users, the system waits until sufficient historical activity is available:

- At least 4 active historical weeks
- At least 14 logged days

This makes the classification more meaningful and transparent.

## 🏗️ Project Structure

```text
StreakForce/
│
├── assets/                     # Images and other assets
├── css/                        # Stylesheets
├── js/                         # Frontend JavaScript
├── lib/                        # Application logic and ML
├── reports/                    # Project reports
├── scripts/                    # Utility and migration scripts
├── streak/                     # Project resources
├── tests/                      # Automated tests
│
├── index.html                  # Main application interface
├── server.js                   # Main application server
├── server-postgres.js          # PostgreSQL server
├── server-sqlite-backup.js     # SQLite backup server
├── postgres-schema.sql         # PostgreSQL database schema
├── PROJECT_GUIDE.md            # Technical documentation
├── package.json                # Dependencies and scripts
└── .gitignore                  # Git ignore configuration
```

## 🚀 Getting Started

### Prerequisites

- Node.js
- npm
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/h27031705-netizen/streak.git
```

### 2. Navigate to the Project

```bash
cd streak
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Start the Application

```bash
npm start
```

### 5. Open in Browser

```text
http://localhost:3000
```

The default start command runs `server.js`.

## 🗄️ Database

StreakForce supports:

- SQLite using `better-sqlite3`
- PostgreSQL using `pg`

The project includes database schemas and migration-related scripts to support its database architecture.

Refer to `PROJECT_GUIDE.md` for additional implementation details.

## 🧪 Testing

StreakForce includes automated tests for important application functionality.

Run the test suite using:

```bash
npm test
```

The tests cover:

- Database migration preservation
- Consistency score calculations
- K-Means clustering determinism
- Cold-start handling
- Streak calculations
- Authentication and session handling
- Activity, project, and goal management
- Unified activity history
- User profile isolation

## 🔐 Security

Security-related implementations include:

- Server-side session management
- HTTP-only session cookies
- Per-user salted scrypt password hashing
- Authenticated API operations
- Profile-scoped data access

Sensitive configuration values and credentials should be stored in environment variables and must not be committed to the repository.

## 🔮 Future Enhancements

- Expanded coding platform integrations
- More advanced personalized analytics
- Improved consistency recommendations
- Enhanced dashboard visualizations
- Additional productivity insights
- Further improvements to the machine learning classification system

## 📖 Documentation

For detailed technical information about the architecture, database design, consistency scoring, machine learning implementation, and integration limitations, refer to:

**[PROJECT_GUIDE.md](PROJECT_GUIDE.md)**

## 👩‍💻 Author

**Harini**

B.E. Artificial Intelligence and Machine Learning

GitHub: [@harini3007k](https://github.com/harini3007k)

---

⭐ If you find StreakForce interesting, consider exploring the repository and its implementation.

**StreakForce – Consistency is built, not discovered.**
