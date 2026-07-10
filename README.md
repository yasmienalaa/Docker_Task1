# Docker_Task1
##part1

docker run -d --name alpine_sleeper alpine sleep 1000
docker ps -a
docker stop alpine_sleeper
docker rm alpine_slaaper
docker rmi alpine

###part2

docker run -it --name ubuntu-server ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
docker exec -it ubuntu-server bash
apt update
apt install curl -y
