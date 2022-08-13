---
title: Reflect.preventExtensions()
slug: Web/JavaScript/Reference/Global_Objects/Reflect/preventExtensions
tags:
  - ECMAScript 2015
  - JavaScript
  - Method
  - Reference
  - Reflect
translation_of: Web/JavaScript/Reference/Global_Objects/Reflect/preventExtensions
---
<div>{{JSRef}}</div>

<p><code><strong>Reflect.preventExtensions()</strong></code> 정적 메서드는 새로운 속성을 객체에 추가하지 못하도록 완전히 막습니다. 즉, 미래의 객체 확장을 막습니다. {{jsxref("Object.preventExtensions()")}}와 유사하지만 <a href="#object.preventextensions_와의_차이점">차이점</a>도 있습니다.</p>


<div>{{EmbedInteractiveExample("pages/js/reflect-preventextensions.html")}}</div>



<h2 id="구문">구문</h2>

<pre class="syntaxbox">Reflect.preventExtensions(<em>target</em>)
</pre>

<h3 id="매개변수">매개변수</h3>

<dl>
 <dt><code>target</code></dt>
 <dd>확장을 방지할 대상 객체.</dd>
</dl>

<h3 id="반환_값">반환 값</h3>

<p>대상의 확장을 성공적으로 방지했는지 나타내는 {{jsxref("Boolean")}}.</p>

<h3 id="예외">예외</h3>

<p><code>target</code>이 {{jsxref("Object")}}가 아니면 {{jsxref("TypeError")}}.</p>

<h2 id="설명">설명</h2>

<p><code>Reflect.preventExtensions()</code> 메서드는 새로운 속성을 객체에 추가하지 못하도록 완전히 막습니다. 즉, 미래의 객체 확장을 막습니다. {{jsxref("Object.preventExtensions()")}}와 유사합니다.</p>

<h2 id="예제">예제</h2>

<h3 id="Reflect.preventExtensions()_사용하기"><code>Reflect.preventExtensions()</code> 사용하기</h3>

<p>{{jsxref("Object.preventExtensions()")}}도 참고하세요.</p>

<pre class="brush: js">// 객체는 기본적으로 확장 가능
var empty = {};
Reflect.isExtensible(empty); // === true

// ...하지만 바꿀 수 있음
Reflect.preventExtensions(empty);
Reflect.isExtensible(empty); // === false
</pre>

<h3 id="Object.preventExtensions()와의_차이점"><code>Object.preventExtensions()</code>와의 차이점</h3>

<p><code>Reflect.preventExtensions()</code>는 첫 번째 매개변수가 {{glossary("Primitive", "원시값")}}이면 {{jsxref("TypeError")}}를 던집니다. 반면 {{jsxref("Object.preventExtensions()")}}는 우선 객체로 변환을 시도합니다.</p>

<pre class="brush: js">Reflect.preventExtensions(1);
// TypeError: 1 is not an object

Object.preventExtensions(1);
// 1
</pre>

<h2 id="Specifications">명세</h2>

{{Specifications}}

<h2 id="브라우저_호환성">브라우저 호환성</h2>

<p>{{Compat("javascript.builtins.Reflect.preventExtensions")}}</p>

<h2 id="같이_보기">같이 보기</h2>

<ul>
 <li>{{jsxref("Reflect")}}</li>
 <li>{{jsxref("Object.isExtensible()")}}</li>
</ul>