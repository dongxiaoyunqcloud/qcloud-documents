## 소개

[Tencent Cloud GME SDK](https://cloud.tencent.com/product/tmg?idx=1)의 사용을 환영합니다. 개발자가 Tencent Cloud GME 제품을 연결하는 데 도움이 되도록 여기에 GME SDK에 적합한 음질 선택 문서를 소개합니다.

## 음질 유형 소개

서로 다른 응용프로그램 시나리오에 다양한 오디오 유형이 있으며 자세한 내용은 다음 리스트를 참조하십시오.

| 오디오 유형                   | 의미     | 매개변수 | 음량 유형                         | 콘솔 추천 샘플링 속도 설정                                    | 적용 시나리오                                                     |
| -------------------------- | -------- | ---- | -------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------ |
| ITMG_ROOM_TYPE_FLUENCY     | 보통 음질 | 1    | 스피커: 통화 음량. 헤드폰: 미디어 음량 | 음질에 대해 특별한 요구가 없을 경우 16K 샘플링 속도라면 충분합니다.                    | 유창성이 우선이고 지연 시간이 매우 짧은 음성 채팅으로 게임에서 팀 배틀에 적용되고 FPS, MOBA와 같은 게임에 적합합니다. |
| ITMG_ROOM_TYPE_STANDARD    | 표준 음질 | 2    | 스피커: 통화 음량. 헤드폰: 미디어 음량 | 필요한 음질에 따라 16K/48K 샘플링 속도를 선택할 수 있습니다.                | 음질이 비교적 좋고 시간 지연이 적당하여 마피아 게임, 보드게임 등 캐주얼 게임의 실시간 통화 시나리오에 적합합니다. |
| ITMG_ROOM_TYPE_HIGHQUALITY | 고음질 | 3    | 스피커: 미디어 음량, 헤드폰: 미디어 음량 | 최적의 효과를 보증하기 위해서 콘솔에서 48K 샘플링 속도의 고음질 구성을 설정하기를 권장합니다. | 초고음질, 지연시간이 상대적으로 길어서 음악, 댄스 등 게임 및 음성 소셜류 앱에 적용합니다. 음악방송, 온라인 노래방 등 음질 요구가 있는 시나리오에 적용합니다. |

실제 시나리오에 따라 콘솔에서 해당하는 샘플링 속도(16K 또는 48K)를 선택하십시오. SDK 액세스 과정에서 매개변수 가져오기를 통해 “오디오 유형”을 조정할 수 있지만, 실제 샘플링 속도는 콘솔에서 선택한 샘플링 속도를 초과하지 않습니다. 예를 들어 콘솔에서 16K의 샘플링 속도를 선택하고 클라이언트 "오디오 유형" 가져온 매개변수가 "3"이면 실제 샘플링 속도는 16K입니다. 콘솔에서 48K의 샘플링 속도를 선택하고 클라이언트 "오디오 유형" 가져온 매개변수가 "1"이면 실제 샘플링 속도는 16K입니다.

