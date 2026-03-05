# 网络代理  
git config --global http.https://github.com.proxy http://127.0.0.1:7890 //设置网络代理http或者socks5（windows版本git不支持）  
git config --global --unset http.https://github.com.proxy   //取消代理  
# 设置SSH key   
ssh-keygen -t rsa -C "         @qq.com" 

# 本地仓库    
git init  
git add .   //或者git add README.md添加到暂存区（这个只影响当前分支）    
git commit -m "测试"    //提交到本地仓库  
# 关联github  
git remote add origin git@github.com:Pankik23/Test.git   
# 更新本地 -> github   
git add .   //所有修改  
git status  
git commit -m "修改说明"  
git push -u origin main //上传本地仓库  
# github -> 本地   
git pull   
# 分支  
git checkout -b feature  
git add Testing/  
git commit -m "添加新文件到新分支"  
git push -u origin feature   
git merge feature  
git branch -D feature   //删除本地分支  
git push origin --delete feature    //删除远程分支  
  

# others
git rm README.rd    //删除文件  
git fetch --prune   //清理本地过期的远程分支缓存   
git mv 旧文件名 新文件名    //重命名  
git reset HEAD .    //清除暂存区  
