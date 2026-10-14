이 폴더는 index.html이 사용하는 외부 라이브러리를 사이트에 직접 포함한 것입니다.
(외부 CDN이 변조되어도 토큰·조합원 명단이 유출되지 않도록, 그리고 파일이 바뀌면 브라우저가 실행을 거부하도록 무결성(SRI) 해시를 함께 지정했습니다.)

 xlsx.full.min.js   SheetJS xlsx 0.18.5 (Apache-2.0)   sha384-vtjasyidUo0kW94K5MXDXntzOJpQgBKXmE7e2Ga4LG0skTTLeBi97eFAXsqewJjw
 exceljs.min.js     ExcelJS 4.4.0 (MIT)                sha384-Pqp51FUN2/qzfxZxBCtF0stpc9ONI6MYZpVqmo8m20SoaQCzf+arZvACkLkirlPz

· index.html과 같은 위치에 vendor 폴더째로 올려야 합니다. 파일을 열어 수정하거나 이름을 바꾸면 안 됩니다(해시가 달라져 엑셀 기능이 멈춥니다).
· 라이브러리를 업데이트할 때는 새 파일의 sha384 해시를 다시 계산해 index.html의 integrity 값을 함께 바꿔야 합니다.
