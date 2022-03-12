# [기상과학원] Docker file and demo

__All runs were done on Lab RI server2 (@20.98.84.235).__

### Pull the docker image
'''
docker pull jinkyungjo/weather:v2022.03.0
'''

### Run the container
'''
docker run -d -it -p 8887:8887 jinkyungjo/weather:v2022.03.0
'''
- Choose the possible port number instead of 8887

### Check the name of the container
'''
docker ps -a
'''
- Example: 
<img width="1144" alt="스크린샷 2022-03-12 오후 7 35 14" src="https://user-images.githubusercontent.com/82276223/158014677-752a8e3f-4223-4c9d-ac72-9988fc7461aa.png">

### Execute the container with its name
'''
docker exec -it modest_ardinghelli /bin/bash
'''

### Run API
'''
python3 home/KoBART-summarization/run_api.py 8887 cpu
'''
- Choose the possible port number instead of 8887

### Connect to [Advanced REST client][https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo/related] with Chrome

- GET URL Examples: http://20.98.84.235:8887/api/search/text?source=전기간 전지점 일단위 최고온도 3개&date=2022-03-10 00:00:00
<img width="1193" alt="스크린샷 2022-03-12 오후 7 59 39" src="https://user-images.githubusercontent.com/82276223/158015377-da9b9b4e-7e08-4637-9b25-b04256841a7f.png">