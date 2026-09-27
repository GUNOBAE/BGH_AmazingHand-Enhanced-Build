# AmazingHand Enhanced 제작 프로젝트

## 프로젝트 소개

이 프로젝트는 Pollen Robotics의 오픈소스 로봇핸드  
**AmazingHand Enhanced**를 직접 제작하고, 제작 과정과 제어 방법을 기록하기 위한 프로젝트입니다.

Feetech **STS3032** 서보모터를 기반으로 손의 각 관절을 제어하고 다양한 동작을 테스트합니다.

추후 별도의 로봇팔을 제작하여 AmazingHand와 연결하고,  
ROS2, 비전 인식, 시뮬레이션까지 하나의 로봇 매니퓰레이터 시스템으로 확장할 예정입니다.

---

## 프로젝트 목표

- AmazingHand Enhanced 제작 과정 기록
- 부품 및 3D 출력물 정리
- STS3032 서보모터 설정 및 캘리브레이션
- Python 기반 손 제어
- 손가락 및 손 전체 동작 테스트
- ROS2 기반 제어 구조 구축
- 자체 제작 로봇팔과 AmazingHand 통합
- 비전 기반 물체 인식 및 파지 제어
- Isaac Sim / Isaac Lab 기반 시뮬레이션 연동

---

## 현재 진행 상태

- [x] 기본 부품 준비
- [x] STS3032 서보모터 준비
- [x] FE-URT2 준비
- [ ] Enhanced 전용 파츠 출력
- [ ] 출력물 후가공
- [ ] 서보 ID 및 설정
- [ ] 손가락 1개 조립
- [ ] 손가락 캘리브레이션
- [ ] 전체 손 조립
- [ ] Python 기본 제어
- [ ] 손 전체 동작 테스트
- [ ] ROS2 연동
- [ ] 로봇팔 통합
- [ ] 비전 기반 제어
- [ ] Isaac Sim / Isaac Lab 연동

---

## BOM 및 제작 비용

실제 구매한 부품과 결제 금액을 기준으로 정리했습니다.  
구매처는 모두 **AliExpress**이며, 가격은 배송비와 할인까지 포함한 **실제 원화 결제 금액**입니다.

| 부품 | 모델 / 규격 | 수량 | 구매처 | 실제 결제 금액 | 비고 |
|---|---|---:|---|---:|---|
| Servo Motor | Feetech STS3032 | 9 | AliExpress | ₩332,800 | 사용 8개 + 예비 1개 |
| Ball Joint | M2 × L19 | 30 | AliExpress | ₩18,974 |  |
| Threaded Rod | M2 × 300 mm | 6 | AliExpress | ₩11,884 |  |
| Bushing | GFM-0608-04 | 8개 이상 | AliExpress | ₩19,650 |  |
| Axis | D2×10 / D2×16 | 각 100 | AliExpress | ₩8,700 | 동일 주문 |
| Thermoplastic Screw | M2.5×6 / M2.5×8 | 각 50 | AliExpress | ₩3,374 | 동일 주문 |
| Large Washer | DIN 9021 M2.5 | 1세트 | AliExpress | ₩1,946 |  |
| Serial Bus Driver | Waveshare Bus Servo Adapter (A) | 1 | AliExpress | ₩11,624 |  |
| Servo Interface | Feetech FE-URT2 | 2 | AliExpress | ₩36,747 |  |
| Flexible Filament | eSUN TPE 83A White 1 kg | 1 | AliExpress | ₩50,900 |  |
| Power Supply | 12V 40A SMPS | 1 | AliExpress | ₩26,445 | 추후 6V 변환 사용 예정 |
| PLA Filament | PLA | 보유 / 추후 기록 | - | - |  |

### 현재 구매 비용

**현재까지 확인된 AmazingHand 관련 구매 총액: ₩523,044**

※ PLA 및 추후 추가 구매 부품은 포함하지 않았습니다.

---

## 3D 프린팅 및 제작 과정

AmazingHand의 대부분의 기구부는 3D 프린팅으로 제작합니다.

### 사용 재료

**PLA**

- Finger Frame
- Servo Horn
- Proximal
- Distal
- Gimbal
- Link
- Hand Plate
- Wrist Interface

**Flexible Material**

- eSUN TPE 83A
- Proximal Shell
- Distal Shell
- Palm Shell
- Top Shell

### 출력 설정

- Printer:
- Nozzle:
- Layer Height:
- Wall:
- Infill:
- Support:
- Print Orientation:

원본 프로젝트에 상세한 조립 가이드가 제공되어 있기 때문에  
본 저장소에서는 모든 조립 단계를 그대로 반복해서 설명하지 않습니다.

대신 직접 제작하면서 중요했던 과정, 헷갈렸던 부분,  
추가 가공이 필요했던 부분과 실제 제작 과정에서 발생한 문제를 중심으로 기록합니다.

