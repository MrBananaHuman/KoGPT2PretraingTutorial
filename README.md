# KorGPT2Tutorial
Tutorial for pretraining and finetuning Korean GPT-2 model

Sample model download: https://drive.google.com/drive/folders/124Uux07pym2YaCeQKQWNhzhLNeIlLm7r?usp=sharing   
(100,000 sentences, 1 epoch)   

## 0. Setup
### Virtual Env (Optional)
```bash
python3 -m venv .venv
source .venv/bin/activate
```
### Install packages
```bash
pip install -r requirements.txt
```

## 1. Make vocab and tokenizer from corpus
```python make_tokenizer.py```

## 2. GPT-2 training from scratch   
if you want to train GPT-2 from existing model, add the argument '--init_model'   
```python pretrain_gpt2.py --do_train --do_eval --eval_data_file=pretrain_data/datas/sample_text.txt --model_type=gpt2 --train_data_file=pretrain_data/total_pretrain_data.txt --num_train_epochs=1```   

## 3. Text generation test
```python generation_text.py```

input: 이순신은 조선
-  이순신은 조선 시대 이순신은 무솔한 이순신의 모습을 생생하게 재현했다.
 이순신은 일제강점기 조선의 한 축을 책임지고 있다.
 임진왜란 당시 이순신은 무솔한 이순신을 살려내 이순신의 모습을 담은 전시회를 가졌다.
 이순신은 '역사'로서 이순신을 대표하는 이순신답게, 이순신은 일제강점기 조선 조선 조선 시대의 대표적인 작품 중 하나다.
 이순신은 조선의 역사와 전통을 담아내기 위해 선조들의 관심을 끌었고, 조선 시대 조선총독부에서 이순신이 보여준 이순신의 모습은 이순신과 이순신을 가장 가까이에서 볼 수 있는 대목이다.
 이순신은 1900년 전란 중인 조선총독부 경무국과 조선군사정관을 지냈다.
 이순신은 일제강점기 조선의 역사를 한 획을 그었다.
 이순신 시대 이순신은 조선총독부 경무국장으로 근무했다.
 그 동안 이순신은 조선총독부 경무국과 조선군의 역사를 다년간 지냈다.
 그 동안 이순신의 업적을 재현하기 위해 이순신의 발자취를


input: 밤하늘의 별
-  밤하늘의 별과 비슷한 것인데도 불구하고 하늘엔 태양이나 어두운 기운이 스며 있고, 눈이 하늘보다 높지만 그마저도 태양이나 어두운 색이었다. 빛의 별이나 태양의 별과 마찬가지로 하늘보다 훨씬 높고 밝은 별이 더 많았을 것이다. 하늘엔 태양이나 어두운 기운이 가득 고여 있고, 하늘이 더 밝게 빛났으며, 이 별을 관측하는 것도 하늘의 별과 같은 것이라고 생각했다. 그 별들은 태양을 처럼, 밝은 별들이 더 밝게 빛났었다. 그 별이 빛난 별과 달리 태양이 빛난 별이 더 더 밝게 빛났기 때문이다. 별의 별들은 하늘의 별과 별에 대해 별과 별 사이의 차이점을 구분하였다.


## 4. lyric finetuning and generation
Full data is not availabled but you can download sample model from Google drive link above   
```python lyric_finetuning.py```   
```python lyric_generation.py```   

