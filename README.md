# Web Quiz Engine

Study project from JetBrain Hyperskill for [Java Backend Developer Track](https://hyperskill.org/tracks/12).

## API [/api](http://localhost:8889/api)

#### POST [/register](http://localhost:8889/api/register)
Register a new user

Consumes a JSON:
```javascript
{
  "email": "your@email.com", // Must have a valid format (with @ and .)
  "password": "secret" // Must have at least five characters
}
```

#### GET [/quiz](http://localhost:8889/api/quiz)
Get a sample quiz

#### POST [/quiz](http://localhost:8889/api/quiz)
Answer the simple quiz

#### POST [/quizzes](http://localhost:8889/api/quizzes)
Post your own quiz

Consumes a JSON:
```javascript
{
  "title": "TITLE HERE", // Must not be empty
  "text": "TEXT HERE", // Must not be empty
  "options": ["OPTION1", "OPTION2"], // Must not be null, must have at least 2 options
  "answer": [0,1]
}
```

#### GET [/quizzes](http://localhost:8889/api/quizzes)
Get all the added quizzes

#### GET [/quizzes/{id}](http://localhost:8889/api/quizzes/{id})
Get quiz by id specified by the path variable

#### POST [/quizzes/{id}/solve](http://localhost:8889/api/quizzes/{id}/solve)
Solve quiz by id specified by the path variable

Consumes a JSON:
```javascript
{
  "answer": [0,1]
}
```

#### DELETE [/quizzes/{id}](http://localhost:8889/api/quizzes/{id})
Delete your quiz by id specified by the path variable

### By Eugene Trigubov
