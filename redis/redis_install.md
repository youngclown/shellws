# centos 6 redis 설치

```
# redis 설치 
# epel, remi 저장소는 기본적으로  활성화되지 않으므로 
# --enablerepo 옵션을 주거나 
# /etc/yum.repos.d/{remi,epel}.repo 파일내 enabled 항목을 1로 설정해야 한다.
yum --enablerepo=epel,remi install redis

# 부팅시 자동 실행하도록 설정
chkconfig redis on

# redis 구동
service redis restart
```

# centos install redis-cli only

```
wget http://download.redis.io/redis-stable.tar.gz
tar xvzf redis-stable.tar.gz
cd redis-stable
make
cp src/redis-cli /usr/local/bin/
```
