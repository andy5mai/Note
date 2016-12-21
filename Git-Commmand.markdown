# 查看 branch   
git branch -a
    
# 把版本拉下來    
git pull

# checkout 並轉換到該 branch
git checkout [查看 branch 時顯示的路徑]    
如：git checkout remotes/origin/master

# discard all local changes/commits and pull from upstream
git reset --hard origin/master    
git pull origin master

# 恢復檔案
git checkout [檔案路徑]    
如：git checkout stages/api/post/mail.php

# 查看 remote 路徑
git remote show {branch}
如：git remote show origin