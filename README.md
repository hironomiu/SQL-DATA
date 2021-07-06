# SQL-DATA

## data insert

パスワードについて適時変更（値、直接入力せずなど）すること

### linux

```
zcat users.dump.gz                  | mysql -u root -pmysql -h127.0.0.1 part1
zcat messages.dump.gz               | mysql -u root -pmysql -h127.0.0.1 part1
zcat follows.dump.gz                | mysql -u root -pmysql -h127.0.0.1 part1
zcat user_birth_month_count.dump.gz | mysql -u root -pmysql -h127.0.0.1 part1
```

### mac

```
gzcat users.dump.gz                  | mysql -u root -pmysql -h127.0.0.1 part1
gzcat messages.dump.gz               | mysql -u root -pmysql -h127.0.0.1 part1
gzcat follows.dump.gz                | mysql -u root -pmysql -h127.0.0.1 part1
gzcat user_birth_month_count.dump.gz | mysql -u root -pmysql -h127.0.0.1 part1
```

## data dump

パスワードについて適時変更（値、直接入力せずなど）すること

```
mysqldump -uroot part1 users -pmysql -h127.0.0.1                  | gzip > users.dump.gz
mysqldump -uroot part1 messages -pmysql -h127.0.0.1               | gzip > messages.dump.gz
mysqldump -uroot part1 follows -pmysql -h127.0.0.1                | gzip > follows.dump.gz
mysqldump -uroot part1 user_birth_month_count -pmysql -h127.0.0.1 | gzip > user_birth_month_count.dump.gz
```
