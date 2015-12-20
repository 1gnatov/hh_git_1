создал репозиторий на гитхабе hh_git1_repoA
'''
git clone git@github.com:1gnatov/hh_git1_repoA.git
gedit fileA.txt
gedit stufffff.py
git add fileA.txt  stufffff.py 
git commit -m "1st commit with files: fileA stufffff"
git checkout -b "branch1"
git push origin 
cd ..

git clone https://github.com/1gnatov/hh_git1_repoA hh_git1_repoB
cd hh_git1_repoB/

git branch -a
git checkout -b branch1 origin/branch1 
gedit newest_file.log
git add newest_file.log
git commit -m "2nd commit in repoB with file newest_file"
git push origin
cd ../hh_git1_repoA/

git pull
gedit newest_file.log
git add newest_file.log
git commit -m "some modifications fileC from repoB/branch1"
git push origin
cd ../hh_git1_repoB/

git fetch origin 
git merge origin/branch1 
git add newest_file.log 
git commit -m "repoB merged origin/branch1 from repoA"
'''
создал репозиторий на гитхабе hh_git1_repoB
'''
git remote add artificalorigin git@github.com:1gnatov/hh_git1_repoB.git
git push --all artificalorigin 
cd ../hh_git1_repoA/

git remote add repoB https://github.com/1gnatov/hh_git1_repoB
git fetch repoB
git merge repoB/branch1 
git commit -m "merged repoB/branch1 with resolved conflict"
git push --all
'''