### 주요 제작 과정

1. 부품 준비
2. 3D 출력
3. 출력물 후가공
4. Ball Joint Rod 제작
5. Finger Mechanism 조립
6. STS3032 장착
7. Servo ID 설정
8. Finger Calibration
9. 전체 손 조립
10. 배선 및 Serial Bus 구성
11. 기본 동작 테스트

---

## 제어 및 캘리브레이션

AmazingHand Enhanced의 8개 STS3032 서보모터는  
Serial Bus 방식으로 연결하여 제어합니다.

### Servo ID

| Finger | Servo ID |
|---|---|
| Index | 1, 2 |
| Middle | 3, 4 |
| Ring | 5, 6 |
| Thumb | 7, 8 |

### Calibration 과정

- Servo ID 설정
- Middle Position 설정
- Servo Horn 위치 조정
- 최대 가동 범위 확인
- 각 손가락별 Offset 기록

### Calibration 결과

| Finger | Servo | ID | Middle Offset | Min | Max |
|---|---|---:|---:|---:|---:|
| Index | Servo 1 | 1 |  |  |  |
| Index | Servo 2 | 2 |  |  |  |
| Middle | Servo 1 | 3 |  |  |  |
| Middle | Servo 2 | 4 |  |  |  |
| Ring | Servo 1 | 5 |  |  |  |
| Ring | Servo 2 | 6 |  |  |  |
| Thumb | Servo 1 | 7 |  |  |  |
| Thumb | Servo 2 | 8 |  |  |  |

초기에는 원본 프로젝트에서 제공하는 Python 예제를 기반으로 기본 동작을 테스트하고,  
이후 필요에 따라 자체 제어 코드와 ROS2 인터페이스로 확장할 예정입니다.

---

## CAD / 수정 사항

원본 AmazingHand Enhanced CAD를 기반으로 제작합니다.

기본적으로 원본 설계를 유지하지만,  
추후 로봇팔 통합 및 센서 추가를 위해 일부 부품을 수정할 수 있습니다.

### 수정 가능 항목

- Wrist Interface
- Robot Arm Mount
- Camera Mount
- Cable Routing
- Sensor Mount
- Finger Geometry
- Shell Geometry

---

## 테스트, 문제점 및 고찰

제작 완료 후 기본 동작과 실제 파지 성능을 테스트할 예정입니다.

### 테스트 항목

- Finger Flexion / Extension
- Finger Abduction / Adduction
- Individual Finger Control
- Multiple Finger Synchronization
- 반복 위치 정확도
- Servo Temperature
- Servo Load
- Backdrivability
- Grasping Test

제작 과정에서 발생한 문제와 해결 방법도 함께 기록합니다.

### Issue 01

**문제**

작성 예정.

**원인**

작성 예정.

**해결 방법**

작성 예정.

### 고찰 예정 항목

- STS3032 사용에 대한 평가
- Finger Mechanism 구조
- Mechanical Backlash
- 3D Printing Tolerance
- Flexible Shell 효과
- Servo Calibration 방식
- 유지보수성
- 부품 수급성
- 로봇팔 통합 가능성
- 센서 추가 가능성

---

## 향후 계획

### Robot Arm / ROS2

- 자체 로봇팔 설계
- AmazingHand Wrist Interface 제작
- Arm + Hand 통합
- ROS2 Driver 개발
- Joint State 관리
- Motion Command Interface 개발

### Vision

- Object Detection
- Object Pose Estimation
- Hand / Object Tracking
- Vision-based Grasping
- Visual Servoing

### Simulation / Advanced Control

- URDF / MJCF / USD 모델 정리
- Isaac Sim / Isaac Lab 연동
- Sim2Real 실험
- Current / Load Feedback 활용
- Adaptive Grasping
- Reinforcement Learning
- Tactile Sensor 적용 검토

---

## 원본 프로젝트 / License

본 프로젝트는 Pollen Robotics의  
**AmazingHand / AmazingHand Enhanced** 프로젝트를 기반으로 합니다.

- Original Repository: https://github.com/pollen-robotics/AmazingHand
- Enhanced Branch: https://github.com/pollen-robotics/AmazingHand/tree/Amazing-Hand-Enhanced/AmazingHand_Enhanced

원본 프로젝트의 소프트웨어는 **Apache 2.0**,  
기구 설계는 **Creative Commons Attribution 4.0 International (CC BY 4.0)** 라이선스를 따릅니다.

본 저장소는 원본 프로젝트의 조립 가이드를 그대로 재작성하기 위한 목적이 아니라,  
직접 제작하면서 발생한 부품 선택, 출력 조건, 조립 과정, 설정, 문제점, 수정 사항 및 테스트 결과를 기록하는 것을 목적으로 합니다.
