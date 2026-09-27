# AmazingHand Enhanced 제작 프로젝트

## 프로젝트 소개

이 프로젝트는 Pollen Robotics의 오픈소스 로봇핸드  
**AmazingHand Enhanced**를 직접 제작하고,  
제작 과정과 제어 방법을 기록하기 위한 프로젝트입니다.

AmazingHand Enhanced에 사용되는  
Feetech STS3032 서보모터를 기반으로  
손의 각 관절을 제어하고 다양한 동작을 테스트하는 것을 목표로 합니다.

추후 별도의 로봇팔을 제작하여  
AmazingHand와 연결하고,  
하나의 로봇 매니퓰레이터 시스템으로 확장할 예정입니다.

---

## 프로젝트 목표

- AmazingHand Enhanced 제작 과정 기록
- 부품 및 3D 출력물 정리
- STS3032 서보모터 설정 및 캘리브레이션
- Python 기반 손 제어
- 손가락 및 손 전체 동작 테스트
- ROS2 기반 제어 구조 구축
- 추후 로봇팔 제작 및 AmazingHand와 통합
- 비전 기반 물체 인식 및 파지 제어
- Isaac Sim / Isaac Lab 기반 시뮬레이션 연동 검토

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

## 원본 프로젝트

본 프로젝트는 Pollen Robotics의  
**AmazingHand / AmazingHand Enhanced** 프로젝트를 기반으로 합니다.

- Original Repository: https://github.com/pollen-robotics/AmazingHand
- Enhanced Branch: https://github.com/pollen-robotics/AmazingHand/tree/Amazing-Hand-Enhanced/AmazingHand_Enhanced

본 저장소는 원본 프로젝트의 조립 가이드를 그대로 재작성하기 위한 목적이 아니라,  
직접 제작하면서 발생한 **부품 선택, 출력 조건, 조립 과정, 설정, 문제점, 수정 사항 및 테스트 결과**를 기록하는 것을 목적으로 합니다.

자세한 원본 조립 방법과 CAD 자료는  
Pollen Robotics의 공식 저장소 및 문서를 참고합니다.

---

## 시스템 개요

AmazingHand Enhanced는 4개의 손가락과  
총 8개의 Feetech STS3032 서보모터로 구성된  
8-DOF 로봇핸드입니다.

### 주요 구성

- 4 Fingers
- 8 DOF
- Feetech STS3032 × 8
- Serial Bus Servo Control
- 3D Printed Mechanical Structure
- Flexible Finger / Palm Shell
- Python Based Control

추후 자체 제작 로봇팔과 통합하여  
하나의 로봇 매니퓰레이터 시스템으로 확장할 예정입니다.

---

## BOM 및 제작 비용

실제 제작에 사용한 부품을 기준으로  
구매처, 수량, 가격을 정리할 예정입니다.

| 부품 | 모델 / 규격 | 수량 | 구매처 | 가격 | 비고 |
|---|---|---:|---|---:|---|
| Servo Motor | Feetech STS3032 | 8 |  |  |  |
| Ball Joint | M2 | 16 |  |  |  |
| Threaded Rod | M2 | 1 |  |  |  |
| Bushing | GFM 0608-04 | 8 |  |  |  |
| Axis | D2×10 | 8 |  |  |  |
| Axis | D2×16 | 8 |  |  |  |
| Thermoplastic Screw | M2.5×6 | 16 |  |  |  |
| Thermoplastic Screw | M2.5×8 | 30 |  |  |  |
| Washer | M2.5 | 4 |  |  |  |
| Servo Driver | FE-URT2 | 1 |  |  |  |
| Power Supply | 6V | 1 |  |  |  |
| PLA Filament |  |  |  |  |  |
| Flexible Filament | eSUN TPE 83A |  |  |  |  |

### 총 제작 비용

추후 실제 구매 비용을 기준으로 작성 예정.

---

## 3D 프린팅

AmazingHand의 대부분의 기구부는  
3D 프린팅으로 제작합니다.

### 사용 재료

#### PLA

주요 구조 부품에 사용합니다.

- Finger Frame
- Servo Horn
- Proximal
- Distal
- Gimbal
- Link
- Hand Plate
- Wrist Interface

#### Flexible Material

손가락과 손 외피에 사용합니다.

사용 예정 재료:

- eSUN TPE 83A

적용 부품:

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

추후 실제 출력 결과와 실패 사례를 기준으로  
세부 설정을 추가할 예정입니다.

---

## 제작 과정

원본 프로젝트에 상세한 조립 가이드가 제공되어 있기 때문에  
본 저장소에서는 모든 조립 단계를 그대로 반복해서 설명하지 않습니다.

대신 직접 제작하면서 중요했던 과정,  
헷갈렸던 부분, 추가 가공이 필요했던 부분,  
실제 제작 과정에서 발생한 문제를 중심으로 기록합니다.

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

### 제작 과정 기록

추후 실제 제작 진행에 따라 사진과 내용을 추가할 예정입니다.

---

## 전자 시스템

AmazingHand Enhanced의 8개 STS3032 서보모터는  
Serial Bus 방식으로 연결하여 제어합니다.

```text
PC / Controller
      │
      │ USB / Serial
      ▼
Serial Bus Servo Driver
      │
      ▼
STS3032 Servo Bus
      │
      ├── Servo 1
      ├── Servo 2
      ├── Servo 3
      ├── Servo 4
      ├── Servo 5
      ├── Servo 6
      ├── Servo 7
      └── Servo 8
```

