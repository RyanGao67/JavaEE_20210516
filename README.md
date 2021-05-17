# Build
mvn clean package && docker build -t academy.learnprogramming/hello-todo .

# RUN

docker rm -f hello-todo || true && docker run -d -p 8080:8080 -p 4848:4848 --name hello-todo academy.learnprogramming/hello-todo 

# mvn clean package

# java -jar ~/Downloads/payara-micro-5.2021.3.jar --deploy ./target/hello-todo.war --port 8080

# curl --header "Content-Type: application/json"   --request POST   --data '{"task":"afasdljfldjflksajdfjsa", "dueDate":"2031-01-01"}'  http://localhost:8080/hello-todo/api/v1/todo/new

# curl --header "Content-Type: application/json"     http://localhost:8080/hello-todo/api/v1/todo/list

# java -jar payama.jar --deploy hello-todo.war --port 8080 --outputUberJar helloTodo.jar

# java -jar helloTodo.jar 