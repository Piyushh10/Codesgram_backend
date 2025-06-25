# 🚀 Codesgram LeetCode Backend API

A powerful, easy-to-use backend service that provides rich LeetCode data for user profiles, problems, contests, and discussions. Perfect for integrating into your apps, dashboards, or analytics tools!

---

## ✨ Features

- **User Profile Data:**  
  Fetch detailed LeetCode user profiles, badges, solved questions, contest history, language stats, skill stats, and more.

- **Problem Data:**  
  Retrieve daily problems, selected problems, problem lists (with filters for tags, difficulty, and limits), and official solutions.

- **Contest Data:**  
  Get user contest rankings and performance data.

- **Discussion Data:**  
  Access trending discussions, specific topics, and comments.

- **Fast & Reliable:**  
  Built with Express.js, leverages caching for performance, and designed for easy deployment (Vercel-ready).

---

## 🛣️ API Endpoints Overview

### User Details
| Endpoint | Description |
|----------|-------------|
| `/userProfile/:username` | Get full user profile details |
| `/:username/badges` | Get user badges |
| `/:username/solved` | Get total solved questions |
| `/:username/contest` | Get contest details |
| `/:username/contest/history` | Get all contest history |
| `/:username/submission` | Get last 20 submissions |
| `/:username/acSubmission` | Get last 20 accepted submissions |
| `/:username/calendar` | Get submission calendar |
| `/userProfileCalendar?username=yourname&year=2024` | Get calendar details for a year |
| `/languageStats?username=yourname` | Get language stats |
| `/userProfileUserQuestionProgressV2/:userSlug` | Get question progress |
| `/skillStats/:username` | Get skill stats |

### Problem Data
| Endpoint | Description |
|----------|-------------|
| `/select?titleSlug=two-sum` | Get selected problem |
| `/daily` | Get daily problem |
| `/dailyQuestion` | Get raw daily question |
| `/problems` | Get list of 20 problems |
| `/problems?limit=50` | Get list of problems (limit) |
| `/problems?tags=array+math` | Get problems by tags |
| `/problems?tags=array+math+string&limit=5` | Get problems by tags and limit |
| `/officialSolution?titleSlug=two-sum` | Get official solution for a problem |

### Contest Data
| Endpoint | Description |
|----------|-------------|
| `/userContestRankingInfo/:username` | Get user contest ranking info |

### Discussion Data
| Endpoint | Description |
|----------|-------------|
| `/trendingDiscuss?first=20` | Get top 20 trending discussions |
| `/discussTopic/:topicId` | Get discussion topic |
| `/discussComments/:topicId` | Get discussion comments |

---

## 🚦 Quick Start

1. **Clone the repo:**
   ```bash
   git clone https://github.com/Piyushh10/Codesgram_backend.git
   cd Codesgram_backend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run locally:**
   ```bash
   npm run dev
   ```
   The server will start at `http://localhost:3000` (or your configured port).

4. **Deploy on Vercel:**  
   - Import the repo on [Vercel](https://vercel.com/)
   - Set up as a Node.js backend (see `vercel.json`)
   - Deploy and get your public API URL!

---

## 📦 Example Usage

**Get user profile:**
```http
GET /userProfile/your-username
```

**Get daily problem:**
```http
GET /daily
```

**Get problems by tag:**
```http
GET /problems?tags=array+math&limit=10
```

---

## 🛡️ License

This project is licensed for personal and educational use.  
For commercial use or custom licensing, please contact the author.

---

## 🙋‍♂️ Author

- **Piyush Shivnani**
- [GitHub](https://github.com/Piyushh10)

---

> **Star** this repo if you find it useful!  
> Pull requests and suggestions are welcome. 