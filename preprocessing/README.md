# Human voice Separating with Spleeter
## spleeter를 사용한 계기
Spleeter는 노래에 있어 보컬 부분과 반주(악기별 분류 가능)를 분리하는 딥러닝 모델입니다.  
문제: **train set**의 오디오 파일에 있어 가끔 사람의 목소리가 동물 소리에 섞여 있습니다.  
노래 또한 **반주 속에 사람 목소리가 섞인 오디오 파일**이기 때문에 spleeter를 통해 전처리가 가능할 것으로 판단했습니다.

### output 구조
spleeter를 통해 분리된 ogg파일은 ogg파일명의 디렉토리에 사람목소리인 vocals.wav와 vocals를 제거한 오디오파일인 accompaniment.wav파일로 나뉩니다.  
각 파일을 식별하기 위해 원래 파일명으로 교체해주는 과정을 거칩니다.  
ex) 1234.ogg -spleeter-> 1234/vocals.wav, 1234/accompaniment.wav -> 1234/1234.wav, 1234/1234HumanVoice.wav
