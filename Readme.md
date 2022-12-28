# 总结
- 执行：CASE_INSENSITIVE=1 cargo run to poem.txt > output.txt

- 二进制程序关注点分离的惯例
    - 将程序拆分为main.rs 和lib.rs 将业务逻辑放入到 lib.rs
    - 当命令行解析逻辑较少时，放入到main.rs 中也行
    - 复杂时，提取到 lib.rs 中

- 区分大小写
    - query.to_lowercase()

- 使用环境变量，在命令行输入变量 
    - eg：CASE_INSENSITIVE=1 cargo run to poem.txt
    - env::var("CASE_INSENSITIVE").is_err();
- 标注输出到文件，标注错误输出到 console