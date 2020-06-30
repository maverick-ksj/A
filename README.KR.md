<p align="center">
  <img src="./doc/thumbnail/thumbnail-black.png" alt="thumbnail">
</p>

![[GitHub release (latest SemVer)](https://github.com/maverick-ksj/pill-tong/releases)](https://img.shields.io/github/v/release/maverick-ksj/pill-tong)
![[GitHub tag (latest by date)](https://github.com/maverick-ksj/pill-tong/tags)](https://img.shields.io/github/v/tag/maverick-ksj/pill-tong)
![[LICENSE](https://github.com/maverick-ksj/pill-tong/blob/master/LICENSE)](https://img.shields.io/github/license/maverick-ksj/pill-tong)
[![Known Vulnerabilities](https://snyk.io/test/github/maverick-ksj/pill-tong/badge.svg)](https://snyk.io/test/github/maverick-ksj/pill-tong)

[English](./README.md) | Korean

**Pill-Tong** 은 NodeJS로 작성되었으며, 사용자가 원하는 방식으로 HTTP 요청을 *필터링* 할 수 있도록 고안된 [Reverse Proxy](https://en.wikipedia.org/wiki/Reverse_proxy) 서버입니다.

사용 방법은 간단합니다. (1) [pill-tong](https://www.npmjs.com/package/pill-tong) NPM 모듈을 설치하고 (2) 사용할 Middleware 필터를 설정한 다음 (3) `pilltong` 명령을 입력해 실행하기만 하면 됩니다.

현재 제공되는 필터는 다음과 같습니다 :

* [xss](https://github.com/maverick-ksj/pill-tong-xss-filter)
* [sqli](https://github.com/maverick-ksj/pill-tong-sqli-filter)

이를 통해 HTTP 요청에 대해 필터링을 적용할 수 있게 됩니다.

## 시작하기

### 1\. npm을 통해 pill-tong 모듈 설치

```sh
npm install pill-tong -g
```

### 2\. pill-tong 서비스 생성

```sh
# create a new pill-tong Service
pilltong --create my-proxy-server

# change into the created directory
cd my-proxy-server
```

### 3\. pill-tong 프록시 서버 시작

```sh
pilltong
```

## 옵션

```sh
--create <path> # 서비스 생성 (argument required)
--conf <path> # 설정 파일 위치 지정 (default: ./pill-tong.yml)
--noHello <boolean> # 시작 메시지 출력 여부 (default: false)
```

## 라이센스

Pill-Tong은 [MIT License](./LICENSE)를 따릅니다.