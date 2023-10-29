# Tasks
## Task1
    - Create kubernetes secret with the name **test-secret** which will contain key4=value4. 
    - Mount this secret into pod called **secret-pod** and mount it as OS variable.
    - use **nginx:stable** as image for this task
## Task2
    - Create kubernetes secret with the name **test-secret** which will contain:
     ```
        spring:
            oracle:
                username: user
                password: pass            
     ```
    - Mount this secret into pod called **secret-pod** and mount it file path:
    ```
        /temp/data
    ```
    - use **nginx:stable** as image for this task
## Task3
    - Create a deployment called **deployment-test**
    - image used is **nginx:stable**
    - Configure the resources for this deployment to be:
        - memory-limit: 512Mi
        - memory-request: 128Mi
        - cpu-request: 10mcpu
        - cpu-limit: 100mcpu
## Task4
    - Set the number of replicas to 3 for deployment from **task3**
    - Set affinity that it should split the pods to not run on the same workerNode but if there isn't a enough workerNodes it will allow to deploy it.
## Task5
    - Create a service called **test-service** and match it with the application's from task4
    - try to curl the endpoint to get response
    - Which endpoint was working and what you had to do for it?
## Task6    
    - Edit the service form **Task5** and make it as NodePort service
    - the NodePort on which it should listen should be 31000
    - On which endpoints is the application responding now?
## Task7
    - Create a configmap and mount it to the pod with the same values as it was performed on the **Task1**
    - name the configmap **test-configmap**
## Task8    
    - Create a configmap and mount it to the pod with the same values as it was performed on the **Task2**
    - name the configmap **test-configmap-mount**