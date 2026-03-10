FROM eclipse-temurin:17-jdk-focal

ENV MB_PLUGINS_DIR=/plugins

RUN mkdir -p /plugins
RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*
RUN curl -L https://github.com -o metabase.jar
ADD https://github.com/MotherDuck-Open-Source/metabase_duckdb_driver/releases/download/0.2.12-b/duckdb.metabase-driver.jar /home/plugins/

RUN chmod 744 /home/plugins/duckdb.metabase-driver.jar

CMD ["java", "-jar", "/home/metabase.jar"]