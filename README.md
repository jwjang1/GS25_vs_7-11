# 서울 편의점 브랜드 입지 분석 프로젝트
서울 내에서 7-Eleven과 GS25의 입지는 상당히 차이가 크며, GS25가 서울 남쪽과 일부 주요 지역에서 압도적으로 많은 점포 수를 보이고 있습니다. 이는 소비자 선호도 및 접근성 측면에서 브랜드별 차이를 잘 보여주며, 향후 편의점 입지 전략 수립에 있어 중요한 정보를 제공합니다.

## 프로젝트 개요  
서울시 소상공인시장진흥공단에서 제공하는 상가업소정보 데이터를 바탕으로 7-Eleven과 GS25 편의점의 입지 점유율을 비교한 분석 프로젝트입니다. 2024년 10월 기준 데이터를 활용하여 브랜드별 점포 수와 서울 내 입지 분포를 시각적으로 분석하였습니다.

## 데이터 출처  
- **소상공인시장진흥공단 상가업소정보**  
  데이터 출처:[ https://www.data.go.kr/dataset/15012005/fileData.do](https://www.data.go.kr/dataset/15012005/fileData.do)

## 데이터 처리 및 전처리 과정  
1. **데이터 로드 및 확인**  
   소상공인시장진흥공단에서 제공하는 편의점 데이터는 상가업소정보로, 2024년 10월 기준 데이터를 활용했습니다.

2. **브랜드명 통일**  
   편의점 지점 이름이 다르기 때문에 '브랜드명'이라는 새로운 컬럼을 추가하여 '세븐일레븐'과 'GS25'로 통일했습니다.

3. **경도 및 위도 기반 시각화**  
   pandas와 seaborn을 활용해 `sns.scatterplot(data=df_711, x='경도', y='위도', hue="브랜드명")`을 통해 브랜드별 서울 내 분포를 시각화했습니다.

4. **지도 기반 시각화**  
   folium을 사용해 서울 지도에서 각 편의점의 위치를 시각적으로 확인하며 브랜드별 입지 차이를 분석했습니다.

## 분석 결과  
- GS25가 7-Eleven에 비해 서울 내에서 점포 수가 약 2.25배 많다는 결과가 도출되었습니다.
- 서울 남쪽의 주요 지역(반포동, 방배동, 사당동, 봉천동, 상도동)에서는 7-Eleven 점포가 전혀 없는 반면, GS25는 광범위하게 분포되어 있었습니다.
- 송파구와 강서구에서도 GS25가 훨씬 더 많은 점포 수를 보였으며, 7-Eleven은 거의 존재하지 않았습니다.

## 시각화 결과
- **Scatter Plot 시각화**  
  ![Scatter Plot](여기에 scatterplot 이미지 스크린샷 위치)
  
- **지도 기반 시각화**  
  ![Map Visualization](여기에 지도 시각화 이미지 스크린샷 위치)

## 결론  

