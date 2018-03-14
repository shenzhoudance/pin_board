# 才华横溢 Ruby on Rails 案例教学 4

## 第一部分：准备动作

```
cd workspace
rails new pin_board
构建新的专案

git init
git commit -m "initial commit"
放入到 git 版本管理

rails s
本地运行

git remote add origin https://github.com/shenzhoudance/pin_board.git
对接 远端 Github 的远程仓库

git push -u origin master
将本地的专案 master 分支 推到 pin_board 的仓库
```
```
gem 'haml', '~> 5.0', '>= 5.0.4'
gem 'bootstrap-sass', '~> 3.3', '>= 3.3.7'
gem 'simple_form', '~> 3.5', '>= 3.5.1'
```
bundle install
rails  s

git checkout -b model-Pin

- Model
```
rails g model Pin title:string description:text
rake db:migrate
```
- Contoller

rails g controller Pins
```
def index
end
```
- Views

app/views/pins/index.html.haml
```
%h1 欢迎来到才华横溢的世界
```
- Routes
```
resources :pins
root "pins#index"
```
![image](https://ws2.sinaimg.cn/large/006tNc79gy1fpce1zhbrbj30xi0fumyf.jpg)

```
git add .
git commit -m "Add Pin model RMVC"
git push origin model-Pin
```
