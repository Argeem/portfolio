FROM liquibase/liquibase:4.25.0

WORKDIR /liquibase/

COPY postgresql-42.7.5.jar .
COPY liquibase.properties .
COPY changelog.yml .
COPY ./sql/ ./sql/

RUN mv docker-entrypoint.sh docker-entrypoint-liquibase.sh

COPY --chown=liquibase:liquibase docker-entrypoint.sh .
RUN chmod +x docker-entrypoint.sh


