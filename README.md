# 쇼핑 추천 백엔드 시스템

## 프로젝트 소개
사용자 자연어 입력을 기반으로 추천 조건을 추출하고, 네이버 쇼핑 API를 통해 상품을 조회하는 백엔드 시스템입니다.  
AI는 조건 추출만 수행하고, 추천 판단은 정책 기반 로직으로 처리하도록 설계했습니다.

---

## 기술 스택
- Java
- Spring Boot
- JPA (Hibernate)
- MySQL
- OpenAI API
- Naver Shopping API

---

## 담당 역할
- Naver Shopping API 연동 및 검색 로직 구현
- RecommendationCriteria 기반 검색 파라미터 변환 설계
- NaverClient 인터페이스 및 Fake/Real 구조 설계
- RestTemplate 기반 외부 API 통신 구현
- 프로파일 기반 외부 API 분리 적용

---

## 주요 기능
- 자연어 → 추천 조건 변환
- 조건 기반 상품 검색
- 정책 기반 추천 결과 판단
- 결과 상태 분류 (RECOMMEND, REQUERY, INVALID)

---

## 트러블슈팅

### 외부 API 의존성 문제
- 문제: API 호출에 따라 테스트 불안정
- 해결: Fake Client 도입으로 테스트 가능 구조 설계

### AI 결과 불안정 문제
- 문제: 추천 결과 일관성 부족
- 해결: 추천 판단을 정책 로직으로 분리

### 검색 결과 품질 문제
- 문제: 조건 반영 부족
- 해결: 조건 기반 필터링 구조 설계

---

## 실행 방법
1. application.yml 설정
2. 프로젝트 실행 (Spring Boot)
3. Swagger를 통해 API 테스트
