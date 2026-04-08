<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<%@ page import="com.travel.dao.Member" %>
<%
    Member loginUser = (Member) session.getAttribute("loginUser");
%>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
<nav class="navbar navbar-expand-lg navbar-primary bg-primary">
  <div class="container">
    <a class="navbar-brand text-white fw-bold" href="MainController">Good Travel</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link text-white" href="index.jsp">홈</a></li>
        <li class="nav-item"><a class="nav-link text-white" href="ProductListController">상품</a></li>
        <% if (loginUser != null) { %>
          <li class="nav-item"><a class="nav-link text-white" href="ReservationListController">내 예약</a></li>
          <li class="nav-item"><a class="nav-link text-white" href="mypage.jsp">마이페이지</a></li>
          <li class="nav-item"><a class="nav-link text-white" href="logout">로그아웃</a></li>
        <% } else { %>
          <li class="nav-item"><a class="nav-link text-white" href="member/login.jsp">로그인</a></li>
          <li class="nav-item"><a class="nav-link text-white" href="member/joinForm.jsp">회원가입</a></li>
        <% } %>
      </ul>
    </div>
  </div>
</nav>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
