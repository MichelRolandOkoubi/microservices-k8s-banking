FROM postgres:16-alpine

# Set default environment variables
ENV POSTGRES_DB=banking
ENV POSTGRES_USER=admin
ENV POSTGRES_PASSWORD=password

# Copy initialization scripts
# COPY ./init.sql /docker-entrypoint-initdb.d/

EXPOSE 5432
