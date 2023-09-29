create a new repository on the command line
```shell
echo "# craft" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin "https://github.com/username/repository.git"
git push -u origin main
```
push an existing repository from the command line
```shell
git remote add origin https://github.com/changedragon2/craft.git
git branch -M main
git push -u origin main
```