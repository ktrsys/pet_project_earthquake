FROM metabase/metabase:v0.53.3

# Используем путь относительно контекста сборки
# Если в docker-compose.yaml context: ./metabase, то просто имя файла
# Если context: ., то metabase/duckdb.metabase-driver.jar
COPY ./metabase/duckdb.metabase-driver.jar /plugins/

USER root
RUN chmod 644 /plugins/duckdb.metabase-driver.jar