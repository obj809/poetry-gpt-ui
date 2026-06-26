# PoetryGPT - Poetic ChatGPT Interface


## Project Overview
An interactive chatbot that provides poetic responses using a finely-tuned ChatGPT model. This repository is the React + TypeScript frontend, built with Vite and styled with SCSS. It communicates with a separate backend service (the partner project below) that serves the fine-tuned model.


## Deployment Link
[https://poetry-gpt.netlify.app/](https://poetry-gpt.netlify.app/)

## Partner Project

[https://github.com/cyberforge1/chat-gpt-fine-tuning](https://github.com/cyberforge1/chat-gpt-fine-tuning)

## Screenshot
![Application Screenshot](public/app-screenshot.png "Project Screenshot")


## Table of Contents
- [Goals & MVP](#goals--MVP)
- [Tech Stack](#tech-stack)
- [Build Steps](#build-steps)
- [Design Goals](#design-goals)
- [Project Features](#project-features)
- [Additions & Improvements](#additions--improvements)
- [Learning Highlights](#learning-highlights)
- [Known Issues](#known-issues)
- [Challenges](#challenges)


## Goals & MVP
The aim was to create a Typescript React frontend application that would imitate the current ChatGPT interface, and make requests to a backend service that wraps an OpenAI chat model (configurable via the backend's `OPENAI_MODEL`, defaulting to `gpt-5.4-nano`) prompted to respond with poems.

## Tech Stack
- React 18
- TypeScript
- Vite
- SCSS (Sass)
- Axios
- Font Awesome
- Git

## Build Steps
1. Install dependencies:
   ```bash
   npm install
   ```
2. Point the app at the backend service by setting `VITE_API_BASE_URL` (defaults to `http://localhost:3001` if unset). For example, create a `.env` file:
   ```bash
   VITE_API_BASE_URL=http://localhost:3001
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```
4. Create a production build (type-checks, then bundles to `dist/`):
   ```bash
   npm run build
   ```
5. Preview the production build locally:
   ```bash
   npm run preview
   ```

The frontend sends each prompt as a `POST` to `${VITE_API_BASE_URL}/generate` and renders the returned text.

## How To Use
1. Type a prompt into the input bar and click the submit button to receive a poetic response from the chatbot.
2. Clear the chat history by clicking the new chat button in the top left hand corner of the screen.


## Design Goals
- The goal for this user interface was to have it resemble the current version of the ChatGPT web application but make aesthetic choices that would make it immediately distinguishable as a different application. This was achieved by creating a white interface and using a playful pastel color palette to distinguish specific features.


## Project Features
- [x] Custom imitation of the ChatGPT user interface
- [x] Prompting an OpenAI chat model to return poetic responses
- [x] Animation of API response to closely resemble user experience
- [x] Ability to clear the chat on 'New Chat' button click


## Additions & Improvements
- [ ] Addition of a dropdown menu that allows selection of various ChatGPT models
- [ ] Adding a 'Chat History' section on the left side of the interface
- [ ] Creating a set of pre-written prompts for the user to select
- [ ] Allowing the user to cancel the animated response at any time


## Learning Highlights
- Learning how to animate API responses to enhance user experience 
- Building an interface to directly resemble an existing application
- Selecting TypeScript to build with React for the first time

## Known Issues
- Issues with clashing data in the animation function when another request is submitted before the initial request has completed.


## Challenges

An interesting challenge encountered during this project involved suspected grammatical errors in the response from the API. Subsequent phrases were attached directly to previous phrases and with capitalized letters. 

After mistakenly trying to correct the grammar of the responses, I looked back at the training data, and realized that limericks are structured this way. 

Therefore, to correct this issue, all that was necessary was to break the response onto a new line when the phrase delimiter was encountered.  


## Contact Me
- Visit my [LinkedIn](https://www.linkedin.com/in/obj809/) for more details.
- Check out my [GitHub](https://github.com/cyberforge1) for more projects.
- Or send me an email at obj809@gmail.com
<br />
Thanks for your interest in this project. Feel free to reach out with any thoughts or questions.
<br />
<br />
Oliver Jenkins © 2024