input: 봄바람이 휘날리며
- 봄바람이 휘날리며//살며시 내게 속삭일 때 난 고백하지 못해//그대 날 보는 내 마음을//설레였던 그대 미소 속에 나를 녹여//달나라 그대와 마주앉아//함께한 꿈들 그대 꿈속에서도//함께해 우리 함께한//그 꿈을 찾아//그대라는걸 그대만이 알죠//사랑해요 그대가 그댄 나의 사랑을//늘 달 한 순간도 변함없죠//내 손을 잡던 따뜻한 바람에도//그대가 내 곁을 지켜줄 사람//내 곁을 지켜줄 사람//사랑합니다//그대와 그대 그대 그대 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘//늘 달 한 순간도 변함없죠//내 곁을 지켜줄 사람//사랑합니다//그대와 그대 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘//늘 달 한 순간도 변함없죠//내 곁을 지켜줄 사람//사랑합니다//그대와 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘//늘 달 한 순간도 변함없죠//내 곁을 지켜줄 사람//사랑합니다//그대와 그대죠//그대여야만 하는 시간//그대를 기다리는 이 맘
 
 
input: 비 내리는 등대에서
- 비 내리는 등대에서 내리면// 그 곳으로 날아가요// 나를 향해 가는 노래// 나의 노래// 내 노래를 부르죠// 널 사랑해 사랑해줘// 언제나 내 곁에서 함께 웃어요// 모든 걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대// 언제나 내 곁에서 함께 할 그대// 언제나 내 곁에서 함께 웃을 그 사람// 언제나 내 곁에서 함께 웃어요// 모든걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대// 언제나 내 곁에서 함께 웃어요// 모든 걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대// 언제나 내 곁에서 함께 웃어요// 모든걸 알아줄래요// 우리 함께 하는 이 노래를// 늘 내 곁에서 함께 웃어요// 모든걸 알아줄래요// 우리 함께 하는 이 노래를// 매일 나와 함께 할 그대
 
 
input: 좁고 좁은 저 문으로
- 좁고 좁은 저 문으로// 나를 둘러 싼// 날들은 매일 밤 새침 없이 문을 두드리네// 날 위한 이 밤// 아무도 모르게 날 밝혀주네// 우리 둘만 있어// 나의 작은 방 안에 가득// 가득// 너의 문을 두드리네// 나를 본 이 사람// 내 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준// 널 사랑하는 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어// 너의 마음을 들뜨게 하네// 아무도 모르게 날 밝혀주네// 날 바라보는 날 지켜준 나// 모든 게 너의 달과 같아// 네가 있어 내 곁에 있어

 
## 5. Paraphrasing finetuning
- https://github.com/MrBananaHuman/KoGPT2ForParaphrasing


## 6. Summary finetuning and generation    
```python summary_finetuning.py```   
```python summary_generation.py```   

input: \<science\>, LG유플러스는 미취학 아동 대상 IPTV·모바일 미디어 플랫폼 ‘U+아이들나라’를 활용한 국내 최초 AI 실험을 바탕으로 유아기 올바른 콘텐츠 시청 습관의 중요성을 알리는 공익 캠페인 영상을 공개했다고 11일 밝혔다.\n디지털 네이티브 세대 아이들의 미디어 노출 시기는 점차 빨라지고 있고, 최근 코로나19 상황으로 노출 시간 역시 늘어나고 있다.\nLG유플러스는 국내 최다 AI 특허를 보유한 솔트룩스와 함께 8주간 실험을 진행했다. 실제 사례자의 5세 아이를 3D 모델링 기술로 복제하고, 인공지능 음성합성 기술로 대화가 가능한 두 명의 AI 아이를 구현했다.

- LG유플러스, AI 음성합성 기술로 대화를 가능토록

input: \<social\>, 16일 코로나19 신규 확진자가 34명으로 집계됐다. 그중 국내 발생 사례는 21명이고 나머지 13명은 해외유입 사례다.\n질병관리본부 중앙방역대책본부는 이날 오전 0시 기준 코로나19 확진자가 전날 대비 34명 늘어난 1만2155명이라고 밝혔다. 국내 신규 감염 사례는 지난 10일 이후 40~50명선을 유지했으나 지난 14일부터 20명대로 내려왔다.\n국내 발생 사례를 지역별로 보면 서울 11명, 인천 2명, 경기 4명으로 수도권에서 17명이 나왔다. 그밖에 대전에서 3명, 경남에서 1명이 추가 확진됐다.\n13건의 해외 유입 사례의 경우 검역소에서 9명이 새로 확진을 받았다. 서울, 부산, 경기, 경남에서도 1명씩 신규 확진자가 나왔다.\n수도권의 경우 ‘국내 발생’과 ‘해외 유입’을 모두 합하면 19명의 신규 확진자가 나왔다.\n코로나19로 인한 사망자는 하루새 1명 늘어나 총 278명이다.\n완지로 격리 해제된 사람은 30명이 추가돼 총 1만760명으로 집계됐다. 격리 중인 이는 전날보다 3명 늘어난 1117명이다.

- 국내 사망자만 44명...기준 21명 늘어

