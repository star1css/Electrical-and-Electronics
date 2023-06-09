# Pin diode BPW34 Analysis
> PIN 다이오드를 사용한 방사선 검출기는 광 검출을 이용한 간접적인 방식이 아닌, 직접적인 방식으로 방사선을 검출하는 방법이다. PIN 다이오드의 경우, 감마선과 X-선 검출에 한정되어 사용되며, 충돌에 의해 생성된 전하 캐리어를 측정함으로써 방사선을 감지한다.  

- Absolute Maximum Ratings (절대 최대 정격): 
회로 설계 시 다이오드에 부여할 수 있는 최대 전압, 전류, 온도 등을 확인한다. 이러한 한계를 초과하지 않도록 회로를 설계해야 한다.  

- Electrical Characteristics (전기적 특성): 
스펙트럼 감도, 광전류, 다크 전류, 용량 등의 전기적 특성을 참고하여 회로의 동작 범위와 성능을 결정한다. 이를 바탕으로 적절한 편향 전압을 설정하고, 검출 회로의 민감도를 조절한다.  

- Temperature Characteristics (온도 특성): 
온도에 따른 전기적 특성의 변화를 참고하여, PIN 다이오드가 안정적으로 작동할 수 있는 온도 범위를 결정한다. 필요한 경우 온도를 조절하기 위한 히트싱크나 팬을 설계에 추가한다.  

- Directional Characteristics (방향 특성): 
방향 특성을 참고하여 PIN 다이오드를 최적의 위치와 각도에 배치한다. 이를 통해 방사선의 검출 효율을 최대화할 수 있다.  

- Package and Mounting Information (패키지 및 부착 정보): 
데이터시트의 패키지 및 부착 정보를 참고하여 회로 기판에 다이오드를 올바르게 설치한다. 이는 전기적 및 열적 안정성을 보장하는 데 중요하다.

- Application Notes (응용 노트): 
데이터시트의 응용 노트를 참고하여 일반적인 회로 설계 가이드라인 및 팁을 얻는다. 이를 통해 더 효율적이고 정확한 회로 설계를 수행할 수 있다.
이러한 정보를 바탕으로 회로 설계자는 PIN 다이오드를 사용한 방사선 검출 회로를 올바르게 설계할 수 있다. 
설계 과정에서 데이터시트를 정확히 이해하고, 다양한 조건에서의 성능을 고려하여 안정적이고 정확한 검출 회로를 구축할 수 있다.  

### Pin diode 특성을 그래프로 확인하다  

<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Relative spectral sensitivity-1.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">  [Relative spectral sensitivity Srel = f (λ)]</p>

1. Relative spectral sensitivity Srel: 
이 그래프는 핀 다이오드의 상대 스펙트럼 감도를 파장에 대한 함수로 보여준다. 
이를 통해 다이오드가 어떤 파장의 빛에 더 민감한지 알 수 있다. 
데이터시트에서 보면, BPW34S는 약 800nm 근처에서 최대 감도를 나타낸다.
스펙트럼 감도를 파장에 대한 다이오드가 어떤 파장의 빛에 더 민감한지 데이터시트에서 보면, BPW34S는 약 800nm 근처에서 최대 감도(100%)를 나타내고 있고. 
파장이 400nm에서 약 1100nm 사이에서도 감도가 상대적으로 높다는것을 알수있다.  
  
<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Photocurrent_Open-circuit voltage-2.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">[Photocurrent I/P=f(Ev), VR=5V Open-circuit voltage VO=f(Ev)]</p>

2. Photocurrent, Open-circuit voltage: 
이 그래프는 광전류와 오픈 회로 전압이 조사되는 광자 에너지에 따라 어떻게 변하는지 보여준다. 
이를 통해 빛의 강도(광자 에너지)에 따른 다이오드의 전류 및 전압 특성을 확인할 수 있다.
광전류와 오픈 회로 전압이 조사되는 광자 에너지에 강도(광자 에너지)에 따른 다이오드의 전류 및 전압 특성과 광자 에너지가 증가함에 따라 광전류와 오픈 회로 전압이 증가함을 그리프에서 알수있다.  
  
<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Total power dissipation-3.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">  [Total power dissipation Ptot = f (TA)]</p>  


3. Total power dissipation Ptot: 
이 그래프는 총 전력 소실이 주변 온도에 따라 어떻게 변하는지 보여준다. 
이를 통해 다이오드가 어떤 온도에서 안전하게 작동할 수 있는지 알 수 있다. 
주변 온도가 높아질수록 전력 소실이 감소.
총 전력 소실이은 다이오드가 어떤 온도에서 안전하게 작동할 수 있는지 알 수 있고. 주변 온도가 높아질수록 전력 소실이 감소하고. 주변 온도가 25℃일 때 전력 소실은 약 150mW.  
  
<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Dark current-4.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">  [Dark current IR=f(VR), E=0]</p>   

4. Dark current: 
이 그래프는 빛이 없을 때(어두운 상태)의 전류가 편향 전압에 따라 어떻게 변하는지 보여준다. 
이를 통해 다이오드의 편향 전압에 따른 어두운 상태에서의 전류 특성을 확인할 수 있다.
다이오드의 편향 전압에 따른 어두운 상태에서의 전류 특성을 확인할 수 있고. 전압이 0V에서 20V 사이에서 다크 전류는 전압이 증가함에 따라 대략 선형적으로 증가함.  
  
<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Capacitance-5.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">  [Capacitance C=f(VR), f=1 MHz,E=0]</p>  

5. Capacitance: 
이 그래프는 다이오드의 용량이 편향 전압에 따라 어떻게 변하는지 보여준다. 
이를 통해 다이오드의 전압에 따른 용량 특성을 확인할 수 있다. 
데이터시트에서 보면, 전압이 증가함에 따라 용량이 감소한다.
다이오드의 전압에 따른 용량 특성으로 데이터시트에서 보면, 전압이 증가함에 따라 용량이 감소하며. 전압이 0V에서 약 72pF의 용량을 가지며, 전압이 60V에 도달하면 약 12pF로 감소한다.  
  
<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Dark current-6.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">  [Dark current IR=f(TA), VR=10V,E=0]</p>  

6. Dark current: 
이 그래프는 온도가 달라짐에 따라 어두운 상태에서의 전류가 어떻게 변하는지 보여준다. 
이를 통해 다이오드의 온도에 따른 어두운 상태에서의 전류 특성을 확인
온도가 낮을 때 다크 전류는 매우 낮은 수준을 유지하지만, 온도가 증가함에 따라 다크 전류가 급격히 증가하고. 
이는 고온에서 누설 전류가 더 큰 영향을 미치기 때문이다. 예를 들어, 25℃에서의 다크 전류는 약 2nA이지만, 100℃에서는 약 80nA입니다.  
  
<p align="center">
<img src="https://github.com/star1css/Electrical-and-Electronics/blob/main/./Directional characteristics-7.jpg" width="400px" height="300px" title="Semiconductor type radiation detection sensor"/> 
</p> <p align="center">  [Directional characteristics Srel=f(ϕ)]</p>  

7. Directional characteristics Srel: 
이 그래프는 핀 다이오드의 상대 감도가 입사각에 따라 어떻게 변하는지 보여준다. 
이를 통해 다이오드가 특정 각도에서 빛을 얼마나 잘 감지하는지 파악할 수 있고. 0도(정면)에서 상대 감도가 최대(100%)이며, 각도가 증가함에 따라 감도가 감소하고. 
입사각이 약 60도에서 80도 사이에서 상대 감도가 급격히 감소하여 거의 감지하지 못하게 된다.
