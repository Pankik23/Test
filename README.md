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
git pull    //只能在当前分支改代码   

cd ..   //回到上级目录   
rm -rf "Test Repository"    //删除旧仓库  
git clone https://github.com/Pankik23/Test.git  //重新开始，所有的分支数据都和github一致   
cd Test  

git fetch origin  
git reset --hard origin/main  
git push -u origin main //强制删除本地   

git push -f origin main //强制覆盖远程  

# 分支  
git checkout -b feature_new  
git add Testing/  
git commit -m "添加新文件到新分支"  
git push -u origin feature_new  //第一次使用需要-u   
git merge feature  //合并分支   
git branch -D feature   //删除本地分支  
git push origin --delete feature    //删除远程分支  
git fetch --prune   //清理本地过期的远程分支目录       
  
# others
git rm README.rd    //删除文件  
git mv 旧文件名 新文件名    //重命名  
git reset HEAD .    //清除暂存区  
