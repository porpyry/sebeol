# 커스텀 신세벌식

신세벌식 2015 베이스의 커스텀 배열

### 특징
- 숫자열, 시프트를 사용하지 않는다. (신세벌식 특징)
- 오른손 연타가 없다.

<p>&nbsp;</p>

### 신세벌식 2015 배열과 차이점
- ㅁ받침과 ㅅ받침 교환
- ㅂ받침과 ㅇ받침 교환
- 쌍자음을 연타가 아닌 두 손가락으로 입력
- 이중모음 입력을 위한 ㅗ와 ㅜ의 위치 변경
- 겹받침 입력시 사소한 편의 기능 추가

<p>&nbsp;</p>

## Windows 사용법
날개셋 제어판에서 [sebeol.set](sebeol.set)를 가져오기합니다.

<p>&nbsp;</p>

## Linux Doom Emacs 사용법
[hangul-sebeol.el](hangul-sebeol.el)을 `.doom.d/local`에 저장하고 `.doom.d/config.el`에 다음을 추가합니다.
```elisp
(load! "local/hangul-sebeol")
(setq default-input-method "korean-hangul-sebeol")
(global-set-key (kbd "<Hangul>") 'toggle-input-method)
```
<p>&nbsp;</p>

시스템 입력기를 통해 한영 전환을 사용하고 있다면 다음을 통해 Emacs 내에서 시스템 한영 전환을 비활성화하여 충돌을 방지합니다.
1. `~/.Xresources`에 `Emacs*useXIM: false` 추가
2. `xrdb ~/.Xresources` 명령어 실행

<p>&nbsp;</p>

## 배열

### 시프트
```
ㅎ  ㅅ  ㅂ  ㅈ  ㅍ    □   □   □   □   ;
 ㅆ  ㄴ  ㄹ  ㅌ  ㄷ    ※   '   "   ·   :   /
  ㅇ  ㄱ  ㅁ  ㅊ  ㅋ   〈    〉   <   >   ?
```
(특수문자는 자주 사용하는 것들로 설정하세요)

### 기본
```
ㅒ  ㅖ  ㅕ  ㅐ  ㅓ    ㄹ  ㄷ  ㅁ  ㅊ  ㅍ
 ㅑ  ㅢ  ㅣ  ㅏ  ㅡ    ㄴ  ㅇ  ㄱ  ㅈ  ㅂ  ㅌ
  ㅠ  ㅛ  ㅔ  ㅗ  ㅜ    ㅅ  ㅎ   ,  .  ㅋ
```

<p>&nbsp;</p>

## 겹자모

### 쌍자음
- ㄱ + ㅇ = ㄲ
- ㄷ + ㅁ = ㄸ
- ㅂ + ㅈ = ㅃ
- ㅅ + ㄱ = ㅆ
- ㅈ + ㄱ = ㅉ

### 이중모음
- ㅂ, ㅎ = ㅗ
- ㅊ, ㄷ = ㅜ

### 겹받침
- ㄱ + ㅇ = ㄲ
- ㄴ + ㅆ = ㄶ
- ㄹ + ㅆ = ㅀ

<p>&nbsp;</p>

## 참고
- [날개셋 한글 입력기](http://moogi.new21.org/prg4.html)
- [이맥스 신세벌식 P2 구현](https://github.com/demokritos/hangul-s3p2)
