# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 전재영
- 리뷰어 : 임현석

# PRT(Peer Review Template)
- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 
    퀘스트 문제 요구조건 등을 지칭
1. 인물모드 사진을 성공적으로 제작하였다.	[o]
2. 제작한 인물모드 사진들에서 나타나는 문제점을 정확히 지적하였다.	[o]
3. 인물모드 사진의 문제점을 개선할 수 있는 솔루션을 적절히 제시하였다.    [o]  
    
- [O]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
    - 주석을 보고 코드 이해가 잘 되었는지 확인
```python
# 배경 이미지의 크기를 가져옵니다.
height_bg, width_bg = img_back.shape[:2]

# 타겟 이미지의 크기를 가져옵니다. (이전에 이미 불러왔던 img_sheep에서)
height, width = img_sheep.shape[:2]

# 배경 이미지를 타겟 이미지의 크기에 맞게 크롭합니다.
# 중앙에서부터 크롭을 시작합니다.
start_x = (width_bg - width) // 2
start_y = (height_bg - height) // 2
end_x = start_x + width
end_y = start_y + height

# 실제로 크롭을 수행합니다.
cropped_background2 = img_back[start_y:end_y, start_x:end_x]

# 결과를 확인합니다.
plt.figure(figsize=(12, 6))
plt.subplot(1, 2, 1)
plt.title("Original Background")
plt.imshow(cv2.cvtColor(img_back, cv2.COLOR_BGR2RGB))
plt.axis('off')

plt.subplot(1, 2, 2)
plt.title("Cropped Background")
plt.imshow(cv2.cvtColor(cropped_background, cv2.COLOR_BGR2RGB))
plt.axis('off')

plt.show()
```
        
- [O]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 실험이 기록되어 있는지 확인
  
```python
# 가상의 img_concat1 이미지를 저장할 경로를 지정합니다.
# 실제 코드에서는 이미 생성된 img_concat1 이미지를 이용하게 됩니다.
img_concat1_save_path = '/aiffel/outfocus.jpg'

# 이미지를 저장합니다.
try:
    cv2.imwrite(img_concat1_save_path, img_concat1)
    print(f"Image saved at {img_concat1_save_path}")
except Exception as e:
    print(f"An error occurred: {e}")


# 저장된 이미지 파일의 경로를 반환합니다.
img_concat1_save_path
```
- [O]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
   
        
- [O]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 하드코딩을 하지않고 함수화, 모듈화가 가능한 부분은 함수를 만들거나 클래스로 짰는지
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화했는지
     

# 참고 링크 및 코드 개선
    - 단어 집합에서 희귀 단어를 제외시킬 경우의 단어 집합의 크기 값만 수정하면 학습하면 될것 같습니다!
     (단어 집합의 크기 제한 : 단어 집합의 크기 - 등장빈도 N번 이하인 희귀 단어의 수)

