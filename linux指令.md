1. 多行文本输入

   ```sh
   ➜  Desktop cat >> 1.txt <<ll
   heredoc> he is a good man
   heredoc> oh she is a perfect man
   heredoc> i am a bad man
   heredoc> ll
   ```

2. awk的内置变量

   ```sh
   RS	输入的记录他隔符默 认为换行符
   FS	输入字段分隔符 默认是空格
   NF	当前记录中的字段个数，就是有多少列
   NR	已经读出的记录数，就是行号，从1开始
   FNR	当前记录数
   FILENAME	当前输入文件的名字
   ```

3. mac系统下查ip

   ```sh
   ➜  Desktop ifconfig | egrep 'broadcast' | cut -d" " -f2
   10.222.92.63
   ```

4. 关闭hbase相关的进程

   ```sh
   ➜ jps -l | grep 'hbase' | cut -c 1-4 |xargs kill -9
   ```

5. 统计目录下所有文件总大小

   ```sh
   du -sh dir
   另外还可以通过-d指定统计的深度
   du -h -d1
   ```

   