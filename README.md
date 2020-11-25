# UnicornGymTeam2
raspberrypi에서 다음 명령어 실행해주세요.
```
cd ~
git clone https://github.com/reoim/UnicornGymTeam2.git
```

기존 sample 코드를 백업하고 다운받은 sample 코드로 변경해주세요.
```
mv ~/aws-iot-device-sdk-python/samples/basicPubSub/basicPubSub.py ~/aws-iot-device-sdk-python/samples/basicPubSub/basicPubSub.py.backup

chmod +x ~/UnicornGymTeam2/basicPubSub.py

mv ~/UnicornGymTeam2/basicPubSub.py ~/aws-iot-device-sdk-python/samples/basicPubSub/basicPubSub.py
```

raspberrypi에서 다음 명령어 실행해주세요.
```
echo "export MY_NAME='(자신의 이름으로 변경해주세요)'" >> ~/.bashrc
source ~/.bashrc
```

환경변수 MY_NAME 등록 되었는지 확인
```
echo $MY_NAME
```

결과 예)
```
pi@raspberrypi:~ $ echo $MY_NAME
reolee
```

run 스크립트 실행 (주의: sudo로 실행하지 말것. 환경변수 못 읽어옴)
```
./run_basicpubsub.sh
```

test 결과 (topic은 topic_1 으로 만들었습니다.)
![test](/images/test.png)