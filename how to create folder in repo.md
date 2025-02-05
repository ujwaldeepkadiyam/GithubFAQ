
## Answer  
You **cannot** create an empty folder and then add files to it later. Git does not track empty folders. Instead, a folder is created when you add at least one file inside it.

### Steps to Create a Folder on GitHub:
1. Navigate to the folder where you want to create a subfolder.
2. Click on **"Add file"** → **"Create new file"**.
3. In the file name field, type the folder name followed by a `/` (e.g., `my-folder/`).
4. Type the file name (e.g., `.gitkeep`).  
   - **Note:** `.gitkeep` is a common convention used to make Git track otherwise empty folders. It is not an official Git feature.
5. Add any content (optional).
6. Click **"Commit new file"**.

Now, the new folder will be visible in the repository. 🚀

[Source:](https://stackoverflow.com/questions/12258399/how-do-i-create-a-folder-in-a-github-repository)
