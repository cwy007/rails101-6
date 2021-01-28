# rails101

看板项目（[在线预览](https://rails5-101.herokuapp.com)）

## 项目环境

```bash
➜  rails101 git:(main) ✗ rails about
About your application's environment
Rails version             5.0.7.2
Ruby version              2.6.6-p146 (x86_64-darwin19)
RubyGems version          3.0.8
Rack version              2.2.3
JavaScript Runtime        Node.js (V8)
Middleware                Rack::Sendfile, ActionDispatch::Static, ActionDispatch::Executor, ActiveSupport::Cache::Strategy::LocalCache::Middleware, Rack::Runtime, Rack::MethodOverride, ActionDispatch::RequestId, Sprockets::Rails::QuietAssets, Rails::Rack::Logger, ActionDispatch::ShowExceptions, WebConsole::Middleware, ActionDispatch::DebugExceptions, ActionDispatch::RemoteIp, ActionDispatch::Reloader, ActionDispatch::Callbacks, ActiveRecord::Migration::CheckPending, ActionDispatch::Cookies, ActionDispatch::Session::CookieStore, ActionDispatch::Flash, Rack::Head, Rack::ConditionalGet, Rack::ETag, Warden::Manager
Application root          /Users/chanweiyan/beijing/rails101
Environment               development
Database adapter          sqlite3
Database schema version   20170221075810
```

## 本地启动

```bash
git clone https://github.com/cwy007/rails101.git
cd rails101

bundle install
rails db:create
rails db:migrate
rails server
```

## 部署到 heroku

[注册heroku账号](https://signup.heroku.com/)

>`chanweiyan001@gmail.com`

```bash
heroku login -i
heroku create
git push heroku main:master
heroku run rake db:migrate
heroku open
```

## 参考链接

* [rvm](https://ruby-china.org/wiki/rvm-guide)
* [deploy to heroku](https://courses.growthschool.com/courses/rails-101/lectures/1639213)
* [How do I push a local Git branch to master branch in the remote?](https://stackoverflow.com/questions/5423517/how-do-i-push-a-local-git-branch-to-master-branch-in-the-remote)
  >`git push origin develop:master`
* [IP Address Mismatch on signing into Heroku CLI](https://stackoverflow.com/questions/63363085/ip-address-mismatch-on-signing-into-heroku-cli)
* [Getting Started on Heroku with Rails 5.x](https://devcenter.heroku.com/articles/getting-started-with-rails5)
