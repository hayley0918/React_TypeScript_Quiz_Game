# React TypeScript Quiz Game

## Part 1. Set up the project

1. create react app
   npx create-react-app react-quiz --template typescript
   remove the unnecessary files

2. install the dependency
   npm i styled-components @types/styled-components

3. download the image for the app and place the image file in images/src

4. download the font and copy the embed link and place it in index.html/public

5. api ( Trivia API ) to fetch the data

## Part 2. Logic

1. create components folder in src

2. create QuestionCard.tsx in components folder

3. create API.ts and utils.ts in src folder

4. create startTrivia, checkAnswer, nextQuestion functions in App.tsx

5. JSX in App.tsx to display name of the app, start button, loading, QuestionCard, next question button.

6. define type Props in QuestionCard.tsx

- specify the Functional Component using React.FC to pass the Props down
- destructure the properties from props
- JSX to display the data from Props

7. import useState in App.tsx to manage the states

- define the initial states of the props ( loading, questions, number, userAnswers, score, gameOver )
- pass the props to the QuestionCard component

8. API.ts

- create fetchQuizQuestions taking 2 parameters (amount: number, Difficulty)
- create enum Difficulty and specify the constants in it
- define the endpoint in fetchQuizQuestions
- declare the data using fetch(endpoint)
- create type Question to specify the type of the properties
- create type QuestionState to integrate incorrect answers and correct answer
- import shuffleArray

9. App.tsx

- import fetchQuizQuestions and Difficulty
- import QuestionState
- create type AnswerObject

10. utils.ts

- create shuffleArray to shuffle the answers

11. App.tsx

- setting the initial state of the game
- define newQuestions containing the data from API
- JSX

- checkAnswer function

1. get the answer from the user Click answer
2. set the correct from the data
3. compare if the user answer is same with the correct
4. increase the score
5. save answers in the array for user answers

- nextQuestion function

1. move on to the next question if not the last quesiton

## Part 3. Styling

- create App.styles.ts in src folder
- import styled, { createGlobalStyle } from 'styled-components'
- import BGImage from './images/nattu-adnan.jpg'
- create GlobalStyle using createGlobalStyle``
