---
title: Number.NEGATIVE_INFINITY
slug: Web/JavaScript/Reference/Global_Objects/Number/NEGATIVE_INFINITY
tags:
  - JavaScript
  - Number
  - Property
  - Reference
translation_of: Web/JavaScript/Reference/Global_Objects/Number/NEGATIVE_INFINITY
---
<div>{{JSRef}}</div>

<p><strong><code>Number.NEGATIVE_INFINITY</code></strong> 속성은 음의 무한대를 나타냅니다.</p>

<div>{{EmbedInteractiveExample("pages/js/number-negative-infinity.html")}}</div>



<div>{{js_property_attributes(0, 0, 0)}}</div>

<h2 id="설명">설명</h2>

<p><code>Number.NEGATIVE_INFINITY</code>의 값은 전역 객체 {{jsxref("Infinity")}} 속성의 부호를 바꾼 값과 동일합니다.</p>

<p><code>NEGATIVE_INFINITY</code>는 수학에서의 무한대와 약간 다릅니다.</p>

<ul>
 <li>{{jsxref("Number.POSITIVE_INFINITY", "POSITIVE_INFINITY")}}를 포함한 아무 양의 수와 <code>NEGATIVE_INFINITY</code>를 곱한 결과는 <code>NEGATIVE_INFINITY</code>입니다.</li>
 <li><code>NEGATIVE_INFINITY</code>를 포함한 아무 음의 수와 <code>NEGATIVE_INFINITY</code>를 곱한 결과는 {{jsxref("Number.POSITIVE_INFINITY", "POSITIVE_INFINITY")}}입니다.</li>
 <li>아무 양의 수를 <code>NEGATIVE_INFINITY</code>로 나눈 결과는 음의 부호를 가진 0입니다.</li>
 <li>아무 음의 수를 <code>NEGATIVE_INFINITY</code>로 나눈 결과는 0입니다.</li>
 <li>0을 <code>NEGATIVE_INFINITY</code>로 나눈 결과는 {{jsxref("NaN")}}입니다.</li>
 <li>{{jsxref("NaN")}}에 <code>NEGATIVE_INFINITY</code>를 곱한 결과는 {{jsxref("NaN")}}입니다.</li>
 <li><code>NEGATIVE_INFINITY</code>를, <code>NEGATIVE_INFINITY</code>를 제외한 아무 음의 수로 나눈 결과는 {{jsxref("Number.POSITIVE_INFINITY", "POSITIVE_INFINITY")}}입니다.</li>
 <li><code>NEGATIVE_INFINITY</code>를, {{jsxref("Number.POSITIVE_INFINITY", "POSITIVE_INFINITY")}}를 제외한 아무 양의 수로 나눈 결과는 <code>NEGATIVE_INFINITY</code>입니다.</li>
 <li><code>NEGATIVE_INFINITY</code>를 <code>NEGATIVE_INFINITY</code> 또는 {{jsxref("Number.POSITIVE_INFINITY", "POSITIVE_INFINITY")}}로 나눈 결과는 {{jsxref("NaN")}}입니다.</li>
</ul>

<p><code>Number.NEGATIVE_INFINITY</code>를 사용해 성공 시 유한수를 반환하는 식의 결과를 판별할 수 있습니다. 그러나 이런 경우 {{jsxref("isFinite", "isFinite()")}}를 사용하는 편이 더 적합합니다.</p>

<p><code>NEGATIVE_INFINITY</code>는 {{jsxref("Number")}}의 정적 속성이기 때문에, 직접 생성한 {{jsxref("Number")}} 객체의 속성이 아니라 <code>Number.NEGATIVE_INFINITY</code>의 형식으로 사용해야 합니다.</p>

<h2 id="예제">예제</h2>

<h3 id="NEGATIVE_INFINITY_사용하기"><code>NEGATIVE_INFINITY</code> 사용하기</h3>

<p>다음 코드에서 <code>smallNumber</code>는 JavaScript의 최솟값보다 작은 값을 할당받습니다. {{jsxref("Statements/if...else", "if")}} 문이 실행되면, <code>smallNumber</code>의 값이 <code>-Infinity</code>이므로 <code>smallNumber</code>는 계산에 좀 더 적합한 값을 다시 할당합니다.</p>

<pre class="brush: js ">var smallNumber = (-Number.MAX_VALUE) * 2;

if (smallNumber === Number.NEGATIVE_INFINITY) {
  smallNumber = returnFinite();
}
</pre>

<h2 id="Specifications">명세</h2>

{{Specifications}}

<h2 id="브라우저_호환성">브라우저 호환성</h2>

<p>{{Compat("javascript.builtins.Number.NEGATIVE_INFINITY")}}</p>

<h2 id="같이_보기">같이 보기</h2>

<ul>
 <li>{{jsxref("Number.POSITIVE_INFINITY")}}</li>
 <li>{{jsxref("Number.isFinite()")}}</li>
 <li>{{jsxref("Infinity")}}</li>
 <li>{{jsxref("isFinite", "isFinite()")}}</li>
</ul>