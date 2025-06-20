# Forge Quest
# Forge Apps Overview

This repository contains two Atlassian Forge apps:

- A simple **Hello World** app built for Confluence  
- A more advanced **Weather Gadget** app built for Jira

---

## Part 1: Hello World App for Confluence

### Overview  
This app demonstrates how to create a basic Forge app that displays a "Hello World" message inside a Confluence page. It is intended as a starting point to get familiar with Forge development, module structure, and deployment.

### How I Built It  
- Created a Forge app with the `confluence:macro` module type.  
- Used `@forge/ui` components to render a simple message.  
- Leveraged the Forge CLI (`forge create`, `forge deploy`, and `forge install`) to build and deploy the app.  
- Used the Confluence UI to insert the macro and verify the message renders correctly.

### Key Steps  
1. Initialize the Forge app with `forge create`.  
2. Edit `manifest.yml` to include the `confluence:macro` module.  
3. Write a React component with `@forge/ui` that returns “Hello World”.  
4. Deploy with `forge deploy` and install it on the target Confluence site.  
5. Test by inserting the macro in a Confluence page.

### What I Learned  
- How Forge apps integrate into Atlassian products via modules.  
- Basics of UI Kit for building simple interfaces.  
- Using Forge CLI for development lifecycle.

---

## Part 2: Weather Gadget for Jira

### Overview  
This app is a Jira dashboard gadget that shows current weather information for a user-specified city and country. It calls an external weather API to fetch live data and displays temperature, humidity, and conditions directly within Jira.

### How I Built It  
- Created a Forge app with the `jira:dashboardGadget` module.  
- Used `@forge/react` UI Kit 2 for building an interactive form and weather display components.  
- Implemented backend functions using Forge’s Node.js runtime to call OpenWeatherMap API based on user input.  
- Managed frontend-backend communication using `@forge/bridge`'s `invoke` method.  
- Deployed and installed the app to a Jira Cloud instance.

### Features  
- User inputs city and country via a form in edit mode.  
- The app uses geocoding to get latitude and longitude.  
- Displays current temperature, feels like temperature, humidity, and weather icon.  
- Handles errors and loading states gracefully.

### What I Learned  
- How to integrate third-party APIs securely in Forge.  
- The differences between UI Kit classic and UI Kit 2 (`@forge/react`).  
- Challenges with new frameworks and debugging unfamiliar code.  
- The Forge app lifecycle: registering, deploying, updating, and managing permissions.

---

## How to Run These Apps

1. Clone this repository.  
2. Install Forge CLI: [https://developer.atlassian.com/platform/forge/getting-started/](https://developer.atlassian.com/platform/forge/getting-started/)  
3. Log in to your Atlassian account:  
   ```bash
   forge login
