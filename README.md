<a name="readme-top"></a>

<!--
!!! IMPORTANT !!!
This README is an example of how you could professionally present your codebase. 
Writing documentation is a crucial part of your work as a professional software developer and cannot be ignored. 

You should modify this file to match your project and remove sections that don't apply.

REQUIRED SECTIONS:
- Table of Contents
- About the Project
  - Built With
  - Live Demo
- Getting Started
- Authors
- Future Features
- Contributing
- Show your support
- Acknowledgements
- License

OPTIONAL SECTIONS:
- FAQ

After you're finished please remove all the comments and instructions!

For more information on the importance of a professional README for your repositories: https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/readme_best_practices.md
-->

  <h1 align = "center"><b>WebPack Configurations</b></h1>

</div>


### Pre-requisites

Configure <a href="https://github.com/MasumaJaffery/linters-config/tree/master/html-css-js">Linters</a>
 in main Branch.
 
### Step 1 (Files):
Create Three Files inside src folder that must be inside repo folder;
<ol>
<li>index.html</li>
<li>style.css</li>
<li>index.js</li>
</ol>

### Step 2 (Create WebPack File)
Create an webpack.config.js file inside repo folder.
```sh
 const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  mode: 'development',
  entry: {
    index: './src/index.js',
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './src/index.html',
    }),
  ],
  output: {
    filename: '[name].bundle.js',
    path: path.resolve(__dirname, 'dist'),
    clean: true,
  },
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: ['style-loader', 'css-loader'],
      },
    ],
  },
};
```

### Step 3 (Install WebPack):

```sh
 npm install webpack webpack-cli --save-dev
```

### Step 4 (Install style-loader and css-loader):

```sh
npm install --save-dev style-loader css-loader
```

### Step 5 (Install HtmlWebpackPlugin plugin):

```sh
npm install --save-dev html-webpack-plugin
```

### Step 6 (Install Webpack-dev-server):

```sh
npm install --save-dev webpack-dev-server
```

### Step 8 (Make Changes in package.json file):
Update scripts part of package.json with these lines!
```sh
"test": "echo \"Error: no test specified\" && exit 1",
"start": "webpack serve --open",
"build": "webpack"
```
### Step 9 (Run Following Command to Generate .dist/ folder):
```sh
npm run build
```
### Step 10 (Run Following Command to Run Project by WebPack Server):
```sh
npm start
```
### Setup
Clone this repository to your desired folder:
<!--
Example commands:

```sh
  cd my-folder
  git clone git@github.com:MasumaJaffery/WebPack.git
```
--->

<!-- AUTHORS -->

## 👥 Authors <a name="authors"></a>

👤 **Noel FOKA**

- GitHub: [@noelfoka](https://github.com/noelfoka)
- Twitter: [@MasumaJaffery](https://twitter.com/noelnomgne)
- LinkedIn: [Masuma Jaffery](https://www.linkedin.com/in/no%C3%ABl-nomgne-foka-063013231/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGEMENTS -->

## 🙏 Acknowledgments <a name="acknowledgements"></a>

I would like to thank Microverse!

<!-- LICENSE -->

## 📝 License <a name="license"></a>

This project is [MIT](./LICENSE) licensed.

<p align="right">(<a href="#readme-top">back to top</a>)</p>