### Servo ID

| Finger | Servo ID |
|---|---|
| Index | 1, 2 |
| Middle | 3, 4 |
| Ring | 5, 6 |
| Thumb | 7, 8 |

---

## Servo Calibration

각 서보의 중심 위치와  
손가락의 가동 범위를 맞추기 위해  
개별 캘리브레이션을 수행합니다.

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

---

## 제어

초기에는 원본 프로젝트에서 제공하는  
Python 예제 코드를 기반으로 기본 동작을 테스트합니다.

추후 필요한 부분을 수정하거나  
자체 제어 코드로 확장할 예정입니다.

### 목표

- Individual Finger Control
- Hand Pose Control
- Motion Sequence
- Servo Feedback Monitoring
- ROS2 Command Interface

---

## CAD 및 수정 사항

원본 AmazingHand Enhanced CAD를 기반으로 제작합니다.

기본적으로 원본 설계를 유지하지만,  
추후 로봇팔 통합 및 센서 추가를 위해  
일부 부품을 수정할 수 있습니다.

### 수정 가능 항목

- Wrist Interface
- Robot Arm Mount
- Camera Mount
- Cable Routing
- Sensor Mount
- Finger Geometry
- Shell Geometry

---

## 테스트

제작 완료 후 손의 기본 동작과 실제 파지 성능을 테스트할 예정입니다.

### 기본 동작 테스트

- Finger Flexion / Extension
- Finger Abduction / Adduction
- Individual Finger Control
- Multiple Finger Synchronization

### 성능 테스트

- 반복 위치 정확도
- Servo Temperature
- Servo Load
- Backdrivability
- Grasping Test

### 파지 테스트

추후 다양한 형태와 크기의 물체를 대상으로  
파지 테스트를 진행할 예정입니다.

---

## 문제점 및 해결 과정

제작 과정에서 발생한 문제와 해결 방법을 기록합니다.

### Issue 01

**문제**

작성 예정.

**원인**

작성 예정.

**해결 방법**

작성 예정.

---

## 설계 및 제작 고찰

직접 제작하면서 확인한 설계 특징과  
장단점, 개선 가능한 부분을 기록합니다.

### 검토 예정 항목

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

## ROS2 연동

AmazingHand를 ROS2 기반 시스템에 통합할 예정입니다.

예상 구조:

```text
ROS2
 │
 ├── Hand Driver Node
 ├── Servo Communication Node
 ├── Joint State Publisher
 └── Hand Command Interface
```

예상 Topic:

```text
/hand/joint_states
/hand/command
/hand/servo_state
```

구체적인 구조는 실제 개발 과정에서 변경될 수 있습니다.

---

## 로봇팔 통합

AmazingHand 제작 완료 후  
별도의 로봇팔을 직접 설계 및 제작하여  
AmazingHand와 연결할 예정입니다.

### 목표

- Custom Robot Arm 제작
- Wrist Interface 설계
- Arm + Hand 통합
- ROS2 기반 통합 제어
- End-Effector 좌표계 구성
- Motion Planning 적용 검토

---

## Vision

추후 카메라 기반 비전 시스템을 추가하여  
물체를 인식하고 로봇팔과 손을 제어하는 기능을 개발할 예정입니다.

### 목표

- Object Detection
- Object Pose Estimation
- Hand / Object Tracking
- Vision-based Grasping
- Visual Servoing

---

## Simulation

실물 제작과 함께  
시뮬레이션 환경에서 사용할 수 있는 로봇 모델도 구성할 예정입니다.

### 목표

- URDF 정리
- MJCF 활용
- USD 변환
- Isaac Sim 연동
- Isaac Lab 연동
- Sim2Real 실험

추후 자체 제작 로봇팔과 AmazingHand를  
하나의 articulated robot으로 통합하는 것을 목표로 합니다.

---

## 향후 계획

### Robot Arm

- 자체 로봇팔 설계
- AmazingHand Wrist Interface 제작
- Arm + Hand 통합

### ROS2

- AmazingHand Driver 개발
- Joint State 관리
- Motion Command Interface 개발

### Vision

- 물체 인식
- Object Pose Estimation
- Hand / Object Tracking
- Vision-based Grasping

### Simulation

- URDF / MJCF / USD 모델 정리
- Isaac Sim / Isaac Lab 연동
- Sim2Real 실험

### Advanced Control

- Current / Load Feedback 활용
- Adaptive Grasping
- Reinforcement Learning
- Tactile Sensor 적용 검토

---

## References

- Pollen Robotics
- AmazingHand
- AmazingHand Enhanced
- Feetech STS3032

추후 참고한 문서, 논문, 데이터시트 등을 추가할 예정입니다.

---

## License / Attribution

본 프로젝트는 Pollen Robotics의 AmazingHand 프로젝트를 기반으로 합니다.

원본 프로젝트의 소프트웨어는 Apache 2.0,  
기구 설계는 Creative Commons Attribution 4.0 International(CC BY 4.0) 라이선스를 따릅니다.

본 저장소에서 새롭게 작성한 코드,  
수정한 설계 파일 및 제작 기록에 대한 라이선스는  
추후 별도로 명시할 예정입니다.
