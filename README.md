# create-chatgpt-app-react-node-tailwind

# How to create Tailwind CSS React Forms.

Table of Content
Prerequisites
What is TailwindCSS
Creating our React Project
Installing TailwindCSS
Creating Tailwind CSS form in our App.js
Conclusion
Resources
Prerequisities
To make the most of this article, you must have the following:

A basic understanding of HTML.
A basic understanding of CSS.
A basic understanding of React.
Node and its package manager, npm, Run the command node -v && npm -v to verify we have them installed, or install them from here.
Alternatively, we can use another package manager, Yarn.
What is Tailwind CSS
Tailwind CSS, according to the documentation on their website, tailwind CSS is a utility-first CSS framework. Tailwind CSS helps developers bring designs to life, it is fast and easy to use, with its custom class names that gift our application with ready-to-use styles.

Creating our React project
To create a new react project, we go to our terminal, cd in the directory we want, and then run this command npx create-react-app project-name.

cd Documents
npx create-react-app project-name
Installing Tailwind CSS
To have tailwind CSS available in your project, cd into the project you created earlier

cd project-name
next run

npm install -D tailwindcss postcss autoprefixer
This helps to install the tailwind CSS and its peer dependencies, we then generate our tailwind.config.js and postcss.config.js files by running this command:

npx tailwindcss init -p
Configuring your templates path

To configure your paths go to your tailwind.config.js, and edit your module.exports object, add the paths to your template files in your content array.

JS
module.exports = {
  content: ['./src/**/*.{js,jsx,ts,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
Next add the Tailwind directives to your CSS

Add the tailwind directives in your ./src/index.css file.

CSS
@tailwind base;
@tailwind components;
@tailwind utilities;
After this, we run our project

npm run start
You should see the image below on your browser when you go to http://localhost:3000/.
