# 서울 편의점 브랜드 입지 분석 프로젝트
서울시 소상공인시장진흥공단에서 제공하는 상가업소정보 데이터를 바탕으로 7-Eleven과 GS25 편의점의 입지 점유율을 비교한 분석 프로젝트입니다. 2024년 10월 기준 데이터를 활용하여 브랜드별 점포 수와 서울 내 입지 분포를 시각적으로 분석하였습니다.


## 프로젝트 개요  

최근 **7-Eleven(코리아세븐)**의 실적 부진이 업계의 주목을 받고 있습니다. 관련 기사에 따르면:  
1. [**"세븐일레븐, 3년째 적자…재무 부담 '가중'"**](https://www.topdaily.kr/articles/98770)  
2. [**"코리아세븐, 불어난 적자에 실적 반등 총력전"**](https://www.datanews.co.kr/news/article.html?no=134453)  

기사에서는 **7-Eleven이 지속적인 적자로 어려움을 겪고 있으며, 시장 점유율 회복을 위해 다양한 노력을 기울이고 있다**고 전하고 있습니다. 이러한 상황에서, **7-Eleven의 입지 전략이 업계 1위인 GS25와 비교했을 때 어떤 차이를 보이는지 분석하는 것**은 실적 부진의 원인을 파악하고 개선 방향을 모색하는 데 중요한 단서를 제공할 수 있습니다.  

## 프로젝트의 목표  

이 프로젝트는 **서울 내 주요 편의점 브랜드인 GS25와 7-Eleven의 입지 분포를 비교 분석**하여, **7-Eleven이 시장 경쟁력을 높이기 위한 전략적 방향**을 도출하고자 진행되었습니다.  

### 구체적인 목표  
1. **서울 내 7-Eleven과 GS25 점포의 분포를 비교**해 두 브랜드의 입지 전략 차이를 시각적으로 분석합니다.  
2. **입지 차이가 소비자 접근성과 브랜드 선택에 미치는 영향을 추정**합니다.  
3. **7-Eleven의 입지 공백 지역을 파악**해 향후 점포 확장 전략에 대한 구체적인 인사이트를 제공합니다.  

이번 분석은 단순히 점포 수의 차이를 넘어, **서울에서 7-Eleven이 부족한 지역적 요인과 GS25의 성공적인 입지 전략**을 심층적으로 이해하려는 데 초점을 맞추고 있습니다. 이를 통해 **7-Eleven의 실적 개선을 위한 데이터 기반의 구체적인 전략 수립에 도움을 주는 것이 목표**입니다.


## 사용 데이터 
- **소상공인시장진흥공단 상가업소정보**  
  데이터 출처:[ https://www.data.go.kr/dataset/15012005/fileData.do](https://www.data.go.kr/dataset/15012005/fileData.do)

## 데이터 전처리 및 시각화  
1. **데이터 로드 및 확인**  
   <img width="1099" alt="image" src="https://github.com/user-attachments/assets/67c470c7-5a61-4690-a49c-5f22c61a6ae9" />

2. **브랜드명 통일**  
   편의점 지점마다 이름이 다르기 때문에 '브랜드명'이라는 새로운 컬럼을 추가하여 '세븐일레븐'과 'GS25'로 통일
   <img width="613" alt="image" src="https://github.com/user-attachments/assets/a4b3cc4c-828f-4bef-b014-7d80403b4e97" />

4. **경도 및 위도 기반 시각화**  
   위도와 경도의 데이터 타입을 float으로 수정 뒤 scatterplot으로 시각화   
   <img width="516" alt="image" src="https://github.com/user-attachments/assets/bf02584f-346d-49a2-9235-1c6090ee7552" />

6. **지도 기반 시각화**  
   folium을 사용해 서울 지도에서 각 편의점의 위치를 시각적으로 확인하며 브랜드별 입지 차이를 분석
   <img width="705" alt="image" src="https://github.com/user-attachments/assets/54ae34c8-12f5-4a7b-90df-8af9553c83a6" />
   <img width="1190" alt="image" src="https://github.com/user-attachments/assets/36352c3e-82d6-4f35-aa95-ad86d3e0ea56" />



## 분석 결과  
- GS25가 7-Eleven에 비해 서울 내에서 점포 수가 약 2.25배 많다는 결과가 도출되었습니다.
- 서울 남쪽의 주요 지역(반포동, 방배동, 사당동, 봉천동, 상도동)에서는 7-Eleven 점포가 전혀 없는 반면, GS25는 광범위하게 분포되어 있었습니다.
- 송파구와 강서구에서도 GS25가 훨씬 더 많은 점포 수를 보였으며, 7-Eleven은 거의 존재하지 않았습니다.

## 시각화 결과
- **Scatter Plot 시각화**  
  <img width="588" alt="image" src="https://github.com/user-attachments/assets/621c8549-d4d9-46c6-9bf3-db00862ec3ab" />

- **지도 기반 시각화**  
  <img width="988" alt="image" src="https://github.com/user-attachments/assets/050925f3-7437-4279-a5b7-f00ee56c7c68" />
  <img width="971" alt="image" src="https://github.com/user-attachments/assets/aacae8d8-ec77-4924-bf74-f8f1ac3df52d" />


## 결론  
향후 편의점 입지 전략을 수립할 때 **소비자 접근성**과 **지역별 브랜드 선호도**를 고려하는 것이 중요합니다. 본 프로젝트는 소비자들의 브랜드 선택 행동과 입지 전략을 이해하는 데 있어 다음과 같은 주요 정보를 제공합니다:

### 1. 소비자 접근성  
GS25는 서울 남쪽과 주요 지역에 점포가 고르게 분포되어 있으며, 이는 소비자들이 쉽게 접근할 수 있는 위치에 전략적으로 입지하고 있음을 보여줍니다. 이러한 접근성은 소비자들이 브랜드에 자주 노출되고, 구매 행동에 긍정적인 영향을 미칠 가능성을 시사합니다.  
반면, 7-Eleven은 송파구, 강서구를 포함한 서울 남쪽 주요 지역에서 점포 수가 현저히 적어 소비자 접근성이 제한적입니다.  
**→ 따라서, 서울 남쪽과 같은 입지 공백 지역에 전략적으로 점포를 확장한다면 브랜드 인지도를 높이고, 매출 증대에 기여할 가능성이 큽니다.**

### 2. 지역별 브랜드 선호도  
GS25가 높은 점유율을 차지하는 것은 해당 지역에서 **브랜드 선호도가 높고, 브랜드 이미지나 소비자 만족도가 상대적으로 우수**하다는 것을 의미합니다.  
반면, 7-Eleven은 특정 지역에서 점포 수 부족으로 인해 브랜드 인지도와 소비자 충성도가 낮아질 위험이 있습니다.  
**→ GS25의 점유율이 높은 지역에서 소비자 선호도를 분석하고, 7-Eleven이 경쟁에서 밀린 요인을 파악해 해당 지역에 적합한 전략을 수립하는 것이 중요합니다.**

### 3. 경쟁 브랜드 입지 패턴 분석  
GS25와 7-Eleven의 입지 차이는 **경쟁 브랜드의 입지 전략을 이해하고, 대응 방안을 마련하는 데 중요한 통찰**을 제공합니다.  
GS25가 우위를 점하고 있는 지역에서는 고객 접근성이 용이하며, 이와 유사한 입지 전략을 적용하면 소비자 반응을 극대화할 수 있습니다.  
**→ 7-Eleven은 부족한 지역에 점포를 늘리고, 소비자 접근성을 높이는 동시에 브랜드 경쟁력을 강화하는 전략이 필요합니다.**

결론적으로, **소비자 접근성과 지역별 브랜드 선호도를 기반으로 한 데이터 분석**은 편의점의 입지 전략 수립에 있어 필수적인 요소입니다.  
**이를 통해 소비자 행동을 이해하고, 7-Eleven의 현재 실적 부진을 극복할 효과적인 방향을 제시**할 수 있습니다. 결과적으로, 보다 경쟁력 있는 입지 전략이 브랜드 강화와 시장 점유율 확대에 기여할 것입니다.
