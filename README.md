# deploying-Microservices-based-voting-application
deploying a fully functional microservices-based voting application

Created Deployments for all components: vote, worker, result, redis, and db.
Configured Services:
-- NodePort for external access (vote and result)
-- ClusterIP for internal communication (redis and db)
-- Connected microservices internally so that:
-- Frontend communicates with worker and Redis.
-- Worker updates results in Redis and/or PostgreSQL.
-- Result service reads from Redis/PostgreSQL.
-- Handled storage:
-- Used emptyDir for Redis caching and DB storage (ephemeral for simplicity).
-- Ensured namespace isolation by deploying everything under vote namespace.
