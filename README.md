# How to run Docker file and Demo

_All runs were done on Lab RI server2 (@20.98.84.235)._

## Pull the docker image 
    docker pull jinkyungjo/weather:v2022.03.0

## Run the containe
    docker run -d -it -p 8887:8887 jinkyungjo/weather:v2022.03.0 python3 home/KoBART-summarization/run_api.py 8887 cpu
- Choose the possible port number instead of "8887"

## Connect to [Advanced REST client](https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo/related) with Chrome

- GET URL Examples: http<hi>://20.98.84.235:8887/api/search/text?source=전기간 전지점 일단위 최고온도 3개&date=2022-03-10 00:00:00
    - You can leave the "date" variable empty. (Automatically set to the current date)
<img width="1193" alt="스크린샷 2022-03-12 오후 7 59 39" src="https://user-images.githubusercontent.com/82276223/158015377-da9b9b4e-7e08-4637-9b25-b04256841a7f.png">
