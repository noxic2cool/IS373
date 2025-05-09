# 12 Factor App

https://s7280.pcdn.co/wp-content/uploads/2019/02/12-factor-app.png
Credits: https://www.bmc.com/blogs/twelve-factor-app/

The 12 Factor App is a methodology for building software-as-a-service applications that emphasizes best practices for modern web applications. It was formulated by Heroku and serves as a guide to ensure that applications are scalable, maintainable, and easy to deploy. Here are the 12 factors:

1. **Codebase**: A single codebase tracked in version control, with many deploys.
   
2. **Dependencies**: Explicitly declare and isolate dependencies, ensuring the app runs consistently in different environments.

3. **Config**: Store configuration in the environment, separating it from code to avoid hardcoding sensitive information.

4. **Backing services**: Treat backing services (like databases, caches, etc.) as attached resources, enabling easy swapping or scaling.

5. **Build, release, run**: Strictly separate the build, release, and run stages, allowing for a consistent deployment process.

6. **Processes**: Execute the app as one or more stateless processes, which can be scaled out and replicated.

7. **Port binding**: Export services via port binding, making the app self-contained and able to run independently.

8. **Concurrency**: Scale out via the process model, allowing the app to handle more requests by adding processes.

9. **Disposability**: Maximize robustness with fast startup and graceful shutdown, ensuring the app can be deployed and scaled easily.

10. **Dev/prod parity**: Keep development, staging, and production environments as similar as possible to avoid discrepancies.

11. **Logs**: Treat logs as event streams, allowing them to be captured and aggregated in real-time for monitoring.

12. **Admin processes**: Run administrative or management tasks as one-off processes, ensuring that they are easily executed in the same environment.

Following these principles helps developers create applications that are resilient, easy to manage, and scalable.

## [GitHub Actions](githubActions.md)
### [Table of Contents](README.md)
