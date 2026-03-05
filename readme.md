# 网络代理
git config --global http.https://github.com.proxy http://127.0.0.1:7890   //设置网络代理http或者socks5（windows版本git不支持）
git config --global --unset http.https://github.com.proxy   //取消代理

# 设置SSH key
ssh-keygen -t rsa -C "         @qq.com"

# 本地仓库
git init
git add .   //或者git add README.md添加到暂存区
git commit -m "第一次修改"  //提交到本地仓库
# 关联github
git remote add origin git@github.com:Pankik23/Test.git
git push -u origin main //上传本地代码

# 更新本地 -> github
git status
git add .
git commit -m "修改说明"
git push
# github -> 本地
git pull