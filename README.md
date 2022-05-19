# 커스텀 신세벌식

## 특징
- 숫자열, 시프트를 사용하지 않는다. (신세벌식)
- 오른손 연타가 없다.

<p>&nbsp;</p>

## 사용법 (Windows)
날개셋 제어판에서 [sebeol.set](sebeol.set)를 가져오기합니다.

<p>&nbsp;</p>

## 사용법 (Doom Emacs)
[hangul-sebeol.el](hangul-sebeol.el)을 `.doom.d/local`에 저장하고 `.doom.d/config.el`에 다음을 추가합니다.
```elisp
(load! "local/hangul-sebeol")
(setq default-input-method "korean-hangul-sebeol")
(global-set-key (kbd "<Hangul>") 'toggle-input-method)
```

<p>&nbsp;</p>

## 배열

### 시프트
```
ㅎ  ㅅ  ㅂ  ㅈ  ㅍ    ←   ↓   ↑   →   ;
 ㅆ  ㄴ  ㄹ  ㅌ  ㄷ    ※   '   "   ·   :   /
  ㅇ  ㄱ  ㅁ  ㅊ  ㅋ   〈    〉   <   >   ?
```

### 기본
```
ㅒ  ㅖ  ㅕ  ㅐ  ㅓ    ㄹ  ㄷ  ㅁ  ㅊ  ㅍ
 ㅑ  ㅢ  ㅣ  ㅏ  ㅡ    ㄴ  ㅇ  ㄱ  ㅈ  ㅂ  ㅌ
  ㅠ  ㅛ  ㅔ  ㅗ  ㅜ    ㅅ  ㅎ   ,  .  ㅋ
```

<p>&nbsp;</p>

## 겹자모

### 초성
- ㄱ + ㅇ = ㄲ
- ㄷ + ㅁ = ㄸ
- ㅂ + ㅈ = ㅃ
- ㅅ + ㄱ = ㅆ
- ㅈ + ㄱ = ㅉ

### 중성
- ㅂ, ㅎ = ㅗ
- ㅊ, ㄷ = ㅜ

### 종성
- ㄱ + ㅇ = ㄲ
- ㄴ + ㅆ = ㄶ
- ㄹ + ㅆ = ㅀ

<p>&nbsp;</p>

## 참고
- [날개셋 한글 입력기](http://moogi.new21.org/prg4.html)
- [이맥스 신세벌식 P2 구현](https://github.com/demokritos/hangul-s3p2)
