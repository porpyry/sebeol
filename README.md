# 커스텀 세벌식

갬성으로 개조한 세벌식 세팅 ([신세벌식 2015](https://cafe.daum.net/3bulsik/JMKX/64) 베이스)

### 특징
- 숫자열, 시프트를 사용하지 않는다.
- 쌍자음을 두 손가락으로 입력한다.

###  변경점
- ㅅ받침, ㅁ받침 교환
- ㅂ받침, ㅇ받침 교환
- 조합용 모음(ㅗ, ㅜ) 위치 변경

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

## 겹자모

### 쌍자음
- ㄱ + ㅇ = ㄲ
- ㄷ + ㅁ = ㄸ
- ㅂ + ㅈ = ㅃ
- ㅅ + ㄱ = ㅆ
- ㅈ + ㄱ = ㅉ

### 조합용 모음
- ㅂ, ㅎ = ㅗ
- ㅊ, ㄷ = ㅜ

### 겹받침
- ㄱ + ㅇ = ㄲ
- ㄴ + ㅆ = ㄶ
- ㄹ + ㅆ = ㅀ

## Windows
날개셋 제어판에서 [sebeol.set](sebeol.set)를 가져오기합니다.

## Doom Emacs

### 설치
[hangul-sebeol.el](hangul-sebeol.el)을 `.doom.d/local`에 저장하고 `.doom.d/config.el`에 다음을 추가합니다.
```elisp
(load! "local/hangul-sebeol")
(setq default-input-method "korean-hangul-sebeol")
(global-set-key (kbd "<Hangul>") 'toggle-input-method)
```

### (Linux) 시스템 한영 전환 비활성화
1. `~/.Xresources`에 `Emacs*useXIM: false` 추가
2. `xrdb ~/.Xresources` 명령어 실행

## 참고
- [날개셋 한글 입력기](http://moogi.new21.org/prg4.html)
- [이맥스 신세벌식 P2 구현](https://github.com/demokritos/hangul-s3p2)
