## Descargar cliente
```
curl http://localhost:9090/jnlpJars/jenkins-cli.jar -o jenkins-cli.jar
```
Descargar Job
```
java -jar jenkins-cli.jar -s http://localhost:9090 -auth admin:admin  get-job  Ejemplo  > job_config.xml
```
Crear job
```
java -jar jenkins-cli.jar -s http://localhost:9090 -auth admin:admin  create-job  Ejemplo2  < pipeline_config.xml
```