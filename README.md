# 수수료 개선을 통한 전문가 이탈 방지 및 추천 시스템 기반 고객 만족도 향상을 통한 경쟁력 강화

# 프로젝트 팀 소개
<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/3bad0c6d-7c60-443b-93a9-fbc07f2dfa74" />

# 1. 수행절차
<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/e1131c7a-f853-40de-9ce9-bbb0dac87f50" />

# 2. 추진배경 및 현황
<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/9b2a485a-b40d-4d19-9853-5d1ba3eb66c3" />
- 아웃소싱 중계 플랫폼 시장과 함께 자사도 성장 중이지만, 경쟁사의 공격적 마케팅과 IT 전문가 이탈로 위기감이 조성

-> 당사의 IT 전문가 이탈을 막고 경쟁력을 강화할 필요가 있음

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/0de564e8-551d-481e-809a-06f148fc32f3" />

재능마켓 플랫폼을 활용하는 판매자들이 과도한 수수료 문제로 고통 받고 있는 것으로 확인

-> 수수료 시스템 개선을 통해 판매자들의 안정적인 활동 지원 필요

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/1dff048c-7bb1-4fe7-88d7-504a594ec15e" />

비교 견적과 2개 이상의 업체 연결을 희망하는 선택권을 가질 수 있는 성향으로 파악됨

 -> IT 아웃소싱에서 전문업체 연결 기능, 업체 간 견적 비교 기능 필요

 # 3. 특성요인도
 <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/c97fec28-d066-4251-ab89-460fd8a04d7e" />

 # 4. 사용 데이터
 <table border="1">
    <thead>
        <tr>
            <th>변수명</th>
            <th>타입</th>
            <th>설명</th>
            <th>변수명</th>
            <th>타입</th>
            <th>설명</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>거래일자</td>
            <td>TimeStamp</td>
            <td>서비스가 거래된 일자</td>
            <td>판매금액</td>
            <td>연속형</td>
            <td>처음 판매자와 구매자가 계약한 서비스의 거래 금액 (원)</td>
        </tr>
        <tr>
            <td>고객ID</td>
            <td>ID</td>
            <td>고객 고유 ID</td>
            <td>서비스가격</td>
            <td>연속형</td>
            <td>판매자가 올린 해당 서비스 가격</td>
        </tr>
        <tr>
            <td>프로그램 수정횟수</td>
            <td>연속형</td>
            <td>고객이 요청한 프로그램 수정횟수 (1회)</td>
            <td>평점</td>
            <td>연속형</td>
            <td>사용자의 이용 평점 (0 ~ 5점)</td>
        </tr>
        <tr>
            <td>추가결제 금액</td>
            <td>연속형</td>
            <td>고객이 추가로 지불한 추가 결제금액 (원)</td>
            <td>이용자수</td>
            <td>연속형</td>
            <td>해당 서비스의 총 이용자 수</td>
        </tr>
        <tr>
            <td>거래취소 여부</td>
            <td>범주형</td>
            <td>고객 또는 전문가에 의한 서비스 취소 여부</td>
            <td>서비스 대분류</td>
            <td>범주형</td>
            <td>서비스 대분류</td>
        </tr>
        <tr>
            <td>거래취소 일자</td>
            <td>TimeStamp</td>
            <td>취소일자</td>
            <td>서비스 번호</td>
            <td>ID</td>
            <td>서비스 고유 ID</td>
        </tr>
        <tr>
            <td>서비스명</td>
            <td>ID</td>
            <td>전문가가 설정한 서비스 명</td>
            <td>수수료율</td>
            <td>연속형</td>
            <td>자사에서 얻어가는 수수료율 (%)</td>
        </tr>
        <tr>
            <td>판매자</td>
            <td>범주형</td>
            <td>판매자 ID</td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>

