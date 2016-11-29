# Build
docker build haproxy --tag haproxy
docker build frontend --tag frontend
docker build logstash --tag logstash

# Run
docker run -d --name haproxy -p 80:80 haproxy
docker run -d --name frontend -p 9000:80 frontend
docker run -d --name logstash -p 2000:2000 logstash
docker run -d --name mongo -p 3000:27017 -p 3001:28017 mongo mongod --rest