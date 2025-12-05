# Deployment Instructions

## GitHub Pages Deployment

This Logic Playground application is ready to be deployed to GitHub Pages.

### Steps to Deploy:

1. Go to your repository on GitHub: `https://github.com/aacurtis/logic-playground`

2. Navigate to **Settings** → **Pages**

3. Under "Source", select the branch you want to deploy (e.g., `main` or `copilot/build-propositional-logic-app`)

4. Select the root directory `/` as the source folder

5. Click **Save**

6. GitHub will automatically build and deploy your site

7. Your application will be available at: `https://aacurtis.github.io/logic-playground/`

### Testing Locally

To test the application locally before deploying:

```bash
# Navigate to the repository directory
cd logic-playground

# Start a simple HTTP server
python3 -m http.server 8080

# Open your browser to: http://localhost:8080/
```

### Application Features

- No build process required - it's a single self-contained HTML file
- Works in all modern browsers
- No server-side processing needed
- Mobile-friendly responsive design

### Browser Compatibility

The application uses standard HTML5, CSS3, and ES6 JavaScript features:
- Arrow functions
- Template literals
- Array methods (map, filter, every)
- Regular expressions
- CSS Grid and Flexbox

Tested and works on:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

### Usage

Students can:
1. Click variable buttons (P, Q, R, S) to add variables
2. Click operator buttons (∧, ∨, ¬, →, ↔) to add logical operators
3. Use parentheses for complex expressions
4. Click "Evaluate" to generate truth tables
5. See if their formula is a tautology, contradiction, or contingency
6. Try random challenges to practice

### Support

For issues or questions, please create an issue in the GitHub repository.