# 5. 분석계획
<table border="1">
    <thead>
        <tr>
            <th>목적</th>
            <th>분석방법</th>
            <th>주요내용</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan="2">전체 데이터 분포 및 이상치 확인</td>
            <td>히스토그램</td>
            <td>판매금액, 서비스가격 등 연속형 변수들의 분포 및 이상치 확인</td>
        </tr>
        <tr>
            <td>막대그래프</td>
            <td>성별, 거주지, 프리미엄 서비스 가입 여부 등 범주형 변수들의 빈도수 시각화하여 특성 확인</td>
        </tr>
        <tr>
            <td rowspan="3">각 변수 간의 주요 특성 및 관계 파악</td>
            <td>box plot</td>
            <td>프로그램 수정 횟수, 유입경로, 거래취소여부 등 범주형 변수와 수수료율, 이용자수, 평점 등 연속형 변수 특성 파악</td>
        </tr>
        <tr>
            <td>chi-square test</td>
            <td>소득별 프리미엄 서비스 가입 여부, 신속 알림 서비스 사용여부 차이 분석</td>
        </tr>
        <tr>
            <td>2-sample t test</td>
            <td>소득별 총 판매 금액 차이 검정</td>
        </tr>
        <tr>
            <td>서비스명의 특징 파악</td>
            <td>텍스트마이닝</td>
            <td>okt를 이용해 명사 분류 후 각 대분류별 특징 도출</td>
        </tr>
        <tr>
            <td>판매금액별 특징 분석</td>
            <td>군집분석</td>
            <td>판매금액별 총 수량 요청 횟수, 연령대, 취소여부 등 군집의 특성 파악</td>
        </tr>
        <tr>
            <td>수수료 개선을 위한 전문가 세분화</td>
            <td>RFM</td>
            <td>전문가 등급 세분화를 위해 RFM</td>
        </tr>
        <tr>
            <td>추천시스템</td>
            <td>유사도 분석</td>
            <td>비슷한 소비자를 파악하여 추천시스템 개발</td>
        </tr>
        <tr>
            <td>앱과 사이트 추가 문제점 파악</td>
            <td>텍스트마이닝</td>
            <td>앱과 리뷰 데이터로 문제점을 분석하여 니즈 파악</td>
        </tr>
        <tr>
            <td>전문가 이탈 가능성</td>
            <td>RFM, LTV</td>
            <td>RFM 분석 후 전문가 생애 지수를 파악</td>
        </tr>
    </tbody>
</table>

# 6. 현황파악

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/87e4d00c-4b16-4efe-9c0e-08dda3c49957" />

### 판매자, 고객 별 동일한 상황에서 수수료율에 차이가 있음을 확인.  현재 수수료에 대한 명확한 기준 X

-> 명확한 수수료 기준 확립 필요

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/75da56bd-d149-4db7-b15c-20ddfd946dc8" />

### 판매 금액이 높은 사람들이 매출의 큰 비중을 차지
-> 실적에 따른 차별화된 시스템 필요

# 7. RFM 분석기법 적용

### 이탈 예측 클래스 생성

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/c81c2742-6ca0-4bcf-96b6-e2dd6f4b0f53" />


### 예상 기대 수익 모형 생성
<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/c15fec22-28ac-428e-97fd-c4475676cf58" />

<br><br>

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/db1b7be8-189d-4b84-940f-098e607aa97c" />

### 이탈 위험 판매자의 평균 기대수익이 가장 높음

-> 해당 군집의 판매자들을 유인할 수 있는 정책 필요


# 8. 수수료 시스템 개선
<table border="1" style="border-collapse: collapse; text-align: center;">
    <thead>
        <tr style="background-color: #2D2178; color: white;">
            <th>매출</th>
            <th>일괄</th>
            <th>100만원 판매 달성</th>
            <th>200만원 판매 달성</th>
            <th>500만원 판매 달성</th>
            <th>1000만원 판매 달성</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="background-color: #2D2178; color: white;">수수료</td>
            <td>10%</td>
            <td>9%</td>
            <td>7%</td>
            <td>5%</td>
            <td>3%</td>
        </tr>
    </tbody>
</table>

<br>

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/cd3fe01f-6a63-4443-b664-6ffab89ac49f" />

















