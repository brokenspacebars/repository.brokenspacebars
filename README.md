# repository.brokenspacebars
Kodi repository for BrokenSpacebars addons

# Install repository
- Add source
```
 https://brokenspacebars.github.io/repository.brokenspacebars/repo/ 
```
- Install the repository from the zip file

# Add a new addon to repository
- Upload addon to a git repository and then add it as submodule
``` bash
git submodule add <git-repo>
```
- Run the script
```
python _repo_xml_generator.py
```

# Update an addon
- Change to the submodule/addon directory and checkout to ```master```
```
git checkout master
```
- Update it
```
git pull
```
- Go back to root folder, ```cd ..```
- Run the script
```
python _repo_xml_generator.py
```
- Commit the changes, and push them
```
git commit -am "Update <addon> to <version>"
git push origin master
```
Alternatively you can update all submodules at once using,
```
git submodule foreach git pull origin master
```
And then run-script/commit/push