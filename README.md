# happy_new_year_puzzle
A puzzle game to send New Year's greetings

Type in `https://bflyer.github.io/happy_new_year_puzzle/puzzle.html` in your browser to play the game.

**How to play?**
- **直接开始**：If you choose this button, you will be redirected to the game page directly, and get my surprise after finishing the puzzle and the new button is pressed.  
- **上传图片**：If you choose this button, you can upload your own image to replace the default one. Also, you will get a surprise after finishing the puzzle and the new button is pressed.  

## Local Development Guide
1. Clone the repository by 
   ```
   git clone git@github.com:bflyer/happy_new_year_puzzle.git
   ```

2. Enter the directory of the project, and run the below command in the terminal to start the game
   ```
   python -m http.server 8000
   ```

3. Open the browser and go to `http://localhost:8000/puzzle.html` to play the game. If it doesn't work, try to open the file directly in Google Chrome.

4. If you want to replace the puzzle image, you can replace the img.src in puzzle.html and textImg.src in happy_new_year.html with your own puzzle image file.

5. IF you want to replace the greeting image, you can replace the img.src in happy_new_year.html with your own greeting image file.

6. Enjoy the game!

## Hosting a static website on GitHub
1. **Create a GitHub Repository**
- Log in to your GitHub account.  
- Click the "+" icon in the upper right corner and select "New repository" to create a new repository.  
- Fill in the repository name (e.g., my-static-site) and choose whether it should be public or private (public repositories can use GitHub Pages for free).  
- Optionally, you can initialize the repository with a README.md file, but it is not required.

2. **Prepare Your Static Webpage Files**
- A static webpage typically consists of HTML, CSS, and JavaScript files, and may also include images, fonts, and other resources.
- Organize your static website project files, usually with an index.html file as the main entry point.
- For example, your project directory structure might look like this:
```
my-static-site/
├── index.html
├── styles.css
├── script.js
├── images/
│   └── logo.png
└── ...
```
3. **Upload Your Project to the GitHub Repository**
- You can upload your local project to the GitHub repository in several ways:
Method 1: Using GitHub Desktop (Graphical Interface)
- Install and open GitHub Desktop.
- Link your local project folder to the newly created GitHub repository.
- Commit the changes and push them to the remote repository.

Method 2: Using the Command Line (Git Operations)
- Open the terminal or command prompt and navigate to your project directory.
- Initialize the Git repository (if you haven't already):
```bash
git init
```
- Add your project files to the Git repository:
```bash
git add .
```
- Commit the changes:
```bash
git commit -m "Initial commit"
```
- Link your local repository to the GitHub remote repository (replace <your-repo-url> with your GitHub repository URL):
```bash
git remote add origin <your-repo-url>
```
- Push the code to GitHub:
```git push -u origin main```
4. **Configure GitHub Pages**
- Go to your GitHub repository page and click on "Settings" at the top.
- In the left sidebar, find the "Pages" tab.
- In the "Source" section, select the branch (usually main or master) and folder path (default is the repository root /).
- Click the "Save" button.  
If everything is set up correctly, GitHub Pages will automatically deploy your static website.

5. **Access Your Static Website**
- After deployment, GitHub Pages will generate a default URL, usually in the following format:
`https://<your-username>.github.io/<your-repo-name>`
- If your repository name matches your username (e.g., <your-username>.github.io), you can access it directly via:
`https://<your-username>.github.io`

6. **Custom Domain (Optional)**
- If you want to use a custom domain (e.g., www.yourdomain.com), you can:
- In the "Settings" > "Pages" section of your GitHub repository, find the "Custom domain" part.
- Enter your custom domain and save it.
- In your domain registrar, set up DNS records to point to GitHub Pages' server IP addresses (GitHub will provide specific DNS information).

7. **Notes**
- GitHub Pages supports static resources such as HTML, CSS, and JavaScript, but does not support backend languages like PHP or Python.
- If your project uses Jekyll (a static site generator), GitHub Pages will automatically support it.
- If your project uses other static site generators (such as Hugo, VuePress, etc.), you need to generate the static files locally first and then upload them to the GitHub repository.

By following these steps, you can easily host a static website on GitHub!

## Embed resources into html by base64 encoding
You can also embed resources into html by base64 encoding them, and merge the two html files into one. Just replace the path of your resources with the base64 encoded content. 

An example is template.html.