input: \<economy\>, 코로나19 대유행으로 확산했던 재택근무와 개학 연기가 서서히 종료되면서 곤두박질쳤던 백화점 의류 매출도 반등하고 있다.\n14일 신세계백화점에 따르면 6월 남성·여성 패션 장르 매출이 전년 동기 대비 3.8% 증가했다. 지난 5월 매출이 전년 동기보다 13% 줄었던 '역신장'을 딛고 다시 성장세로 돌아선 것이다.\n백화점 의류 매출이 기사회생한 배경에는 '재택근무'와 '개학 연기'가 있다. 직장인과 학생들이 다시 외출을 시작하면서 닫혔던 지갑도 다시 열렸다.\n패션 장르별로 보면 지난 1일부터 11일까지 여성 패션 매출이 16.6% 성장했다. 남성 장르도 10% 매출이 늘었다. 특히 30대 직장이 많이 찾는 '컨템포러리 장르'는 매출이 무려 36.6% 급증했다.\n신세계백화점은 직장인 의류 성장세를 반영해 15일부터 남녀 의류를 최대 30% 할인하는 '시즌오프'를 진행한다. 대표 브랜드는 △맨온더분 △리스 △타미힐피거 △마담포라 △이새 등이다.\n신세계백화점 관계자는 \"전면적 개학과 함께 재택 근무가 줄어들면서 패션 수요가 점점 늘어나는 추세\"라며 \"백화점을 찾는 고객들이 안심하고 쇼핑할 수 있도록 쾌적하고 안전한 매장 조성에 힘쓸 것\"이라고 말했다.
 
- 주간 - 신세계백화점 7월 첫만금박자...19년만에 최대 폭(종합)

## 7. Question and answer generation
To train question and answer generator, KorQuAD v1.0 data will be used.    
Therefore, the fineturning requires preprocessing of training data.    
```cd qa_data```   
```python make_train_data.py```   

Generation consists of two steps.    
1. Obtain a candidate group that can be answer from context.     
2. The question for each answer is extracted.   
   
```python answer_finetuning.py```   
```python question_finetuning.py```   
```python qa_generation.py```   


input: 이순신은 조선 중기의 무신이었다. 본관은 덕수, 자는 여해, 시호는 충무였으며, 한성 출신이었다. 문반 가문 출신으로 1576년 무과에 급제하여 그 관직이 동구비보 권관, 훈련원 봉사, 발포진 수군만호, 조산보 만호, 전라좌도 수군절도사를 거쳐 정헌대부 삼도수군통제사에 이르렀다.   
    
- 이순신이 정헌대부 삼도수군통제사에 오른 해는?   ->       1576년   
이순신이 1576년 정헌대부 삼도수군통제사에 오른것은?     ->       참수   
이순신이 정헌대부 삼도수군통제사에 오른 연도는? ->       1576년   
이순신은 이순신을 조선 중기로 받들고 누구를 따라 유학했는가?    ->       천호   
   
input: 대한민국은 동아시아의 한반도 남부에 있는 민주공화국이다. 서쪽으로는 황해를 사이에 두고 중화인민공화국이, 동쪽으로는 동해를 사이에 두고 일본이 있으며 북쪽으로는 조선민주주의인민공화국과 맞닿아 있다. 수도는 서울특별시이고, 사실상 행정 수도는 세종특별자치시이다.   
   
- 국제법 규정상 대한민국의 영토 중 이름은 무엇인가?       ->      황해를 사이에 두고 중국   
동쪽에 가장 있는 국가는?        ->       일본   
수도는 어디인가?        ->       황해   
동아시아의 서계에 있는 국가는?  ->       대한민국의 한반도 남부에 있는 민주공화국   
국제적으로 밝혀진 두 유지에 대해 중화인민공화국이 어느 지역에 위치한가? ->      황해   

## 8. KorQuAD finetuning
This code can also be used to generate questions and answers from the content.  
```python korquad_finetuning.py```   
```python korquad_evaluation.py```  
```python qa_data/evaluate-v1.0.py qa_data/KorQuAD_v1.0_dev.json qa_data/korquad_result.json```    
   
Result is bad.. 😂   
{"exact_match": 14.132317284378248, "f1": 29.79123370568921}    

## 9. Simple chitchat finetuning (on going)   
Dataset from https://github.com/songys/Chatbot_data   

