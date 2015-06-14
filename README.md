# docker-locust
locust (for Japanese)

docker run -d -p 5557:5557 -p 5558:5558 -p 8089:8089 mnagaku/locust /bin/sh -c 'wget -O test.py ${SCRIPT_URL} && locust -f ./test.py -H ${TARGET_BASE_URL} --master'"

docker run -d -p 5557:5557 -p 5558:5558 mnagaku/locust /bin/sh -c 'wget -O test.py ${SCRIPT_URL} && locust -f ./test.py --slave --master-host=${MASTER_IP}'"
