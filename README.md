# Integrating-Helm-Jenkins
## Jenkins Setup
* Install Jenkins in the system using default settings
<img width="1907" height="974" alt="image" src="https://github.com/user-attachments/assets/3be05bea-aabf-4293-8fe2-19dc3613f93b" />

* To find binary path of HELM
  <img width="1145" height="99" alt="image" src="https://github.com/user-attachments/assets/c956a3e9-c147-4993-ba52-bd05d26a59c3" />
  
* Create a pipeline job
  <img width="1899" height="949" alt="image" src="https://github.com/user-attachments/assets/53833161-efc1-42bb-8236-183ddc735942" />

* Add the script to your pipeline job
  <img width="1920" height="942" alt="image" src="https://github.com/user-attachments/assets/4120d3a8-41d9-4335-a67c-da8cc23bd724" />

* Configure so build triigers once code is committed to repository
 <img width="1920" height="878" alt="image" src="https://github.com/user-attachments/assets/d52c8a9e-5d1e-49f5-b5ba-7aeb5e5457e7" />

* Pipeline script for HELM path
  ~ pipeline {
    agent any
    stages {
        stage('Deploy with Helm') {
            steps {
                script {
                    sh '//usr/bin/helm upgrade --install my-webapp ./webapp --namespace default'
                }
            }
        }
    }
}  ~



## UPDATE HELM CHART AND TRIGGER JENKINS PIPELINE

* Open the values.yml file in your webapp folder and increase count to 3
<img width="1569" height="535" alt="image" src="https://github.com/user-attachments/assets/6dfb3eb1-a2bf-4607-b7db-6b0a8e073706" />

* Edit your templates/deployment.yaml file
  <img width="1433" height="367" alt="image" src="https://github.com/user-attachments/assets/fcc49fbe-7eb6-4f5d-857f-43e15be36533" />

* Commit and push your changes
  


