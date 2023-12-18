    kubectl get nodes
    ls
    vi nginx-replicaset.yml
    ls
    kubectl get pods
    kubectl get namespace
    kubectl get pods -namespaces kube-system
    kubectl get pods -n kube-system
    ls
    kubectl apply -f nginx-replicaset.yml
    kubectl get replicaset
    kubectl get pods
    cat nginx-replicaset.yml
    kubectl describe rs nginx-webapp-rs
    kubectl get pods
    kubectl describe pods nginx-webapp-rs-b85cr
    ls
    vi nginx-nodeport-service.yml
    ls
    cat nginx-nodeport-service.yml
    kubectl get svc
    kubectl apply -f nginx-nodeport-service.yml
    kubectl get svc
    kubectl get pods -o wide



## gke votingapp with nodeport and loadbalancer in a dev/prod

 1  gcloud container clusters get-credentials dev-gke-standard-cluster --zone northamerica-northeast1-a --project celestial-gist-401022gcloud container clusters get-credentials dev-gke-standard-cluster --zone northamerica-northeast1-a --project celestial-gist-401022
    2  gcloud container clusters get-credentials dev-gke-standard-cluster-2 --zone northamerica-northeast1-c --project celestial-gist-401022
    3  kubectl get nodes
    4  ls
    5  mkdir replicaset
    6  ls
    7  cd replicaset
    8  vi nginx-replicaset.yml
    9  ls
   10  vi nginx-replicaset.yml
   11  ls
   12  kubectl get pods
   13  kubectl get namespace
   14  kubectl get pods -namespaces kube-system
   15  kubectl get pods -n kube-system
   16  ls
   17  kubectl apply -f ngnix-replicaset.yml
   18  kubectl apply -f nginx-replicaset.yml
   19  kubectl get replicaset
   20  kubectl get pods
   21  cat nginx-replicaset.yml
   22  kubectl describe re nginx-webapp-rs
   23  kubectl describe rs nginx-webapp-rs
   24  kubectl get pods
   25  kubectl describe pods nginx-webapp-rs-b85cr
   26  ls
   27  vi nginx-nodeport-service.yml
   28  ls
   29  cat nginx-nodeport-service.yml
   30  kubectl get svc
   31  kubectl apply -f ngnix-nodeport-service.yml
   32  kubectl apply -f nginx-nodeport-service.yml
   33  kubectl get svc
   34  kubectl get pods -o wide
   35  history
   36  terraform version
   37  gcloud container clusters get-credentials dev-prod-cluster --zone northamerica-northeast1-a --project celestial-gist-401022
   38  kubectl get nodes
   39  gcloud container clusters get-credentials dev-prod-cluster --zone northamerica-northeast1-a --project celestial-gist-401022
   40  kubectl get nodes
   41  ls
   42  git clone https://github.com/BROOKSGATE/gke-prod-voting-microservice-app.git
   43  ls
   44  cd gke-prod-voting-microservice-app/
   45  ls
   46  ll
   47  kubectl get ns
   48  kubectl get all
   49  kubectl create ns votingapp-dev
   50  kubectl get ns
   51  ll
   52  kubectl apply -f postgres-deployment.yml -n votingapp-dev
   53  ls
   54  cd gke-prod-voting-microservice-app/
   55  ll
   56  kubectl apply -f postgres-deployment.yml -n votingapp-dev
   57  kubectl get pods
   58  kubectl get po
   59  kubectl get po -n votingapp-dev
   60  ls
   61  kubectl apply -f . -n votingapp-dev
   62  kubectl get po -n votingapp-dev
   63  kubectl get deploy -n votingapp-dev
   64  kubectl get svc -n votingapp-dev
   65  gcloud container clusters get-credentials dev-prod-cluster --zone northamerica-northeast1-a --project celestial-gist-401022
   66  history
   67  gcloud container clusters get-credentials dev-prod-cluster --zone northamerica-northeast1-a --project celestial-gist-401022
   68  git clone https://github.com/BROOKSGATE/gke-voting-app-loadbalancer-service.git
   69  ls
   70  cd gke-voting-app-loadbalancer-service/
   71  ls
   72  kubectl create ns votingapp-prod
   73  kubectl get ns
   74  kubectl apply -f . -n votingapp-prod
   75  kubectl get all
   76  kubectl get all -n votingapp-prod
   77  kubectl delete svc result-service -n votingapp-prod
   78  kubectl delete svc voting-service -n votingapp-prod
   79  kubectl delete svc voting-service -n votingapp-dev
   80  kubectl delete svc result-service -n votingapp-dev
   81  history