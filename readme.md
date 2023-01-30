**Network for docker  
docker network create --driver=bridge --ip-range=172.28.1.0/24 --subnet=172.28.0.0/16 --gateway=172.28.1.254 my_custom_network  
docker network ls  
docker network inspect my_custom_network  

**Volume for docker  
docker volume create postgres-volume-testdb  

**Run container  
docker-compose -f docker-compose_postgres.yaml up -d  
( or : docker start pg_container_testdb if container already exists )  
docker logs pg_container_testdb  

psql -h 172.28.0.7 -U postgres  
Password for user postgres: postgres  
postgres=# \l
    List of databases
    Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges   
    -----------+----------+----------+------------+------------+-----------------------
(truncated )
    testdb    | postgres | UTF8     | en_US.utf8 | en_US.utf8 |
    (4 rows)

docker ps  
docker stop pg_container_testdb     


sources for ARCHUNIT :  
https://dzone.com/articles/spring-boot-unit-test-your-project-architecture-wi  
https://github.com/anicetkeric/archunit  
https://www.archunit.org/userguide/html/000_Index.html#_introduction  