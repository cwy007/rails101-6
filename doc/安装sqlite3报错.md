# 安装 sqlite3 报错

## 错误信息

```shell
➜  rails101 git:(main) ✗ sudo gem install sqlite3 -v '1.3.13'
Building native extensions. This could take a while...
ERROR:  Error installing sqlite3:
	ERROR: Failed to build gem native extension.

    current directory: /Users/chanweiyan/.rvm/rubies/ruby-3.0.0/lib/ruby/gems/3.0.0/gems/sqlite3-1.3.13/ext/sqlite3
/Users/chanweiyan/.rvm/rubies/ruby-3.0.0/bin/ruby -I /Users/chanweiyan/.rvm/rubies/ruby-3.0.0/lib/ruby/3.0.0 -r ./siteconf20210128-8351-zvffkq.rb extconf.rb
checking for sqlite3.h... yes
checking for pthread_create() in -lpthread... yes
checking for sqlite3_libversion_number() in -lsqlite3... yes
checking for rb_proc_arity()... yes
checking for rb_integer_pack()... yes
checking for sqlite3_initialize()... yes
checking for sqlite3_backup_init()... yes
checking for sqlite3_column_database_name()... yes
checking for sqlite3_enable_load_extension()... yes
checking for sqlite3_load_extension()... yes
checking for sqlite3_open_v2()... yes
checking for sqlite3_prepare_v2()... yes
checking for sqlite3_int64 in sqlite3.h... yes
checking for sqlite3_uint64 in sqlite3.h... yes
creating Makefile

current directory: /Users/chanweiyan/.rvm/rubies/ruby-3.0.0/lib/ruby/gems/3.0.0/gems/sqlite3-1.3.13/ext/sqlite3
make "DESTDIR=" clean

current directory: /Users/chanweiyan/.rvm/rubies/ruby-3.0.0/lib/ruby/gems/3.0.0/gems/sqlite3-1.3.13/ext/sqlite3
make "DESTDIR="
compiling backup.c
compiling database.c
database.c:60:3: error: implicit declaration of function 'rb_check_safe_obj' is invalid in C99 [-Werror,-Wimplicit-function-declaration]
  rb_check_safe_obj(file);
  ^
database.c:60:3: note: did you mean 'rb_check_safe_str'?
/Users/chanweiyan/.rvm/rubies/ruby-3.0.0/include/ruby-3.0.0/ruby/internal/core/rstring.h:97:6: note: 'rb_check_safe_str' declared here
void rb_check_safe_str(VALUE);
     ^
1 error generated.
make: *** [database.o] Error 1

make failed, exit code 2

Gem files will remain installed in /Users/chanweiyan/.rvm/rubies/ruby-3.0.0/lib/ruby/gems/3.0.0/gems/sqlite3-1.3.13 for inspection.
Results logged to /Users/chanweiyan/.rvm/rubies/ruby-3.0.0/lib/ruby/gems/3.0.0/extensions/x86_64-darwin-20/3.0.0/sqlite3-1.3.13/gem_make.out
```

## 解决方法

ruby 版本问题

ruby 版本不要大于 ruby 2.7

## 参考链接

* <https://github.com/sparklemotion/sqlite3-ruby/pull/277>
