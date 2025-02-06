# set up github repo from established direcotry

### can use github command line tool (cli)
```
conda install gh --channel conda-forge
gh auth login   
git init
~/Projects/my-project$ gh repo create myNewRepo --private --source=.

echo "# mamp_prediction_ml" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/DanielleMStevens/mamp_prediction_ml.git
git push -u origin main
```
