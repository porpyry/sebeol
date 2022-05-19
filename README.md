# 커스텀 신세벌식

장점
1. 숫자행을 사용하지 않음
2. 시프트를 사용하지 않음
3. 반복 입력이 거의 없음

사용방법
- Windows: 날개셋 제어판에서 [sebeol.set](sebeol.set) 파일을 가져오기합니다.
- Linux Emacs
    - 가져오기: [hangul-sebeol.el](hangul-sebeol.el) 파일을 Emacs의 `load-path` 위치에 저장하고 `init.el` 파일에 `(require 'hangul-sebeol)`를 추가합니다.
    - Doom Emacs: 파일을 `.doom.d/local` 위치에 저장하고 `.doom.d/config.el` 파일에 `(load! "local/hangul-sebeol")`를 추가합니다.
    - 적용: `(setq default-input-method "korean-hangul-sebeol")` `(global-set-key (kbd "<Hangul>") 'toggle-input-method)`





## 배열

Shift (중간의 □에는 특수문자를 자유롭게 배치)
```
ㅎ  ㅅ  ㅂ  ㅈ  ㅍ    □   □   □   □   ;
 ㅆ  ㄴ  ㄹ  ㅌ  ㄷ    □   '   "   ·   :   /
  ㅇ  ㄱ  ㅁ  ㅊ  ㅋ    □   □   <   >   ?
```

기본
```
ㅒ  ㅖ  ㅕ  ㅐ  ㅓ    ㄹ  ㄷ  ㅁ  ㅊ  ㅍ
 ㅑ  ㅢ  ㅣ  ㅏ  ㅡ    ㄴ  ㅇ  ㄱ  ㅈ  ㅂ  ㅌ
  ㅠ  ㅛ  ㅔ  ㅗ  ㅜ    ㅅ  ㅎ   ,  .  ㅋ
```





## 겹자모

초성
- ㄱ + ㅇ = ㄲ
- ㄷ + ㅁ = ㄸ
- ㅂ + ㅈ = ㅃ
- ㅅ + ㄱ = ㅆ
- ㅈ + ㄱ = ㅉ

중성
- ㅂ, ㅎ = ㅗ
- ㅊ, ㄷ = ㅜ

종성
- ㄱ + ㅇ = ㄲ
- ㄴ + ㅆ = ㄶ
- ㄹ + ㅆ = ㅀ





## 참고
- [날개셋 한글 입력기](http://moogi.new21.org/prg4.html)
- [이맥스 신세벌식 P2 구현](https://github.com/demokritos/hangul-s3p2)
