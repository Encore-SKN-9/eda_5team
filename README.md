# **프로젝트 명 : 기대수명 요인 분석** 🚀  

## 📌**프로젝트 배경**
![image](https://github.com/user-attachments/assets/e6a39c71-edfd-4a01-9646-d08063af821c)

[Click here for more information](https://www.yna.co.kr/view/AKR20240806040000017)
> **뉴스 헤드라인**: 성별·결혼·교육·인종에 따라 기대수명 18년 차이  
* 미국 연구팀은 성별, 결혼, 교육 수준, 인종의 조합에 따라 기대수명이 최대 18년까지 차이가 날 수 있음을 발견했다.  
* 예를 들어, "고졸 이하·미혼·백인·남성"의 기대수명은 약 37.1년인 반면, "대졸 이상·기혼·백인·여성"의 기대수명은 약 55.1년으로 조사된 바 있다.

---

## 📌 **프로젝트 목표**  
우리 팀은 이 연구에서 한발 더 나아가, 국가적 요인(건강, 교육, GDP, 경제) 및 다양한 변수들이 기대수명에 어떤 영향을 미치는지 구체적으로 분석하여 인사이트를 도출하고자 합니다.

---
## 🌟**팀명**
## 🌟 **팀원 소개**  

| 이름      | GitHub ID                          |
|-----------|------------------------------------|
| 🧑‍💻 박유진  | [@YUJINDL01](https://github.com/YUJINDL01) |
| 👩‍💻 이다인  | [@daainn](https://github.com/daainn)        |
| 👩‍💻 이재혁  | [@ohdyo](https://github.com/ohdyo)          |
| 👨‍💻 최재동  | [@Monkakaka](https://github.com/Monkakaka) |

---

## 🛠️ **기술 스택**  

| **분류**         | **기술/도구**                                                                            |
|------------------|------------------------------------------------------------------------------------------|
| **언어**         | ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python)     |
| **라이브러리**   | ![NumPy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy)       ![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas)   ![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=Matplotlib) ![Folium](https://img.shields.io/badge/Folium-77B829?style=for-the-badge&logo=folium&logoColor=white) |
| **협업 툴**      | ![GitHub](https://img.shields.io/badge/github-121011?style=for-the-badge&logo=github)   ![Git](https://img.shields.io/badge/git-F05033?style=for-the-badge&logo=git)          |

---

## 📄 **프로젝트 설명**  

### 1. 데이터 선택 근거  

* 해당 데이터셋은 다양한 국가의 평균 수명 데이터를 통합한 것으로, 사회경제적 요인과 건강 관련 지표도 함께 제공한다. 
* 따라서 해당 데이터셋을 통해 수명과 지표 간의 상관관계 및 지역 간 불평등을 분석하는 데 유용할 것이라 판단하여서 데이터를 선택하였다.

**데이터 출처**
[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-blue?logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/shreyasg23/life-expectancy-averaged-dataset/code)


### 2. 데이터 구조  

#### **분석 타겟 컬럼**
- `Life_expectancy` (float): 기대수명

#### **유아, 청소년 관련 변수**  
- `Infant_deaths` (float): 영아 사망 수  
- `Under_five_deaths` (float): 5세 이하 사망 수  
- `Polio` (float): 소아마비 예방접종률  
- `Thinness_five_nine_years` (float): 5-9세 저체중 비율  
- `Thinness_ten_nineteen_years` (float): 10-19세 저체중 비율  

#### **건강 관련 변수**  
- `Diphtheria` (float): 디프테리아 예방접종률  
- `Incidents_HIV` (float): HIV 발생 건수  
- `Hepatitis_B` (float): B형 간염 예방접종률  
- `Measles` (float): 홍역 사례 수  

#### **경제적 사회적 요인 변수**  
- `Country` (object): 국가명  
- `Region` (object): 지역명  
- `GDP_per_capita` (float): 1인당 GDP  
- `Population_mln` (float): 인구 (백만 명 단위)  

#### **생활 수준 및 습관 관련 변수**  
- `BMI` (float): 평균 BMI(체질량지수)  
- `Schooling` (float): 평균 교육 연수  
- `Economy_status` (object): 경제 상태 (예: 저소득, 중소득, 고소득)  
- `Alcohol_consumption` (float): 1인당 알코올 소비량  
- `Adult_mortality` (float): 성인 사망률

  

### 3. 데이터 기초 통계량  
|   | Year   | Infant_deaths | Under_five_deaths | Adult_mortality | Alcohol_consumption | Hepatitis_B | Measles | BMI     | Polio   | Diphtheria | Incidents_HIV | GDP_per_capita | Population_mln | Thinness_ten_nineteen_years | Thinness_five_nine_years | Schooling | Economy_status | Life_expectancy |
|---|--------|---------------|-------------------|-----------------|---------------------|-------------|---------|---------|---------|------------|---------------|----------------|-----------------|-----------------------------|--------------------------|-----------|----------------|-----------------|
| **count**      | 179.0  | 179.000000     | 179.000000        | 179.000000      | 179.000000          | 179.000000  | 179.000000 | 179.000000 | 179.000000 | 179.000000  | 179.000000     | 179.000000      | 179.000000     | 179.000000             | 179.000000              | 179.000000 | 179.000000     | 179.000000      |
| **mean**       | 2007.5 | 30.363792      | 42.938268         | 192.251775      | 4.820882            | 84.292598   | 77.344972 | 25.032926 | 86.499651 | 86.271648   | 0.894288       | 11540.924930   | 36.675915      | 4.865852               | 4.899825               | 7.632123  | 0.793296       | 68.856075       |
| **std**        | 0.0    | 26.725485      | 42.916952         | 111.659044      | 3.914554            | 13.820223   | 17.315208 | 2.165490  | 13.581153 | 13.931532   | 2.311895       | 16893.054182   | 136.655286     | 4.111094               | 4.195663               | 3.126912  | 0.406077       | 9.197699        |
| **min**        | 2007.5 | 2.381250       | 3.000000          | 57.710313       | 0.000025            | 30.687500   | 16.250000 | 20.212500 | 35.750000 | 31.312500   | 0.010000       | 263.937500     | 0.085000       | 0.100000               | 0.100000               | 1.337500  | 0.000000       | 45.606250       |
| **25%**        | 2007.5 | 8.159375       | 9.775000          | 107.046906      | 1.317813            | 78.218750   | 64.000000 | 23.225000 | 80.531250 | 80.812500   | 0.080000       | 1409.906250    | 2.108125       | 1.756250               | 1.731250               | 4.946875  | 1.000000       | 62.303125       |
| **50%**        | 2007.5 | 19.368750      | 23.137500         | 164.432406      | 4.209375            | 88.000000   | 83.000000 | 25.650000 | 92.375000 | 92.062500   | 0.164375       | 4402.625000    | 7.660625       | 3.556250               | 3.718750               | 7.831250  | 1.000000       | 71.506250       |
| **75%**        | 2007.5 | 48.959375      | 68.321875         | 247.523922      | 7.843438            | 94.375000   | 92.250000 | 26.425000 | 96.062500 | 95.781250   | 0.516250       | 12037.781250   | 22.745313      | 7.165625               | 7.056250               | 10.365625 | 1.000000       | 74.937500       |
| **max**        | 2007.5 | 115.718750     | 178.725000        | 572.974312      | 15.100000           | 98.875000   | 99.000000 | 31.687500 | 98.937500 | 99.000000   | 18.164375      | 102972.687500  | 1321.239375    | 27.100000              | 27.943750              | 13.268750 | 1.000000       | 82.456250       |

> year 변수는 년도가 2007.5로 고정되어있기 때문에 eda컬럼에서 제외*



### 4. 데이터 전처리  

#### **데이터 결측값**
* 데이터 결측값은 `df.isnull().sum()`을 통해 확인해 본 결과 존재하지 않아서, 따로 처리를 하지 않았다.
#### **데이터 이상값**

##### **수치형 변수 이상값 확인**
![image](https://github.com/user-attachments/assets/183ef5d2-6b10-423e-8c45-5762438de53f)
* 수치형 변수의 이상치를 확인하기 위해 Boxplot으로 시각화 해본 결과 `Alcohol_consumption`, `Schooling`, `Life_expectancy`을 제외하고 사분위수를 기준으로 이상치가 존재하였다.
* 각 변수별 이상치는 변수의 특성을 분석하여 따로 처리하는 것이 좋을 것이라 판단하여 컬럼 별로 분석하여 이상치를 처리하였다.

##### **범주형 변수 이상값 확인**

| Country              | Count |
|----------------------|-------|
| Afghanistan          | 1     |
| Albania              | 1     |
| Algeria              | 1     |
| Angola               | 1     |
| Antigua and Barbuda  | 1     |
| ...                  | ...   |
| Venezuela, RB        | 1     |
| Vietnam              | 1     |
| Yemen, Rep.          | 1     |
| Zambia               | 1     |
| Zimbabwe             | 1     |

| Region                            | Count |
|-----------------------------------|-------|
| Africa                            | 51    |
| Asia                              | 27    |
| European Union                    | 27    |
| Central America and Caribbean     | 19    |
| Rest of Europe                    | 15    |
| ...                               | ...   |

> `value_counts`를 통해 범주형 변수의 이상치를 확인해 본 결과 모든 나라가 1개의 열로 들어가 있는 것을 확인하였다.
> 또한 대륙(지역)별로도 나라가 알맞게 들어가 있는 것을 확인하였다.

##### **컬럼별 이상치 분석**

**GDP와 인구수 이상치 분석**
![image](https://github.com/user-attachments/assets/ae54c2ac-4bb3-4fc7-b01f-7978f530544e)
* 산점도를 확인해 본 결과 지역별로 다른 경향을 보이는 것으로 파악돼 지역별로 나누어 각각 Z-SCORE를 게산한 후 Z-SCORE값이 3이 넘는 수치를 확인하였다.

  
![image](https://github.com/user-attachments/assets/e97aa5b2-401a-4701-af37-4de785d7bd7b)
<p float="left">
  <table border="1">
    <thead>
      <tr>
        <th>Region</th>
        <th>Country</th>
        <th>GDP_per_capita_Z</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Africa</td>
        <td>Equatorial Guinea</td>
        <td>3.308435</td>
      </tr>
      <tr>
        <td>Africa</td>
        <td>Libya</td>
        <td>3.011919</td>
      </tr>
      <tr>
        <td>Central America and Caribbean</td>
        <td>Bahamas, The</td>
        <td>3.263916</td>
      </tr>
      <tr>
        <td>Africa</td>
        <td>Seychelles</td>
        <td>3.368514</td>
      </tr>
      <tr>
        <td>European Union</td>
        <td>Luxembourg</td>
        <td>3.617869</td>
      </tr>
      <tr>
        <td>Asia</td>
        <td>Singapore</td>
        <td>3.341175</td>
      </tr>
    </tbody>
  </table>
</p>

<p float="left">
  <table border="1">
    <thead>
      <tr>
        <th>Region</th>
        <th>Country</th>
        <th>Population_mln_Z</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Africa</td>
        <td>Nigeria</td>
        <td>4.920200</td>
      </tr>
      <tr>
        <td>Asia</td>
        <td>India</td>
        <td>3.204249</td>
      </tr>
      <tr>
        <td>Rest of Europe</td>
        <td>Russian Federation</td>
        <td>3.201684</td>
      </tr>
      <tr>
        <td>South America</td>
        <td>Brazil</td>
        <td>3.046067</td>
      </tr>
      <tr>
        <td>Asia</td>
        <td>China</td>
        <td>3.608051</td>
      </tr>
      <tr>
        <td>European Union</td>
        <td>Germany</td>
        <td>3.029649</td>
      </tr>
    </tbody>
  </table>
</p>

* 경제적 특성과 국가 크기 차이에 따라 판단했을 때 이상치로 판단되는 값들이 그 지역의 특성상 자연스러운 값이라고 판단되어 분포상 Z-score가 3을 넘는 값을 이상치로 판단하지 않고 EDA를 진행하였다.
* 예) 인구 수의 경우 인도와 중국이 지역 평균에 비해 월등이 뛰는 것이 타당함.


### 5. 데이터 EDA (탐색적 데이터 분석)  
#### **5-1. 유아, 청소년 관련 변수와 기대수명간의 관계 EDA**  
**요소 간의 상관관계 파악**
![image](https://github.com/user-attachments/assets/97c5eb57-a0f3-4cd0-96dc-edb3ad8e855b)


![image](https://github.com/user-attachments/assets/ae33fb62-6506-443e-a71f-7b2e60086439)


![image](https://github.com/user-attachments/assets/0271f5ba-5a55-404e-b5f4-8e991f46b7d7)


<p float="left">
  <img src="[이미지_URL_1](https://github.com/user-attachments/assets/662869db-8056-48e2-beb6-7aae08b10a4d)" width="45%" />
  <img src="[이미지_URL_2](https://github.com/user-attachments/assets/832da906-63a5-458e-91d7-2207693fd180)" width="45%" />
</p>


#### **5-2. 건강 관련 변수와 기대수명간의 관계 EDA**  

![image](https://github.com/user-attachments/assets/70da295f-0021-435e-99f0-355edde6acfe)

![image](https://github.com/user-attachments/assets/4beca8a8-145c-405d-9dc7-f9405063b17b)

#### **5-3. 경제적 사회적 요인간의 관계 EDA**

**국가별 기대수명**
![image](https://github.com/user-attachments/assets/15aae3d8-cb64-491b-a3a7-09fc7565114f)
* 나라 별로 기대수명을 시각화 해본 결과 대륙(지역)별로 비슷한 기대수명을 공유하는 경향이 보여 대륙별로 추가 분석을 진행해보았다.

**대륙(지역)별 기대수명**
![image](https://github.com/user-attachments/assets/b20fc8f9-ab72-45c8-af2a-ec337b48823b)
* `아프리카(Africa)` 지역은 가장 낮은 기대수명을 보이며, 국가 간 편차가 큰 편이다.
* `오세아니아(Oceania)`, `유럽(Rest of Europe)`, `북아메리카(North America)`는 높은 기대수명을 공유하며, 분포가 좁고 국가 간 편차가 작다.
* `중남미 및 아시아 지역`은 중간 수준의 기대수명을 보이지만, 일부 국가는 더 높은 기대수명을 가지며 분포가 넓게 퍼져 있다.

**GDP, 인구수별 기대수명**
![image](https://github.com/user-attachments/assets/724f2ab2-0c06-47a8-b0aa-79bf22a3d319)
* GDP에 따른 기대수명 변화
    * GDP가 낮은 구간에서는 기대수명이 상대적으로 낮고 변동폭도 크다.
    * GDP가 증가할수록 기대수명이 뚜렷하게 상승하며, 변동폭이 감소한다.특히 20K 이상 구간에서는 기대수명이 75세 이상으로 안정화되며, GDP가 더 증가해도 큰 변화는 없다.
    * 회귀선을 기준으로 데이터가 고르게 분포하여 상관관계가 뚜렷함을 알 수 있다.

* 인구수에 따른 기대수명 변화
    * 인구가 적은 나라는 기대수의 분포가 넓고 국가 간 편차가 크다. 반대로 인구가 많은 나라는 기대수명이 상대적으로 좁은 범위에 걸쳐져 있다.
    * 로그 변환된 인구와 기대수명 간에 회귀선의 기울기가 수평에 가까워 뚜렷한 상관관계는 발견되지 않았다.

#### **5-4. 생활 수준 및 습관 관련 변수**



### 6. 최종 인사이트  


---

## 🌈 **팀원 한 줄 회고**  

| 이름      | 한 줄 회고                                                          |
|-----------|--------------------------------------------------------------------|
| 박유진     |   |
| 이다인     | |
| 이재혁     | |
| 최재동     | |
