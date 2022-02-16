## [Servlet Filter] 서블릿 필터
* Client로 부터 Server로 요청이 들어오기 전, Server에서 Client로 나가기 전에 서블릿을 거쳐서 필터링 하는 것을 서블릿 필터
* 사용자 인증이나 로깅과 같은 기능들은 모든 서블릿이나 JSP가 공통적으로 필요

1. 인증(사용자 인증) 필터   
2. 로깅 및 감시(Audit) 필터   
3. 이미지 변환 및 데이터 압축 필터   
4. 암호화 필터   
5. XML 컨텐츠를 변형하는 XSLT 필터   
6. URL 및 기타 정보들을 캐싱하는 필터   

~~~
public void doFilter(ServletRequest request, ServletResponse response, FilterChain chain) throws IOException, ServletException {
	// 들어오기 전
	chain.doFilter(request, response);
	// 나가기 전
}
~~~
