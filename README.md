<div data-target="readme-toc.content" class="Box-body px-5 pb-5">
          <article class="markdown-body entry-content container-lg" itemprop="text"><h1><a id="user-content-clean-code-php" class="anchor" aria-hidden="true" href="#clean-code-php"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Clean Code PHP</h1>
<h2><a id="user-content-mục-lục" class="anchor" aria-hidden="true" href="#mục-lục"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Mục lục</h2>
<ol>
<li><a href="#gi%E1%BB%9Bi-thi%E1%BB%87u">Giới thiệu</a></li>
<li><a href="#bi%E1%BA%BFn">Biến</a>
<ul>
<li><a href="#s%E1%BB%AD-d%E1%BB%A5ng-t%C3%AAn-bi%E1%BA%BFn-c%C3%B3-%C3%BD-ngh%C4%A9a-v%C3%A0-d%E1%BB%85-hi%E1%BB%83u">Sử dụng tên biến có ý nghĩa và dễ hiểu</a></li>
<li><a href="#s%E1%BB%AD-d%E1%BB%A5ng-c%C3%B9ng-t%E1%BB%AB-v%E1%BB%B1ng-cho-c%C3%B9ng-m%E1%BB%99t-lo%E1%BA%A1i-bi%E1%BA%BFn">Sử dụng cùng từ vựng cho cùng một loại biến</a></li>
<li><a href="#%C4%90%E1%BA%B7t-t%C3%AAn-sao-cho-d%E1%BB%85-t%C3%ACm-ki%E1%BA%BFm-ph%E1%BA%A7n-1">Đặt tên sao cho dễ tìm kiếm (phần 1)</a></li>
<li><a href="#%C4%90%E1%BA%B7t-t%C3%AAn-sao-cho-d%E1%BB%85-t%C3%ACm-ki%E1%BA%BFm-ph%E1%BA%A7n-2">Đặt tên sao cho dễ tìm kiếm (phần 2)</a></li>
<li><a href="#%C4%91%E1%BA%B7t-t%C3%AAn-bi%E1%BA%BFn-d%E1%BB%85-hi%E1%BB%83u">Đặt tên biến có dễ hiểu</a></li>
<li><a href="#tr%C3%A1nh-l%E1%BB%93ng-nesting-qu%C3%A1-nhi%E1%BB%81u-v%C3%A0-n%C3%AAn-return-s%E1%BB%9Bm-ph%E1%BA%A7n-1">Tránh lồng (nesting) quá nhiều và nên return sớm (phần 1)</a></li>
<li><a href="#tr%C3%A1nh-l%E1%BB%93ng-nesting-qu%C3%A1-nhi%E1%BB%81u-v%C3%A0-n%C3%AAn-return-s%E1%BB%9Bm-ph%E1%BA%A7n-2">Tránh lồng (nesting) quá nhiều và nên return sớm (phần 2)</a></li>
<li><a href="#tr%C3%A1nh-hack-n%C3%A3o-ng%C6%B0%E1%BB%9Di-%C4%91%E1%BB%8Dc">Tránh hack não người đọc</a></li>
<li><a href="#%C4%90%E1%BB%ABng-th%C3%AAm-nh%E1%BB%AFng-n%E1%BB%99i-dung-kh%C3%B4ng-c%E1%BA%A7n-thi%E1%BA%BFt">Đừng thêm những nội dung không cần thiết</a></li>
<li><a href="#s%E1%BB%AD-d%E1%BB%A5ng-%C4%91%E1%BB%91i-s%E1%BB%91-m%E1%BA%B7c-%C4%91%E1%BB%8Bnh-thay-v%C3%AC-ph%E1%BA%A3i-ki%E1%BB%83m-tra-b%E1%BA%B1ng-bi%E1%BB%83u-th%E1%BB%A9c-%C4%91i%E1%BB%81u-ki%E1%BB%87n">Sử dụng đối số mặc định thay vì phải kiểm tra bằng biểu thức điều kiện</a></li>
</ul>
</li>
<li><a href="#so-s%C3%A1nh">So sánh</a>
<ul>
<li><a href="#s%E1%BB%AD-d%E1%BB%A5ng-identical-comparison">Sử dụng identical comparison</a></li>
</ul>
</li>
<li><a href="#h%C3%A0m">Hàm</a>
<ul>
<li><a href="#%C4%90%E1%BB%91i-s%E1%BB%91-c%E1%BB%A7a-h%C3%A0m-%C3%ADt-h%C6%A1n-ho%E1%BA%B7c-b%E1%BA%B1ng-2-l%C3%A0-l%C3%BD-t%C6%B0%E1%BB%9Fng">Đối số của hàm (ít hơn hoặc bằng 2 là lý tưởng)</a></li>
<li><a href="#h%C3%A0m-ch%E1%BB%89-th%E1%BB%B1c-hi%E1%BB%87n-m%E1%BB%99t-ch%E1%BB%A9c-n%C4%83ng">Hàm chỉ thực hiện một chức năng</a></li>
<li><a href="#t%C3%AAn-h%C3%A0m-n%C3%AAn-th%E1%BB%83-hi%E1%BB%87n-ch%E1%BB%A9c-n%C4%83ng-c%E1%BB%A7a-h%C3%A0m">Tên hàm nên thể hiện chức năng của hàm</a></li>
<li><a href="#h%C3%A0m-ch%E1%BB%89-n%C3%AAn-ch%E1%BB%A9a-m%E1%BB%99t-c%E1%BA%A5p-tr%E1%BB%ABu-t%C6%B0%E1%BB%A3ng">Hàm chỉ nên chứa một cấp trừu tượng</a></li>
<li><a href="#%C4%90%E1%BB%ABng-s%E1%BB%AD-d%E1%BB%A5ng-c%E1%BB%9D-nh%C6%B0-l%C3%A0-m%E1%BB%99t-%C4%91%E1%BB%91i-s%E1%BB%91-c%E1%BB%A7a-h%C3%A0m">Đừng sử dụng cờ như là một đối số của hàm</a></li>
<li><a href="#tr%C3%A1nh-t%C3%A1c-d%E1%BB%A5ng-ph%E1%BB%A5">Tránh tác dụng phụ</a></li>
<li><a href="#%C4%90%E1%BB%ABng-vi%E1%BA%BFt-h%C3%A0m-global">Đừng viết hàm global</a></li>
<li><a href="#%C4%90%E1%BB%ABng-s%E1%BB%AD-d%E1%BB%A5ng-singleton-pattern">Đừng sử dụng Singleton pattern</a></li>
<li><a href="#%C4%90%C3%B3ng-g%C3%B3i-%C4%91i%E1%BB%81u-ki%E1%BB%87n">Đóng gói điều kiện</a></li>
<li><a href="#tr%C3%A1nh-%C4%91i%E1%BB%81u-ki%E1%BB%87n-ph%E1%BB%A7-%C4%91%E1%BB%8Bnh">Tránh điều kiện phủ định</a></li>
<li><a href="#tr%C3%A1nh-d%C3%B9ng-%C4%91i%E1%BB%81u-ki%E1%BB%87n">Tránh dùng điều kiện</a></li>
<li><a href="#tr%C3%A1nh-ki%E1%BB%83m-tra-ki%E1%BB%83u-d%E1%BB%AF-li%E1%BB%87u-ph%E1%BA%A7n-1">Tránh kiểm tra kiểu dữ liệu (phần 1)</a></li>
<li><a href="#tr%C3%A1nh-ki%E1%BB%83m-tra-ki%E1%BB%83u-d%E1%BB%AF-li%E1%BB%87u-ph%E1%BA%A7n-2">Tránh kiểm tra kiểu dữ liệu (phần 2)</a></li>
<li><a href="#x%C3%B3a-dead-code">Xóa dead code</a></li>
</ul>
</li>
<li><a href="#%C4%90%E1%BB%91i-t%C6%B0%E1%BB%A3ng-v%C3%A0-ki%E1%BA%BFn-tr%C3%BAc-d%E1%BB%AF-li%E1%BB%87u">Đối tượng và kiến trúc dữ liệu</a>
<ul>
<li><a href="#s%E1%BB%AD-d%E1%BB%A5ng-%C4%91%E1%BB%91i-t%C6%B0%E1%BB%A3ng-%C4%91%C3%B3ng-g%C3%B3i">Sử dụng đối tượng đóng gói</a></li>
<li><a href="#t%E1%BA%A1o-%C4%91%E1%BB%91i-t%C6%B0%E1%BB%A3ng-c%C3%B3-ch%E1%BB%A9a-thu%E1%BB%99c-t%C3%ADnh-ho%E1%BA%B7c-ph%C6%B0%C6%A1ng-th%E1%BB%A9c-private/protected">Tạo đối tượng có chứa thuộc tính hoặc phương thức private/protected</a></li>
</ul>
</li>
<li><a href="#l%E1%BB%9Bp">Lớp</a>
<ul>
<li><a href="#%C6%AFu-ti%C3%AAn-th%C3%A0nh-ph%E1%BA%A7n-h%C6%A1n-k%E1%BA%BF-th%E1%BB%ABa">Ưu tiên thành phần hơn kế thừa</a></li>
<li><a href="#tr%C3%A1nh-vi%E1%BA%BFt-fluent-interfaces">Tránh viết fluent interfaces</a></li>
</ul>
</li>
<li><a href="#solid">SOLID</a>
<ul>
<li><a href="#nguy%C3%AAn-l%C3%BD-tr%C3%A1ch-nhi%E1%BB%87m-duy-nh%E1%BA%A5t-srp">Nguyên lý trách nhiệm duy nhất (SRP)</a></li>
<li><a href="#nguy%C3%AAn-l%C3%BD-%C4%91%C3%B3ng/m%E1%BB%9F-ocp">Nguyên lý Đóng/Mở (OCP)</a></li>
<li><a href="#nguy%C3%AAn-l%C3%BD-thay-th%E1%BA%BF-liskov-lsp">Nguyên lý thay thế Liskov (LSP)</a></li>
<li><a href="#nguy%C3%AAn-l%C3%BD-ph%C3%A2n-t%C3%A1ch-interface-isp">Nguyên lý phân tách interface (ISP)</a></li>
<li><a href="#nguy%C3%AAn-l%C3%BD-%C4%91%E1%BA%A3o-ng%C6%B0%E1%BB%A3c-dependencies-dip">Nguyên lý đảo ngược dependencies (DIP)</a></li>
</ul>
</li>
<li><a href="#nguy%C3%AAn-l%C3%BD-%C4%91%E1%BB%ABng-l%E1%BA%B7p-l%E1%BA%A1i-ch%C3%ADnh-m%C3%ACnh-dry">Nguyên lý đừng lặp lại chính mình (DRY)</a></li>
<li><a href="#c%C3%A1c-ng%C3%B4n-ng%E1%BB%AF-kh%C3%A1c">Các ngôn ngữ khác</a></li>
</ol>
<h2><a id="user-content-giới-thiệu" class="anchor" aria-hidden="true" href="#giới-thiệu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Giới thiệu</h2>
<p>Đây là những nguyên lý kỹ thuật phần mềm, được trích từ cuốn sách <a href="https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882" rel="nofollow"><em>Clean Code</em></a> của tác giả Robert C. Martin(thường gọi là Uncle Bob) rất thích hợp cho ngôn ngữ PHP. Tài liệu này không phải là sách hướng dẫn về phong cách viết code, mà là hướng dẫn cách làm thế nào để viết phần mềm dễ đọc, dễ sử dụng lại, và dễ cải tiến trong PHP.</p>
<p>Bạn không cần phải tuân theo tất cả các nguyên tắc trong tài liệu này.
Đây chỉ đơn giản là những hướng dẫn, nhưng dù sao nó cũng là đúc kết từ nhiều năm kinh nghiệm của tác giả.</p>
<p>Repository này lấy cảm hứng từ <a href="https://github.com/ryanmcdermott/clean-code-javascript">clean-code-javascript</a></p>
<p>Lưu ý: Dù nhiều lập trình viên còn sử dụng PHP 5, nhưng nhiều ví dụ trong đây chỉ chạy được trên PHP 7.1+.</p>
<h2><a id="user-content-biến" class="anchor" aria-hidden="true" href="#biến"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Biến</h2>
<h3><a id="user-content-sử-dụng-tên-biến-có-ý-nghĩa-và-dễ-hiểu" class="anchor" aria-hidden="true" href="#sử-dụng-tên-biến-có-ý-nghĩa-và-dễ-hiểu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Sử dụng tên biến có ý nghĩa và dễ hiểu</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>ymdstr</span> = <span class="pl-s1"><span class="pl-c1">$</span>moment</span>-&gt;<span class="pl-en">format</span>(<span class="pl-s">'y-m-d'</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$ymdstr = $moment->format('y-m-d');
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>currentDate</span> = <span class="pl-s1"><span class="pl-c1">$</span>moment</span>-&gt;<span class="pl-en">format</span>(<span class="pl-s">'y-m-d'</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$currentDate = $moment->format('y-m-d');
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-sử-dụng-cùng-từ-vựng-cho-cùng-một-loại-biến" class="anchor" aria-hidden="true" href="#sử-dụng-cùng-từ-vựng-cho-cùng-một-loại-biến"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Sử dụng cùng từ vựng cho cùng một loại biến</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-en">getUserInfo</span>();
<span class="pl-en">getUserData</span>();
<span class="pl-en">getUserRecord</span>();
<span class="pl-en">getUserProfile</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="getUserInfo();
getUserData();
getUserRecord();
getUserProfile();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-en">getUser</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="getUser();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đặt-tên-sao-cho-dễ-tìm-kiếm-phần-1" class="anchor" aria-hidden="true" href="#đặt-tên-sao-cho-dễ-tìm-kiếm-phần-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đặt tên sao cho dễ tìm kiếm (phần 1)</h3>
<p>Thường thì chúng ta sẽ đọc code nhiều hơn viết code. Nên điều quan trọng là code chúng ta viết ra phải dễ đọc và dễ tìm kiếm.
Nếu <em>không</em> đặt tên biến có ý nghĩa và làm chương trình dễ hiểu, chúng ta sẽ gây khó cho những lập trình viên khác. Do đó mỗi khi đặt tên biến, hàm thì hãy đặt có ý nghĩa.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-c">// Oh man, 448 là cái giề vậy?</span>
<span class="pl-c"></span><span class="pl-s1"><span class="pl-c1">$</span>result</span> = <span class="pl-s1"><span class="pl-c1">$</span>serializer</span>-&gt;<span class="pl-en">serialize</span>(<span class="pl-s1"><span class="pl-c1">$</span>data</span>, <span class="pl-c1">448</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="// Oh man, 448 là cái giề vậy?
$result = $serializer->serialize($data, 448);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>json</span> = <span class="pl-s1"><span class="pl-c1">$</span>serializer</span>-&gt;<span class="pl-en">serialize</span>(<span class="pl-s1"><span class="pl-c1">$</span>data</span>, <span class="pl-c1">JSON_UNESCAPED_SLASHES</span> | <span class="pl-c1">JSON_PRETTY_PRINT</span> | <span class="pl-c1">JSON_UNESCAPED_UNICODE</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$json = $serializer->serialize($data, JSON_UNESCAPED_SLASHES | JSON_PRETTY_PRINT | JSON_UNESCAPED_UNICODE);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<h3><a id="user-content-đặt-tên-sao-cho-dễ-tìm-kiếm-phần-2" class="anchor" aria-hidden="true" href="#đặt-tên-sao-cho-dễ-tìm-kiếm-phần-2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đặt tên sao cho dễ tìm kiếm (phần 2)</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-c">// Lại nữa, 4 nghĩa là cái giề đây?</span>
<span class="pl-c"></span><span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>user</span>-&gt;<span class="pl-c1">access</span> &amp; <span class="pl-c1">4</span>) {
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="// Lại nữa, 4 nghĩa là cái giề đây?
if ($user->access &amp; 4) {
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">User</span>
{
    <span class="pl-k">const</span> <span class="pl-c1">ACCESS_READ</span> = <span class="pl-c1">1</span>;
    <span class="pl-k">const</span> <span class="pl-c1">ACCESS_CREATE</span> = <span class="pl-c1">2</span>;
    <span class="pl-k">const</span> <span class="pl-c1">ACCESS_UPDATE</span> = <span class="pl-c1">4</span>;
    <span class="pl-k">const</span> <span class="pl-c1">ACCESS_DELETE</span> = <span class="pl-c1">8</span>;
}

<span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>user</span>-&gt;<span class="pl-c1">access</span> &amp; <span class="pl-v">User</span>::<span class="pl-c1">ACCESS_UPDATE</span>) {
    <span class="pl-c">// do edit ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class User
{
    const ACCESS_READ = 1;
    const ACCESS_CREATE = 2;
    const ACCESS_UPDATE = 4;
    const ACCESS_DELETE = 8;
}

if ($user->access &amp; User::ACCESS_UPDATE) {
    // do edit ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đặt-tên-biến-dễ-hiểu" class="anchor" aria-hidden="true" href="#đặt-tên-biến-dễ-hiểu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đặt tên biến dễ hiểu</h3>
<p>Tức là đặt tên biến sao cho đọc vô là hiểu nó là gì và nó dùng để làm gì. Không cần phải suy nghĩ, suy diễn.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>address</span> = <span class="pl-s">'One Infinite Loop, Cupertino 95014'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>cityZipCodeRegex</span> = <span class="pl-s">'/^[^,]+,\s*(.+?)\s*(\d{5})$/'</span>;
<span class="pl-en">preg_match</span>(<span class="pl-s1"><span class="pl-c1">$</span>cityZipCodeRegex</span>, <span class="pl-s1"><span class="pl-c1">$</span>address</span>, <span class="pl-s1"><span class="pl-c1">$</span>matches</span>);

<span class="pl-en">saveCityZipCode</span>(<span class="pl-s1"><span class="pl-c1">$</span>matches</span>[<span class="pl-c1">1</span>], <span class="pl-s1"><span class="pl-c1">$</span>matches</span>[<span class="pl-c1">2</span>]);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$address = 'One Infinite Loop, Cupertino 95014';
$cityZipCodeRegex = '/^[^,]+,\s*(.+?)\s*(\d{5})$/';
preg_match($cityZipCodeRegex, $address, $matches);

saveCityZipCode($matches[1], $matches[2]);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Không tệ lắm:</strong></p>
<p>Tốt hơn một chút, nhưng vẫn còn phụ thuộc nhiều vào regex.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>address</span> = <span class="pl-s">'One Infinite Loop, Cupertino 95014'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>cityZipCodeRegex</span> = <span class="pl-s">'/^[^,]+,\s*(.+?)\s*(\d{5})$/'</span>;
<span class="pl-en">preg_match</span>(<span class="pl-s1"><span class="pl-c1">$</span>cityZipCodeRegex</span>, <span class="pl-s1"><span class="pl-c1">$</span>address</span>, <span class="pl-s1"><span class="pl-c1">$</span>matches</span>);

[, <span class="pl-s1"><span class="pl-c1">$</span>city</span>, <span class="pl-s1"><span class="pl-c1">$</span>zipCode</span>] = <span class="pl-s1"><span class="pl-c1">$</span>matches</span>;
<span class="pl-en">saveCityZipCode</span>(<span class="pl-s1"><span class="pl-c1">$</span>city</span>, <span class="pl-s1"><span class="pl-c1">$</span>zipCode</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$address = 'One Infinite Loop, Cupertino 95014';
$cityZipCodeRegex = '/^[^,]+,\s*(.+?)\s*(\d{5})$/';
preg_match($cityZipCodeRegex, $address, $matches);

[, $city, $zipCode] = $matches;
saveCityZipCode($city, $zipCode);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<p>Đã giảm phụ thuộc vào regex bằng "naming subpatterns".</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>address</span> = <span class="pl-s">'One Infinite Loop, Cupertino 95014'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>cityZipCodeRegex</span> = <span class="pl-s">'/^[^,]+,\s*(?&lt;city&gt;.+?)\s*(?&lt;zipCode&gt;\d{5})$/'</span>;
<span class="pl-en">preg_match</span>(<span class="pl-s1"><span class="pl-c1">$</span>cityZipCodeRegex</span>, <span class="pl-s1"><span class="pl-c1">$</span>address</span>, <span class="pl-s1"><span class="pl-c1">$</span>matches</span>);

<span class="pl-en">saveCityZipCode</span>(<span class="pl-s1"><span class="pl-c1">$</span>matches</span>[<span class="pl-s">'city'</span>], <span class="pl-s1"><span class="pl-c1">$</span>matches</span>[<span class="pl-s">'zipCode'</span>]);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$address = 'One Infinite Loop, Cupertino 95014';
$cityZipCodeRegex = '/^[^,]+,\s*(?<city>.+?)\s*(?<zipCode>\d{5})$/';
preg_match($cityZipCodeRegex, $address, $matches);

saveCityZipCode($matches['city'], $matches['zipCode']);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-lồng-nesting-quá-nhiều-và-nên-return-sớm-phần-1" class="anchor" aria-hidden="true" href="#tránh-lồng-nesting-quá-nhiều-và-nên-return-sớm-phần-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh lồng (nesting) quá nhiều và nên return sớm (phần 1)</h3>
<p>Quá nhiều if else lồng nhau sẽ khiến code tăng độ phức tạp, khó debug. Giảm sự phức tạp bằng cách giảm số if else lồng nhau xuống ít nhất có thể. Return sớm chính là một cách giảm số lần lồng nhau.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">isShopOpen</span>(<span class="pl-s1"><span class="pl-c1">$</span>day</span>): <span class="pl-smi">bool</span>
{
    <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>day</span>) {
        <span class="pl-k">if</span> (<span class="pl-en">is_string</span>(<span class="pl-s1"><span class="pl-c1">$</span>day</span>)) {
            <span class="pl-s1"><span class="pl-c1">$</span>day</span> = <span class="pl-en">strtolower</span>(<span class="pl-s1"><span class="pl-c1">$</span>day</span>);
            <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>day</span> === <span class="pl-s">'friday'</span>) {
                <span class="pl-k">return</span> <span class="pl-c1">true</span>;
            } <span class="pl-k">elseif</span> (<span class="pl-s1"><span class="pl-c1">$</span>day</span> === <span class="pl-s">'saturday'</span>) {
                <span class="pl-k">return</span> <span class="pl-c1">true</span>;
            } <span class="pl-k">elseif</span> (<span class="pl-s1"><span class="pl-c1">$</span>day</span> === <span class="pl-s">'sunday'</span>) {
                <span class="pl-k">return</span> <span class="pl-c1">true</span>;
            } <span class="pl-k">else</span> {
                <span class="pl-k">return</span> <span class="pl-c1">false</span>;
            }
        } <span class="pl-k">else</span> {
            <span class="pl-k">return</span> <span class="pl-c1">false</span>;
        }
    } <span class="pl-k">else</span> {
        <span class="pl-k">return</span> <span class="pl-c1">false</span>;
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function isShopOpen($day): bool
{
    if ($day) {
        if (is_string($day)) {
            $day = strtolower($day);
            if ($day === 'friday') {
                return true;
            } elseif ($day === 'saturday') {
                return true;
            } elseif ($day === 'sunday') {
                return true;
            } else {
                return false;
            }
        } else {
            return false;
        }
    } else {
        return false;
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">isShopOpen</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>day</span>): <span class="pl-smi">bool</span>
{
    <span class="pl-k">if</span> (<span class="pl-en">empty</span>(<span class="pl-s1"><span class="pl-c1">$</span>day</span>)) {
        <span class="pl-k">return</span> <span class="pl-c1">false</span>;
    }

    <span class="pl-s1"><span class="pl-c1">$</span>openingDays</span> = [
        <span class="pl-s">'friday'</span>, <span class="pl-s">'saturday'</span>, <span class="pl-s">'sunday'</span>
    ];

    <span class="pl-k">return</span> <span class="pl-en">in_array</span>(<span class="pl-en">strtolower</span>(<span class="pl-s1"><span class="pl-c1">$</span>day</span>), <span class="pl-s1"><span class="pl-c1">$</span>openingDays</span>, <span class="pl-c1">true</span>);
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function isShopOpen(string $day): bool
{
    if (empty($day)) {
        return false;
    }

    $openingDays = [
        'friday', 'saturday', 'sunday'
    ];

    return in_array(strtolower($day), $openingDays, true);
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-lồng-nesting-quá-nhiều-và-nên-return-sớm-phần-2" class="anchor" aria-hidden="true" href="#tránh-lồng-nesting-quá-nhiều-và-nên-return-sớm-phần-2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh lồng (nesting) quá nhiều và nên return sớm (phần 2)</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">fibonacci</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>n</span>)
{
    <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>n</span> &lt; <span class="pl-c1">50</span>) {
        <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>n</span> !== <span class="pl-c1">0</span>) {
            <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>n</span> !== <span class="pl-c1">1</span>) {
                <span class="pl-k">return</span> <span class="pl-en">fibonacci</span>(<span class="pl-s1"><span class="pl-c1">$</span>n</span> - <span class="pl-c1">1</span>) + <span class="pl-en">fibonacci</span>(<span class="pl-s1"><span class="pl-c1">$</span>n</span> - <span class="pl-c1">2</span>);
            } <span class="pl-k">else</span> {
                <span class="pl-k">return</span> <span class="pl-c1">1</span>;
            }
        } <span class="pl-k">else</span> {
            <span class="pl-k">return</span> <span class="pl-c1">0</span>;
        }
    } <span class="pl-k">else</span> {
        <span class="pl-k">return</span> <span class="pl-s">'Not supported'</span>;
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function fibonacci(int $n)
{
    if ($n < 50) {
        if ($n !== 0) {
            if ($n !== 1) {
                return fibonacci($n - 1) + fibonacci($n - 2);
            } else {
                return 1;
            }
        } else {
            return 0;
        }
    } else {
        return 'Not supported';
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">fibonacci</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>n</span>): <span class="pl-smi">int</span>
{
    <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>n</span> === <span class="pl-c1">0</span> || <span class="pl-s1"><span class="pl-c1">$</span>n</span> === <span class="pl-c1">1</span>) {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>n</span>;
    }

    <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>n</span> &gt; <span class="pl-c1">50</span>) {
        <span class="pl-k">throw</span> <span class="pl-k">new</span> \<span class="pl-v">Exception</span>(<span class="pl-s">'Not supported'</span>);
    }

    <span class="pl-k">return</span> <span class="pl-en">fibonacci</span>(<span class="pl-s1"><span class="pl-c1">$</span>n</span> - <span class="pl-c1">1</span>) + <span class="pl-en">fibonacci</span>(<span class="pl-s1"><span class="pl-c1">$</span>n</span> - <span class="pl-c1">2</span>);
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function fibonacci(int $n): int
{
    if ($n === 0 || $n === 1) {
        return $n;
    }

    if ($n > 50) {
        throw new \Exception('Not supported');
    }

    return fibonacci($n - 1) + fibonacci($n - 2);
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-hack-não-người-đọc" class="anchor" aria-hidden="true" href="#tránh-hack-não-người-đọc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh hack não người đọc</h3>
<p>Đừng khiến người đọc code phải khó khăn để hiểu ý nghĩa của biến. Tên biến càng rõ ràng càng tốt.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>l</span> = [<span class="pl-s">'Austin'</span>, <span class="pl-s">'New York'</span>, <span class="pl-s">'San Francisco'</span>];

for (<span class="pl-s1"><span class="pl-c1">$</span>i</span> = <span class="pl-c1">0</span>; <span class="pl-s1"><span class="pl-c1">$</span>i</span> &lt; <span class="pl-en">count</span>(<span class="pl-s1"><span class="pl-c1">$</span>l</span>); <span class="pl-s1"><span class="pl-c1">$</span>i</span>++) {
    <span class="pl-s1"><span class="pl-c1">$</span>li</span> = <span class="pl-s1"><span class="pl-c1">$</span>l</span>[<span class="pl-s1"><span class="pl-c1">$</span>i</span>];
    <span class="pl-en">doStuff</span>();
    <span class="pl-en">doSomeOtherStuff</span>();
    <span class="pl-c">// ...</span>
    <span class="pl-c">// ...</span>
    <span class="pl-c">// ...</span>
    <span class="pl-c">// Đợi đã, `$li` là cái gì?</span>
<span class="pl-c"></span>    <span class="pl-en">dispatch</span>(<span class="pl-s1"><span class="pl-c1">$</span>li</span>);
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$l = ['Austin', 'New York', 'San Francisco'];

for ($i = 0; $i < count($l); $i++) {
    $li = $l[$i];
    doStuff();
    doSomeOtherStuff();
    // ...
    // ...
    // ...
    // Đợi đã, `$li` là cái gì?
    dispatch($li);
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>locations</span> = [<span class="pl-s">'Austin'</span>, <span class="pl-s">'New York'</span>, <span class="pl-s">'San Francisco'</span>];

<span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>locations</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>location</span>) {
    <span class="pl-en">doStuff</span>();
    <span class="pl-en">doSomeOtherStuff</span>();
    <span class="pl-c">// ...</span>
    <span class="pl-c">// ...</span>
    <span class="pl-c">// ...</span>
    <span class="pl-en">dispatch</span>(<span class="pl-s1"><span class="pl-c1">$</span>location</span>);
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$locations = ['Austin', 'New York', 'San Francisco'];

foreach ($locations as $location) {
    doStuff();
    doSomeOtherStuff();
    // ...
    // ...
    // ...
    dispatch($location);
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đừng-thêm-những-nội-dung-không-cần-thiết" class="anchor" aria-hidden="true" href="#đừng-thêm-những-nội-dung-không-cần-thiết"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đừng thêm những nội dung không cần thiết</h3>
<p>Nếu tên của class/object đã rõ ràng, không nên lặp lại chúng trong tên biến.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Car</span>
{
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>carMake</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>carModel</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>carColor</span>;

    <span class="pl-c">//...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Car
{
    public $carMake;
    public $carModel;
    public $carColor;

    //...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Car</span>
{
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>make</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>model</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>color</span>;

    <span class="pl-c">//...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Car
{
    public $make;
    public $model;
    public $color;

    //...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-sử-dụng-đối-số-mặc-định-thay-vì-phải-kiểm-tra-bằng-biểu-thức-điều-kiện" class="anchor" aria-hidden="true" href="#sử-dụng-đối-số-mặc-định-thay-vì-phải-kiểm-tra-bằng-biểu-thức-điều-kiện"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Sử dụng đối số mặc định thay vì phải kiểm tra bằng biểu thức điều kiện</h3>
<p><strong>Chưa tốt:</strong></p>
<p>Chưa tốt vì <code>$breweryName</code> có thể bị <code>NULL</code>.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">createMicrobrewery</span>(<span class="pl-s1"><span class="pl-c1">$</span>breweryName</span> = <span class="pl-s">'Hipster Brew Co.'</span>): <span class="pl-smi">void</span>
{
 &nbsp; &nbsp;<span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function createMicrobrewery($breweryName = 'Hipster Brew Co.'): void
{
 &nbsp; &nbsp;// ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Không tệ lắm:</strong></p>
<p>Cái này tốt hơn cái trước, nhưng nó nên quản lý được giá trị của biến thì tốt hơn.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">createMicrobrewery</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span> = <span class="pl-c1">null</span>): <span class="pl-smi">void</span>
{
 &nbsp; &nbsp;<span class="pl-s1"><span class="pl-c1">$</span>breweryName</span> = <span class="pl-s1"><span class="pl-c1">$</span>name</span> ?: <span class="pl-s">'Hipster Brew Co.'</span>;
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function createMicrobrewery($name = null): void
{
 &nbsp; &nbsp;$breweryName = $name ?: 'Hipster Brew Co.';
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<p>Bạn có thể sử dụng <a href="http://php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration" rel="nofollow">type hinting</a> và chắc chắn <code>$breweryName</code> sẽ không bị <code>NULL</code>.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">createMicrobrewery</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>breweryName</span> = <span class="pl-s">'Hipster Brew Co.'</span>): <span class="pl-smi">void</span>
{
 &nbsp; &nbsp;<span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function createMicrobrewery(string $breweryName = 'Hipster Brew Co.'): void
{
 &nbsp; &nbsp;// ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-so-sánh" class="anchor" aria-hidden="true" href="#so-sánh"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>So sánh</h2>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-sử-dụng-identical-comparison" class="anchor" aria-hidden="true" href="#sử-dụng-identical-comparison"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Sử dụng <a href="http://php.net/manual/en/language.operators.comparison.php" rel="nofollow">identical comparison</a></h3>
<p><strong>Chưa tốt:</strong></p>
<p>Sử dụng <em>simple comparison</em> (so sánh đơn giản)</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>a</span> = <span class="pl-s">'42'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>b</span> = <span class="pl-c1">42</span>;
<span class="pl-v">S</span>ử dụng simple comparison thì nó sẽ tự chuyển kiểu string qua kiểu int

<span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>a</span> != <span class="pl-s1"><span class="pl-c1">$</span>b</span>) {
   <span class="pl-c">//Biểu thức này sẽ trả về `false`</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$a = '42';
$b = 42;
Sử dụng simple comparison thì nó sẽ tự chuyển kiểu string qua kiểu int

if ($a != $b) {
   //Biểu thức này sẽ trả về `false`
}

" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Phép so sánh $a != $b trả về <code>false</code> nhưng trong thực tế thì nó phải là <code>true</code>.
<strong>Chuỗi</strong> '42' thì phải khác <strong>số</strong> 42 chứ đúng không.</p>
<p><strong>Tốt:</strong></p>
<p>Sử dụng <em>identical comparison</em> (so sánh giống hệt nhau) để so sánh cả kiểu dữ liệu và giá trị</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>a</span> !== <span class="pl-s1"><span class="pl-c1">$</span>b</span>) {
    <span class="pl-c">//Biểu thức này trả về `true`</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="if ($a !== $b) {
    //Biểu thức này trả về `true`
}

" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-hàm" class="anchor" aria-hidden="true" href="#hàm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Hàm</h2>
<h3><a id="user-content-đối-số-của-hàm-ít-hơn-hoặc-bằng-2-là-lý-tưởng" class="anchor" aria-hidden="true" href="#đối-số-của-hàm-ít-hơn-hoặc-bằng-2-là-lý-tưởng"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đối số của hàm (ít hơn hoặc bằng 2 là lý tưởng)</h3>
<p>Giới hạn số lượng đối số (parameters) của hàm vô cùng quan trọng bởi vì nó giúp dễ test hơn.
Có nhiều hơn 3 đối số dẫn đến một tổ hợp rất nhiều trường hợp khác nhau cần phải test.</p>
<p>Lý tưởng nhất là khi hàm không có đối số nào. Một hoặc hai đối số là ok, còn ba thì nên hạn chế.
Bất cứ khi nào hàm có nhiều hơn 3 đối số thì cần phải xem xét tìm cách giảm bớt lại.
Bởi vì nếu hàm có nhiều hơn hai đối số thì nó phải xử lý rất nhiều.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">createMenu</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>title</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>body</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>buttonText</span>, <span class="pl-smi">bool</span> <span class="pl-s1"><span class="pl-c1">$</span>cancellable</span>): <span class="pl-smi">void</span>
{
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function createMenu(string $title, string $body, string $buttonText, bool $cancellable): void
{
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">MenuConfig</span>
{
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>title</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>body</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>buttonText</span>;
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>cancellable</span> = <span class="pl-c1">false</span>;
}

<span class="pl-s1"><span class="pl-c1">$</span>config</span> = <span class="pl-k">new</span> <span class="pl-v">MenuConfig</span>();
<span class="pl-s1"><span class="pl-c1">$</span>config</span>-&gt;<span class="pl-c1">title</span> = <span class="pl-s">'Foo'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>config</span>-&gt;<span class="pl-c1">body</span> = <span class="pl-s">'Bar'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>config</span>-&gt;<span class="pl-c1">buttonText</span> = <span class="pl-s">'Baz'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>config</span>-&gt;<span class="pl-c1">cancellable</span> = <span class="pl-c1">true</span>;

<span class="pl-k">function</span> <span class="pl-en">createMenu</span>(<span class="pl-smi">MenuConfig</span> <span class="pl-s1"><span class="pl-c1">$</span>config</span>): <span class="pl-smi">void</span>
{
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class MenuConfig
{
    public $title;
    public $body;
    public $buttonText;
    public $cancellable = false;
}

$config = new MenuConfig();
$config->title = 'Foo';
$config->body = 'Bar';
$config->buttonText = 'Baz';
$config->cancellable = true;

function createMenu(MenuConfig $config): void
{
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-hàm-chỉ-thực-hiện-một-chức-năng" class="anchor" aria-hidden="true" href="#hàm-chỉ-thực-hiện-một-chức-năng"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Hàm chỉ thực hiện một chức năng</h3>
<p>Đây là nguyên tắc quan trọng nhất trong phát triển phần mềm.
Khi hàm thực hiện nhiều hơn một chức năng, chúng khó biên dịch, kiểm tra và biết được nguyên nhân lỗi.
Khi bạn tạo hàm chỉ với một chức năng, sẽ dễ dàng refactor hơn và code sẽ dễ đọc hơn.
Nếu làm được điều này thì bạn sẽ tốt hơn nhiều lập trình viên khác.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">emailClients</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>clients</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>clients</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>client</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>clientRecord</span> = <span class="pl-s1"><span class="pl-c1">$</span>db</span>-&gt;<span class="pl-en">find</span>(<span class="pl-s1"><span class="pl-c1">$</span>client</span>);
        <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>clientRecord</span>-&gt;<span class="pl-en">isActive</span>()) {
            <span class="pl-en">email</span>(<span class="pl-s1"><span class="pl-c1">$</span>client</span>);
        }
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function emailClients(array $clients): void
{
    foreach ($clients as $client) {
        $clientRecord = $db->find($client);
        if ($clientRecord->isActive()) {
            email($client);
        }
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">emailClients</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>clients</span>): <span class="pl-smi">void</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>activeClients</span> = <span class="pl-en">activeClients</span>(<span class="pl-s1"><span class="pl-c1">$</span>clients</span>);
    <span class="pl-en">array_walk</span>(<span class="pl-s1"><span class="pl-c1">$</span>activeClients</span>, <span class="pl-s">'email'</span>);
}

<span class="pl-k">function</span> <span class="pl-en">activeClients</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>clients</span>): <span class="pl-smi">array</span>
{
    <span class="pl-k">return</span> <span class="pl-en">array_filter</span>(<span class="pl-s1"><span class="pl-c1">$</span>clients</span>, <span class="pl-s">'isClientActive'</span>);
}

<span class="pl-k">function</span> <span class="pl-en">isClientActive</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>client</span>): <span class="pl-smi">bool</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>clientRecord</span> = <span class="pl-s1"><span class="pl-c1">$</span>db</span>-&gt;<span class="pl-en">find</span>(<span class="pl-s1"><span class="pl-c1">$</span>client</span>);

    <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>clientRecord</span>-&gt;<span class="pl-en">isActive</span>();
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function emailClients(array $clients): void
{
    $activeClients = activeClients($clients);
    array_walk($activeClients, 'email');
}

function activeClients(array $clients): array
{
    return array_filter($clients, 'isClientActive');
}

function isClientActive(int $client): bool
{
    $clientRecord = $db->find($client);

    return $clientRecord->isActive();
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tên-hàm-nên-thể-hiện-chức-năng-của-hàm" class="anchor" aria-hidden="true" href="#tên-hàm-nên-thể-hiện-chức-năng-của-hàm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tên hàm nên thể hiện chức năng của hàm</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Email</span>
{
    <span class="pl-c">//...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">handle</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-en">mail</span>(<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">to</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">subject</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">body</span>);
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>message</span> = <span class="pl-k">new</span> <span class="pl-v">Email</span>(...);
<span class="pl-c">// Hàm này dùng làm gì? Có phải nó xử lý mail? Nó có đang ghi gì vào file không?</span>
<span class="pl-c"></span><span class="pl-s1"><span class="pl-c1">$</span>message</span>-&gt;<span class="pl-en">handle</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Email
{
    //...

    public function handle(): void
    {
        mail($this->to, $this->subject, $this->body);
    }
}

$message = new Email(...);
// Hàm này dùng làm gì? Có phải nó xử lý mail? Nó có đang ghi gì vào file không?
$message->handle();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Email</span> 
{
    <span class="pl-c">//...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">send</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-en">mail</span>(<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">to</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">subject</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">body</span>);
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>message</span> = <span class="pl-k">new</span> <span class="pl-v">Email</span>(...);
<span class="pl-c">// Rõ ràng và minh bạch, hàm này gửi mail</span>
<span class="pl-s1"><span class="pl-c1">$</span>message</span>-&gt;<span class="pl-en">send</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Email 
{
    //...

    public function send(): void
    {
        mail($this->to, $this->subject, $this->body);
    }
}

$message = new Email(...);
// Rõ ràng và minh bạch, hàm này gửi mail
$message->send();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-hàm-chỉ-nên-có-độ-trừu-tượng-một-cấp" class="anchor" aria-hidden="true" href="#hàm-chỉ-nên-có-độ-trừu-tượng-một-cấp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Hàm chỉ nên có độ trừu tượng một cấp</h3>
<p>Khi bạn có độ trừu tượng nhiều hơn một cấp thì hàm thường phải làm quá nhiều việc.
Hãy chia tách hàm ra thành nhiều phần để dễ sử dụng lại và dễ test.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">parseBetterJSAlternative</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>code</span>): <span class="pl-smi">void</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>regexes</span> = [
        <span class="pl-c">// ...</span>
    ];

    <span class="pl-s1"><span class="pl-c1">$</span>statements</span> = <span class="pl-en">explode</span>(<span class="pl-s">' '</span>, <span class="pl-s1"><span class="pl-c1">$</span>code</span>);
    <span class="pl-s1"><span class="pl-c1">$</span>tokens</span> = [];
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>regexes</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>regex</span>) {
        <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>statements</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>statement</span>) {
            <span class="pl-c">// ...</span>
        }
    }

    <span class="pl-s1"><span class="pl-c1">$</span>ast</span> = [];
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>tokens</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>token</span>) {
        <span class="pl-c">// lex...</span>
    }

    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>ast</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>node</span>) {
        <span class="pl-c">// parse...</span>
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function parseBetterJSAlternative(string $code): void
{
    $regexes = [
        // ...
    ];

    $statements = explode(' ', $code);
    $tokens = [];
    foreach ($regexes as $regex) {
        foreach ($statements as $statement) {
            // ...
        }
    }

    $ast = [];
    foreach ($tokens as $token) {
        // lex...
    }

    foreach ($ast as $node) {
        // parse...
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Cũng chưa tốt:</strong></p>
<p>Chúng ta đã thực hiện tách ra vài hàm, nhưng hàm <code>parseBetterJSAlternative()</code> vẫn còn khá phức tạp và khó test.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">tokenize</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>code</span>): <span class="pl-smi">array</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>regexes</span> = [
        <span class="pl-c">// ...</span>
    ];

    <span class="pl-s1"><span class="pl-c1">$</span>statements</span> = <span class="pl-en">explode</span>(<span class="pl-s">' '</span>, <span class="pl-s1"><span class="pl-c1">$</span>code</span>);
    <span class="pl-s1"><span class="pl-c1">$</span>tokens</span> = [];
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>regexes</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>regex</span>) {
        <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>statements</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>statement</span>) {
            <span class="pl-s1"><span class="pl-c1">$</span>tokens</span>[] = <span class="pl-c">/* ... */</span>;
        }
    }

    <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>tokens</span>;
}

<span class="pl-k">function</span> <span class="pl-en">lexer</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>tokens</span>): <span class="pl-smi">array</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>ast</span> = [];
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>tokens</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>token</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>ast</span>[] = <span class="pl-c">/* ... */</span>;
    }

    <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>ast</span>;
}

<span class="pl-k">function</span> <span class="pl-en">parseBetterJSAlternative</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>code</span>): <span class="pl-smi">void</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>tokens</span> = <span class="pl-en">tokenize</span>(<span class="pl-s1"><span class="pl-c1">$</span>code</span>);
    <span class="pl-s1"><span class="pl-c1">$</span>ast</span> = <span class="pl-en">lexer</span>(<span class="pl-s1"><span class="pl-c1">$</span>tokens</span>);
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>ast</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>node</span>) {
        <span class="pl-c">// parse...</span>
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function tokenize(string $code): array
{
    $regexes = [
        // ...
    ];

    $statements = explode(' ', $code);
    $tokens = [];
    foreach ($regexes as $regex) {
        foreach ($statements as $statement) {
            $tokens[] = /* ... */;
        }
    }

    return $tokens;
}

function lexer(array $tokens): array
{
    $ast = [];
    foreach ($tokens as $token) {
        $ast[] = /* ... */;
    }

    return $ast;
}

function parseBetterJSAlternative(string $code): void
{
    $tokens = tokenize($code);
    $ast = lexer($tokens);
    foreach ($ast as $node) {
        // parse...
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<p>Giải pháp tốt nhất là chuyển các phần thành các dependencies của hàm <code>parseBetterJSAlternative()</code></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Tokenizer</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">tokenize</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>code</span>): <span class="pl-smi">array</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span>regexes</span> = [
            <span class="pl-c">// ...</span>
        ];

        <span class="pl-s1"><span class="pl-c1">$</span>statements</span> = <span class="pl-en">explode</span>(<span class="pl-s">' '</span>, <span class="pl-s1"><span class="pl-c1">$</span>code</span>);
        <span class="pl-s1"><span class="pl-c1">$</span>tokens</span> = [];
        <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>regexes</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>regex</span>) {
            <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>statements</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>statement</span>) {
                <span class="pl-s1"><span class="pl-c1">$</span>tokens</span>[] = <span class="pl-c">/* ... */</span>;
            }
        }

        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>tokens</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">Lexer</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">lexify</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>tokens</span>): <span class="pl-smi">array</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span>ast</span> = [];
        <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>tokens</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>token</span>) {
            <span class="pl-s1"><span class="pl-c1">$</span>ast</span>[] = <span class="pl-c">/* ... */</span>;
        }

        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>ast</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">BetterJSAlternative</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>tokenizer</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>lexer</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">Tokenizer</span> <span class="pl-s1"><span class="pl-c1">$</span>tokenizer</span>, <span class="pl-smi">Lexer</span> <span class="pl-s1"><span class="pl-c1">$</span>lexer</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">tokenizer</span> = <span class="pl-s1"><span class="pl-c1">$</span>tokenizer</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">lexer</span> = <span class="pl-s1"><span class="pl-c1">$</span>lexer</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">parse</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>code</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span>tokens</span> = <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">tokenizer</span>-&gt;<span class="pl-en">tokenize</span>(<span class="pl-s1"><span class="pl-c1">$</span>code</span>);
        <span class="pl-s1"><span class="pl-c1">$</span>ast</span> = <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">lexer</span>-&gt;<span class="pl-en">lexify</span>(<span class="pl-s1"><span class="pl-c1">$</span>tokens</span>);
        <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>ast</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>node</span>) {
            <span class="pl-c">// parse...</span>
        }
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Tokenizer
{
    public function tokenize(string $code): array
    {
        $regexes = [
            // ...
        ];

        $statements = explode(' ', $code);
        $tokens = [];
        foreach ($regexes as $regex) {
            foreach ($statements as $statement) {
                $tokens[] = /* ... */;
            }
        }

        return $tokens;
    }
}

class Lexer
{
    public function lexify(array $tokens): array
    {
        $ast = [];
        foreach ($tokens as $token) {
            $ast[] = /* ... */;
        }

        return $ast;
    }
}

class BetterJSAlternative
{
    private $tokenizer;
    private $lexer;

    public function __construct(Tokenizer $tokenizer, Lexer $lexer)
    {
        $this->tokenizer = $tokenizer;
        $this->lexer = $lexer;
    }

    public function parse(string $code): void
    {
        $tokens = $this->tokenizer->tokenize($code);
        $ast = $this->lexer->lexify($tokens);
        foreach ($ast as $node) {
            // parse...
        }
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đừng-sử-dụng-cờ-như-là-một-đối-số-của-hàm" class="anchor" aria-hidden="true" href="#đừng-sử-dụng-cờ-như-là-một-đối-số-của-hàm"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đừng sử dụng cờ như là một đối số của hàm</h3>
<p>Cờ dùng để nói rằng hàm này thực hiện nhiều hơn một công việc. Nhưng hàm thì chỉ nên xử lý một công việc mà thôi.
Do đó hãy chia tách hàm của bạn nếu như chúng có nhiều luồng code phân biệt bằng boolean(true/false).</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">createFile</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>, <span class="pl-smi">bool</span> <span class="pl-s1"><span class="pl-c1">$</span>temp</span> = <span class="pl-c1">false</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>temp</span>) {
        <span class="pl-en">touch</span>(<span class="pl-s">'./temp/'</span>.<span class="pl-s1"><span class="pl-c1">$</span>name</span>);
    } <span class="pl-k">else</span> {
        <span class="pl-en">touch</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>);
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function createFile(string $name, bool $temp = false): void
{
    if ($temp) {
        touch('./temp/'.$name);
    } else {
        touch($name);
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">createFile</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>): <span class="pl-smi">void</span>
{
    <span class="pl-en">touch</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>);
}

<span class="pl-k">function</span> <span class="pl-en">createTempFile</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>): <span class="pl-smi">void</span>
{
    <span class="pl-en">touch</span>(<span class="pl-s">'./temp/'</span>.<span class="pl-s1"><span class="pl-c1">$</span>name</span>);
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function createFile(string $name): void
{
    touch($name);
}

function createTempFile(string $name): void
{
    touch('./temp/'.$name);
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-tác-dụng-phụ" class="anchor" aria-hidden="true" href="#tránh-tác-dụng-phụ"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh tác dụng phụ</h3>
<p>Một hàm sinh ra tác dụng phụ nếu nó thực hiện thêm việc khác ngoài việc lấy giá trị vào và trả về một hoặc nhiều giá trị khác.
Tác dụng phụ có thể là viết vào một file nào đó, sửa đổi biến global, hoặc vô tình chuyển hết tiền của bạn cho người lạ nào đó.</p>
<p>Vậy nếu bây giờ bạn cần hàm thực hiện các tác dụng phụ đó thì sao. Giống như ví dụ trước, bạn cần ghi vào file. Điều bạn cần làm
là tập trung những việc này lại một chỗ. Đừng viết vài hàm và vài lớp chỉ để ghi vào vài file cụ thể.
Hãy viết một service để làm điều đó. Một và chỉ một service.</p>
<p>Hãy tránh những sai lầm phổ biến như: chia sẻ trạng thái giữa các object mà không tuân theo cấu trúc nào,
sử dụng kiểu dữ liệu có thể thay đổi/bị thay đổi dễ dàng, không tổng hợp các tác dụng phụ có thể xảy ra khi viết hàm.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-c">// Biến glabal được tham chiếu bởi hàm bên dưới.</span>
<span class="pl-c">// Nếu ta tạo một function khác sử dụng chính biến name, ví dụ bên dưới cho thấy nó biến thành array và đã bị phá vỡ.</span>
<span class="pl-s1"><span class="pl-c1">$</span>name</span> = <span class="pl-s">'Ryan McDermott'</span>;

<span class="pl-k">function</span> <span class="pl-en">splitIntoFirstAndLastName</span>(): <span class="pl-smi">void</span>
{
    <span class="pl-k">global</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>;

    <span class="pl-s1"><span class="pl-c1">$</span>name</span> = <span class="pl-en">explode</span>(<span class="pl-s">' '</span>, <span class="pl-s1"><span class="pl-c1">$</span>name</span>);
}

<span class="pl-en">splitIntoFirstAndLastName</span>();

<span class="pl-en">var_dump</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>); <span class="pl-c">// ['Ryan', 'McDermott'];</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="// Biến glabal được tham chiếu bởi hàm bên dưới.
// Nếu ta tạo một function khác sử dụng chính biến name, ví dụ bên dưới cho thấy nó biến thành array và đã bị phá vỡ.
$name = 'Ryan McDermott';

function splitIntoFirstAndLastName(): void
{
    global $name;

    $name = explode(' ', $name);
}

splitIntoFirstAndLastName();

var_dump($name); // ['Ryan', 'McDermott'];
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">splitIntoFirstAndLastName</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>): <span class="pl-smi">array</span>
{
    <span class="pl-k">return</span> <span class="pl-en">explode</span>(<span class="pl-s">' '</span>, <span class="pl-s1"><span class="pl-c1">$</span>name</span>);
}

<span class="pl-s1"><span class="pl-c1">$</span>name</span> = <span class="pl-s">'Ryan McDermott'</span>;
<span class="pl-s1"><span class="pl-c1">$</span>newName</span> = <span class="pl-en">splitIntoFirstAndLastName</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>);

<span class="pl-en">var_dump</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>); <span class="pl-c">// 'Ryan McDermott';</span>
<span class="pl-en">var_dump</span>(<span class="pl-s1"><span class="pl-c1">$</span>newName</span>); <span class="pl-c">// ['Ryan', 'McDermott'];</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function splitIntoFirstAndLastName(string $name): array
{
    return explode(' ', $name);
}

$name = 'Ryan McDermott';
$newName = splitIntoFirstAndLastName($name);

var_dump($name); // 'Ryan McDermott';
var_dump($newName); // ['Ryan', 'McDermott'];
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đừng-viết-hàm-global" class="anchor" aria-hidden="true" href="#đừng-viết-hàm-global"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đừng viết hàm global</h3>
<p>Dùng nhiều hàm global là bad practice với nhiều ngôn ngữ bởi vì có thể gây xung đột với thư viện khác
và người sử dụng API của bạn không hề hay biết gì cho đến khi nhận được thông báo lỗi.</p>
<p>Hãy xem xét ví dụ sau: bạn sẽ làm gì nếu muốn trả về một mảng.</p>
<p>Bạn có thể viết hàm global như <code>config()</code>, nhưng nó có thể xung đột với thư viện khác thực hiện cùng chức năng.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">config</span>(): <span class="pl-smi">array</span>
{
    <span class="pl-k">return</span>  [
        <span class="pl-s">'foo'</span> =&gt; <span class="pl-s">'bar'</span>,
    ]
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function config(): array
{
    return  [
        'foo' => 'bar',
    ]
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Configuration</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>configuration</span> = [];

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>configuration</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">configuration</span> = <span class="pl-s1"><span class="pl-c1">$</span>configuration</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">get</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>key</span>): ?<span class="pl-smi">string</span>
    {
        <span class="pl-k">return</span> <span class="pl-en">isset</span>(<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">configuration</span>[<span class="pl-s1"><span class="pl-c1">$</span>key</span>]) ? <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">configuration</span>[<span class="pl-s1"><span class="pl-c1">$</span>key</span>] : <span class="pl-c1">null</span>;
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Configuration
{
    private $configuration = [];

    public function __construct(array $configuration)
    {
        $this->configuration = $configuration;
    }

    public function get(string $key): ?string
    {
        return isset($this->configuration[$key]) ? $this->configuration[$key] : null;
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Tạo instance của lớp <code>Configuration</code></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>configuration</span> = <span class="pl-k">new</span> <span class="pl-v">Configuration</span>([
    <span class="pl-s">'foo'</span> =&gt; <span class="pl-s">'bar'</span>,
]);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$configuration = new Configuration([
    'foo' => 'bar',
]);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Và bây giờ sử dụng instance <code>Configuration</code> trong ứng dụng của bạn.</p>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đừng-sử-dụng-singleton-pattern" class="anchor" aria-hidden="true" href="#đừng-sử-dụng-singleton-pattern"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đừng sử dụng Singleton pattern</h3>
<p>Singleton là một <a href="https://en.wikipedia.org/wiki/Singleton_pattern" rel="nofollow">anti-pattern</a>. Trích đoạn từ Brian Button:</p>
<ol>
<li>Chúng thường được sử dụng như <strong>global instance</strong>, vì sao lại Chưa tốt? Bởi vì <strong>bạn ẩn dependencies</strong> của ứng dụng bên trong code của bạn,
thay vì thông qua interfaces</li>
<li>Chúng vi phạm <a href="#single-responsibility-principle-srp">single responsibility principle</a>: bởi vì thực tế là <strong>chúng điều khiển những gì chúng tạo ra và vòng đời của nó</strong></li>
<li>Chúng đã tạo ra kiểu code <a href="https://en.wikipedia.org/wiki/Coupling_%28computer_programming%29" rel="nofollow">coupling</a>. Đây là một sự giả mạo và được giấu bằng cách tạo ra nhiều trường hợp <strong>test khó khăn hơn</strong>.</li>
<li>Chúng giữ trạng thái suốt vòng đời của ứng dụng. Bạn nên kết thúc sớm testing khi lỗi. Nhưng Singleton thì lại duy trì trạng thái nên nó Chưa tốt.</li>
</ol>
<p>Đây là một ý kiến khác của <a href="http://misko.hevery.com/about/" rel="nofollow">Misko Hevery</a> về <a href="http://misko.hevery.com/2008/08/25/root-cause-of-singletons/" rel="nofollow">gốc rễ của vấn đề</a>.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">DBConnection</span>
{
    <span class="pl-k">private</span> <span class="pl-k">static</span> <span class="pl-c1"><span class="pl-c1">$</span>instance</span>;

    <span class="pl-k">private</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>dsn</span>)
    {
        <span class="pl-c">// ...</span>
    }

    <span class="pl-k">public</span> <span class="pl-k">static</span> <span class="pl-k">function</span> <span class="pl-en">getInstance</span>(): <span class="pl-smi">DBConnection</span>
    {
        <span class="pl-k">if</span> (<span class="pl-smi">self</span>::<span class="pl-s1"><span class="pl-c1">$</span>instance</span> === <span class="pl-c1">null</span>) {
            <span class="pl-smi">self</span>::<span class="pl-s1"><span class="pl-c1">$</span>instance</span> = <span class="pl-k">new</span> self();
        }

        <span class="pl-k">return</span> <span class="pl-smi">self</span>::<span class="pl-s1"><span class="pl-c1">$</span>instance</span>;
    }

    <span class="pl-c">// ...</span>
}

<span class="pl-s1"><span class="pl-c1">$</span>singleton</span> = <span class="pl-v">DBConnection</span>::<span class="pl-en">getInstance</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class DBConnection
{
    private static $instance;

    private function __construct(string $dsn)
    {
        // ...
    }

    public static function getInstance(): DBConnection
    {
        if (self::$instance === null) {
            self::$instance = new self();
        }

        return self::$instance;
    }

    // ...
}

$singleton = DBConnection::getInstance();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">DBConnection</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>dsn</span>)
    {
        <span class="pl-c">// ...</span>
    }

     <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class DBConnection
{
    public function __construct(string $dsn)
    {
        // ...
    }

     // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Tạo instance của lớp <code>DBConnection</code> và cấu hình chúng với <a href="http://php.net/manual/en/pdo.construct.php#refsect1-pdo.construct-parameters" rel="nofollow">DSN</a>.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-s1"><span class="pl-c1">$</span>connection</span> = <span class="pl-k">new</span> <span class="pl-v">DBConnection</span>(<span class="pl-s1"><span class="pl-c1">$</span>dsn</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="$connection = new DBConnection($dsn);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Và bây giờ sử dụng instance <code>DBConnection</code> cho ứng dụng của bạn.</p>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-đóng-gói-điều-kiện" class="anchor" aria-hidden="true" href="#đóng-gói-điều-kiện"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đóng gói điều kiện</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>article</span>-&gt;<span class="pl-c1">state</span> === <span class="pl-s">'published'</span>) {
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="if ($article->state === 'published') {
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>article</span>-&gt;<span class="pl-en">isPublished</span>()) {
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="if ($article->isPublished()) {
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-điều-kiện-phủ-định" class="anchor" aria-hidden="true" href="#tránh-điều-kiện-phủ-định"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh điều kiện phủ định</h3>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">isDOMNodeNotPresent</span>(\<span class="pl-smi">DOMNode</span> <span class="pl-s1"><span class="pl-c1">$</span>node</span>): <span class="pl-smi">bool</span>
{
    <span class="pl-c">// ...</span>
}

<span class="pl-k">if</span> (!<span class="pl-en">isDOMNodeNotPresent</span>(<span class="pl-s1"><span class="pl-c1">$</span>node</span>))
{
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function isDOMNodeNotPresent(\DOMNode $node): bool
{
    // ...
}

if (!isDOMNodeNotPresent($node))
{
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">isDOMNodePresent</span>(\<span class="pl-smi">DOMNode</span> <span class="pl-s1"><span class="pl-c1">$</span>node</span>): <span class="pl-smi">bool</span>
{
    <span class="pl-c">// ...</span>
}

<span class="pl-k">if</span> (<span class="pl-en">isDOMNodePresent</span>(<span class="pl-s1"><span class="pl-c1">$</span>node</span>)) {
    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function isDOMNodePresent(\DOMNode $node): bool
{
    // ...
}

if (isDOMNodePresent($node)) {
    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-dùng-điều-kiện" class="anchor" aria-hidden="true" href="#tránh-dùng-điều-kiện"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh dùng điều kiện</h3>
<p>Điều này có vẻ không khả quan. Hầu hết mọi người sẽ thắc mắc,
"làm sao có thể làm gì đó mà không có <code>if</code>?" Bạn có thể dùng tính đa hình để hoàn thành việc đó trong khá nhiều trường hợp.
Câu hỏi thứ hai là, "ồ ngon nhưng tại sao phải làm thế?"
Bởi vì khái niệm clean code mà ta đã học trước đây: một hàm chỉ nên thực hiện một chức năng.
Khi bạn có một lớp hoặc hàm chứa <code>if</code>, tức là bạn đang muốn nó thực hiện nhiều việc. Luôn nhớ, chỉ một mà thôi.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Airplane</span>
{
    <span class="pl-c">// ...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getCruisingAltitude</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">switch</span> (<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">type</span>) {
            <span class="pl-k">case</span> <span class="pl-s">'777'</span>:
                <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getMaxAltitude</span>() - <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getPassengerCount</span>();
            <span class="pl-k">case</span> <span class="pl-s">'Air Force One'</span>:
                <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getMaxAltitude</span>();
            <span class="pl-k">case</span> <span class="pl-s">'Cessna'</span>:
                <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getMaxAltitude</span>() - <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getFuelExpenditure</span>();
        }
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Airplane
{
    // ...

    public function getCruisingAltitude(): int
    {
        switch ($this->type) {
            case '777':
                return $this->getMaxAltitude() - $this->getPassengerCount();
            case 'Air Force One':
                return $this->getMaxAltitude();
            case 'Cessna':
                return $this->getMaxAltitude() - $this->getFuelExpenditure();
        }
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">interface</span> <span class="pl-v">Airplane</span>
{
    <span class="pl-c">// ...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getCruisingAltitude</span>(): <span class="pl-smi">int</span>;
}

<span class="pl-k">class</span> <span class="pl-v">Boeing777</span> <span class="pl-k">implements</span> <span class="pl-v">Airplane</span>
{
    <span class="pl-c">// ...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getCruisingAltitude</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getMaxAltitude</span>() - <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getPassengerCount</span>();
    }
}

<span class="pl-k">class</span> <span class="pl-v">AirForceOne</span> <span class="pl-k">implements</span> <span class="pl-v">Airplane</span>
{
    <span class="pl-c">// ...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getCruisingAltitude</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getMaxAltitude</span>();
    }
}

<span class="pl-k">class</span> <span class="pl-v">Cessna</span> <span class="pl-k">implements</span> <span class="pl-v">Airplane</span>
{
    <span class="pl-c">// ...</span>

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getCruisingAltitude</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getMaxAltitude</span>() - <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">getFuelExpenditure</span>();
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="interface Airplane
{
    // ...

    public function getCruisingAltitude(): int;
}

class Boeing777 implements Airplane
{
    // ...

    public function getCruisingAltitude(): int
    {
        return $this->getMaxAltitude() - $this->getPassengerCount();
    }
}

class AirForceOne implements Airplane
{
    // ...

    public function getCruisingAltitude(): int
    {
        return $this->getMaxAltitude();
    }
}

class Cessna implements Airplane
{
    // ...

    public function getCruisingAltitude(): int
    {
        return $this->getMaxAltitude() - $this->getFuelExpenditure();
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-kiểm-tra-kiểu-dữ-liệu-phần-1" class="anchor" aria-hidden="true" href="#tránh-kiểm-tra-kiểu-dữ-liệu-phần-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh kiểm tra kiểu dữ liệu (phần 1)</h3>
<p>PHP là một ngôn ngữ không ràng buộc kiểu dữ liệu, nghĩa hàm có thể nhận bất kỳ kiểu nào.
Thỉnh thoảng thì chúng ta bị ảnh hưởng bởi sự tự do này và nó trở thành điều kiện để phải kiểm tra kiểu dữ liệu trong hàm.
Có nhiều cách để tránh phải làm việc đó.</p>
<p>Điều đầu tiên cần làm là tạo ra những API nhất quán.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">travelToTexas</span>(<span class="pl-s1"><span class="pl-c1">$</span>vehicle</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>vehicle</span> instanceof <span class="pl-v">Bicycle</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>vehicle</span>-&gt;<span class="pl-en">pedalTo</span>(<span class="pl-k">new</span> <span class="pl-v">Location</span>(<span class="pl-s">'texas'</span>));
    } <span class="pl-k">elseif</span> (<span class="pl-s1"><span class="pl-c1">$</span>vehicle</span> instanceof <span class="pl-v">Car</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>vehicle</span>-&gt;<span class="pl-en">driveTo</span>(<span class="pl-k">new</span> <span class="pl-v">Location</span>(<span class="pl-s">'texas'</span>));
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function travelToTexas($vehicle): void
{
    if ($vehicle instanceof Bicycle) {
        $vehicle->pedalTo(new Location('texas'));
    } elseif ($vehicle instanceof Car) {
        $vehicle->driveTo(new Location('texas'));
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">travelToTexas</span>(<span class="pl-smi">Traveler</span> <span class="pl-s1"><span class="pl-c1">$</span>vehicle</span>): <span class="pl-smi">void</span>
{
    <span class="pl-s1"><span class="pl-c1">$</span>vehicle</span>-&gt;<span class="pl-en">travelTo</span>(<span class="pl-k">new</span> <span class="pl-v">Location</span>(<span class="pl-s">'texas'</span>));
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function travelToTexas(Traveler $vehicle): void
{
    $vehicle->travelTo(new Location('texas'));
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-kiểm-tra-kiểu-dữ-liệu-phần-2" class="anchor" aria-hidden="true" href="#tránh-kiểm-tra-kiểu-dữ-liệu-phần-2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh kiểm tra kiểu dữ liệu (phần 2)</h3>
<p>Nếu bạn đang làm việc với các kiểu dữ liệu nguyên thủy như strings, integers, và arrays,
và sử dụng PHP 7+ và bạn không thể sử dụng tính đa hình nhưng bạn vẫn cảm thấy cần kiểm tra kiểu dữ liệu, hãy xem
<a href="http://php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration" rel="nofollow">type declaration</a>
hoặc strict mode. Nó cung cấp cho bạn kiểu static trên PHP standard.
Vấn đề thông thường khi kiểm tra kiểu dữ liệu là sẽ khiến code khó đọc nên tóm lại mất nhiều hơn là được.</p>
<p>Hãy giữ PHP nguyên thủy, viết tests cho tốt, và code reviews cẩn thận là được.
Nếu không thì chỉ còn cách định nghĩa theo kiểu nghiêm ngặt(strict type declaration) hoặc dùng strict mode.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">combine</span>(<span class="pl-s1"><span class="pl-c1">$</span>val1</span>, <span class="pl-s1"><span class="pl-c1">$</span>val2</span>): <span class="pl-smi">int</span>
{
    <span class="pl-k">if</span> (!<span class="pl-en">is_numeric</span>(<span class="pl-s1"><span class="pl-c1">$</span>val1</span>) || !<span class="pl-en">is_numeric</span>(<span class="pl-s1"><span class="pl-c1">$</span>val2</span>)) {
        <span class="pl-k">throw</span> <span class="pl-k">new</span> \<span class="pl-v">Exception</span>(<span class="pl-s">'Must be of type Number'</span>);
    }

    <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>val1</span> + <span class="pl-s1"><span class="pl-c1">$</span>val2</span>;
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function combine($val1, $val2): int
{
    if (!is_numeric($val1) || !is_numeric($val2)) {
        throw new \Exception('Must be of type Number');
    }

    return $val1 + $val2;
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">combine</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>val1</span>, <span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>val2</span>): <span class="pl-smi">int</span>
{
    <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span>val1</span> + <span class="pl-s1"><span class="pl-c1">$</span>val2</span>;
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function combine(int $val1, int $val2): int
{
    return $val1 + $val2;
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-xóa-dead-code" class="anchor" aria-hidden="true" href="#xóa-dead-code"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Xóa dead code</h3>
<p>Dead code thì cũng củ chuối giống như duplicate code. Không có lý do gì để giữ chúng.
Nếu đoạn code nào đó không được gọi, hãy xóa đi!
Sau này cần thì chỉ cần tìm lại phiên bản trước bằng git là được.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">oldRequestModule</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">void</span>
{
    <span class="pl-c">// ...</span>
}

<span class="pl-k">function</span> <span class="pl-en">newRequestModule</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">void</span>
{
    <span class="pl-c">// ...</span>
}

<span class="pl-s1"><span class="pl-c1">$</span>request</span> = <span class="pl-en">newRequestModule</span>(<span class="pl-s1"><span class="pl-c1">$</span>requestUrl</span>);
<span class="pl-en">inventoryTracker</span>(<span class="pl-s">'apples'</span>, <span class="pl-s1"><span class="pl-c1">$</span>request</span>, <span class="pl-s">'www.inventory-awesome.io'</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function oldRequestModule(string $url): void
{
    // ...
}

function newRequestModule(string $url): void
{
    // ...
}

$request = newRequestModule($requestUrl);
inventoryTracker('apples', $request, 'www.inventory-awesome.io');
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">requestModule</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">void</span>
{
    <span class="pl-c">// ...</span>
}

<span class="pl-s1"><span class="pl-c1">$</span>request</span> = <span class="pl-en">requestModule</span>(<span class="pl-s1"><span class="pl-c1">$</span>requestUrl</span>);
<span class="pl-en">inventoryTracker</span>(<span class="pl-s">'apples'</span>, <span class="pl-s1"><span class="pl-c1">$</span>request</span>, <span class="pl-s">'www.inventory-awesome.io'</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function requestModule(string $url): void
{
    // ...
}

$request = requestModule($requestUrl);
inventoryTracker('apples', $request, 'www.inventory-awesome.io');
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-đối-tượng-và-kiến-trúc-dữ-liệu" class="anchor" aria-hidden="true" href="#đối-tượng-và-kiến-trúc-dữ-liệu"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Đối tượng và kiến trúc dữ liệu</h2>
<h3><a id="user-content-sử-dụng-đối-tượng-đóng-gói" class="anchor" aria-hidden="true" href="#sử-dụng-đối-tượng-đóng-gói"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Sử dụng đối tượng đóng gói</h3>
<p>Trong PHP bạn có thể khai <code>public</code>, <code>protected</code> và <code>private</code> cho phương thức và thuộc tính.
Hãy sử dụng chúng để kiểm soát được sự thay đổi thuộc tính trong object.</p>
<ul>
<li>Khi bạn muốn nhiều hơn là chỉ nhận được thuộc tính của object,
thì ưu điểm là ta không cần phải tìm kiếm và thay đổi quyền mỗi khi truy cập vào object.</li>
<li>Giúp tạo validation đơn giản mỗi khi thực hiện <code>set</code>.</li>
<li>Đóng gói các thành phần bên trong.</li>
<li>Dễ dàng ghi log và xử lý lỗi khi get và set.</li>
<li>Kế thừa lớp, bạn có thể ghi đè những phương thức mặc định.</li>
<li>Bạn có thể lazy load các thuộc tính của object, giả sử nó được lấy từ máy chủ chẳng hạn.</li>
</ul>
<p>Thêm vào đó, đây là một phần của nguyên tắc <a href="#openclosed-principle-ocp">Open/Closed</a>.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">BankAccount</span>
{
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>balance</span> = <span class="pl-c1">1000</span>;
}

<span class="pl-s1"><span class="pl-c1">$</span>bankAccount</span> = <span class="pl-k">new</span> <span class="pl-v">BankAccount</span>();

<span class="pl-c">// Buy shoes...</span>
<span class="pl-s1"><span class="pl-c1">$</span>bankAccount</span>-&gt;<span class="pl-c1">balance</span> -= <span class="pl-c1">100</span>;</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class BankAccount
{
    public $balance = 1000;
}

$bankAccount = new BankAccount();

// Buy shoes...
$bankAccount->balance -= 100;
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">BankAccount</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>balance</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>balance</span> = <span class="pl-c1">1000</span>)
    {
      <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">balance</span> = <span class="pl-s1"><span class="pl-c1">$</span>balance</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">withdraw</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>amount</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>amount</span> &gt; <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">balance</span>) {
            <span class="pl-k">throw</span> <span class="pl-k">new</span> \<span class="pl-v">Exception</span>(<span class="pl-s">'Amount greater than available balance.'</span>);
        }

        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">balance</span> -= <span class="pl-s1"><span class="pl-c1">$</span>amount</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">deposit</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>amount</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">balance</span> += <span class="pl-s1"><span class="pl-c1">$</span>amount</span>;
    }

 &nbsp; &nbsp;<span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getBalance</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">balance</span>;
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>bankAccount</span> = <span class="pl-k">new</span> <span class="pl-v">BankAccount</span>();

<span class="pl-c">// Buy shoes...</span>
<span class="pl-s1"><span class="pl-c1">$</span>bankAccount</span>-&gt;<span class="pl-en">withdraw</span>(<span class="pl-s1"><span class="pl-c1">$</span>shoesPrice</span>);

<span class="pl-c">// Get balance</span>
<span class="pl-s1"><span class="pl-c1">$</span>balance</span> = <span class="pl-s1"><span class="pl-c1">$</span>bankAccount</span>-&gt;<span class="pl-en">getBalance</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class BankAccount
{
    private $balance;

    public function __construct(int $balance = 1000)
    {
      $this->balance = $balance;
    }

    public function withdraw(int $amount): void
    {
        if ($amount > $this->balance) {
            throw new \Exception('Amount greater than available balance.');
        }

        $this->balance -= $amount;
    }

    public function deposit(int $amount): void
    {
        $this->balance += $amount;
    }

 &nbsp; &nbsp;public function getBalance(): int
    {
        return $this->balance;
    }
}

$bankAccount = new BankAccount();

// Buy shoes...
$bankAccount->withdraw($shoesPrice);

// Get balance
$balance = $bankAccount->getBalance();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tạo-đối-tượng-có-chứa-thuộc-tính-hoặc-phương-thức-privateprotected" class="anchor" aria-hidden="true" href="#tạo-đối-tượng-có-chứa-thuộc-tính-hoặc-phương-thức-privateprotected"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tạo đối tượng có chứa thuộc tính hoặc phương thức private/protected</h3>
<ul>
<li>Phương thức và thuộc tính <code>public</code> khá nguy hiểm, bởi vì vài dòng code phía
bên ngoài có thể dễ dàng thay đổi chúng và bạn không thể kiểm soát được nó bị
thay đổi những gì. <strong>Thay đổi trong một lớp thì nguy hiểm cho tất cả các người dùng của lớp đó.</strong></li>
<li><code>protected</code> cũng nguy hiểm không kém, bởi vì chúng được cấp quyền ở tất cả các lớp con. Điều này có nghĩa là sự khác nhau giữa public và protected chỉ là cơ chế truy cập, nhưng tính đóng gói đảm bảo vẫn giữ nguyên. <strong>Sửa đổi trong lớp thì rất nguy hiểm cho các lớp con.</strong></li>
<li><code>private</code> sửa đổi đảm bảo rằng code <strong>sửa đổi chỉ nguy hiểm trong lớp đó</strong> (bạn sẽ được an toàn khi sửa và không có hiệu ứng <a href="http://www.urbandictionary.com/define.php?term=Jengaphobia&amp;defid=2494196" rel="nofollow">Jenga</a>).</li>
</ul>
<p>Do đó, hãy mặc định sử dụng <code>private</code> và <code>public/protected</code> khi bạn cần cung cấp sự truy cập cho các class bên ngoài.</p>
<p>Đọc thêm tại <a href="http://fabien.potencier.org/pragmatism-over-theory-protected-vs-private.html" rel="nofollow">blog post</a> được viết bởi <a href="https://github.com/fabpot">Fabien Potencier</a>.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-c1"><span class="pl-c1">$</span>name</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span> = <span class="pl-s1"><span class="pl-c1">$</span>name</span>;
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>employee</span> = <span class="pl-k">new</span> <span class="pl-v">Employee</span>(<span class="pl-s">'John Doe'</span>);
<span class="pl-k">echo</span> <span class="pl-s">'Employee name: '</span>.<span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-c1">name</span>; <span class="pl-c">// Employee name: John Doe</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Employee
{
    public $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }
}

$employee = new Employee('John Doe');
echo 'Employee name: '.$employee->name; // Employee name: John Doe
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>name</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span> = <span class="pl-s1"><span class="pl-c1">$</span>name</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getName</span>(): <span class="pl-smi">string</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span>;
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>employee</span> = <span class="pl-k">new</span> <span class="pl-v">Employee</span>(<span class="pl-s">'John Doe'</span>);
<span class="pl-k">echo</span> <span class="pl-s">'Employee name: '</span>.<span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">getName</span>(); <span class="pl-c">// Employee name: John Doe</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Employee
{
    private $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    public function getName(): string
    {
        return $this->name;
    }
}

$employee = new Employee('John Doe');
echo 'Employee name: '.$employee->getName(); // Employee name: John Doe
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-lớp" class="anchor" aria-hidden="true" href="#lớp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Lớp</h2>
<h3><a id="user-content-ưu-tiên-thành-phần-hơn-kế-thừa" class="anchor" aria-hidden="true" href="#ưu-tiên-thành-phần-hơn-kế-thừa"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Ưu tiên thành phần hơn kế thừa</h3>
<p>Như đã nói trong <a href="https://en.wikipedia.org/wiki/Design_Patterns" rel="nofollow"><em>Design Patterns</em></a> nổi tiếng của Gang of Four,
bạn nên ưu tiên sử dụng "kiểu thành phần" hơn là "kiểu kế thừa". Có nhiều lý do để sử dụng kiểu kế thừa và cũng có nhiều nguyên nhân để sử dụng kiểu thành phần.
Điểm chính của sự tối đa hóa này là nếu bạn thích theo kiểu kế thừa,
hãy thử suy nghĩ "kiểu thành phần" có thể giúp giải quyết vấn đề tốt hơn không. Vì có một vài trường hợp nó sẽ tốt hơn.</p>
<p>Có thể bạn sẽ tự hỏi, "khi nào thì nên dùng kế thừa?" Nó tùy thuộc vào từng vấn đề, khi nào thì kiểu kế thừa tốt hơn kiểu thành phần:</p>
<ol>
<li>Kiểu kế thừa đó đại diện cho một mối quan hệ "is-a" (Ví dụ: Người-&gt;Động vật) chứ không phải mối quan hệ "has-a" (Người dùng-&gt;Thông tin người dùng).</li>
<li>Bạn cần sử dụng lại code từ lớp cha (Người có thể di chuyển như động vật).</li>
<li>Bạn muốn khi sửa đổi lớp cha thì tất cả lớp có liên quan sẽ thay đổi dễ dàng.
(Thay đổi lượng calo của tất cả động vật khi chúng di chuyển).</li>
</ol>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Employee</span> 
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>name</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>email</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>email</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span> = <span class="pl-s1"><span class="pl-c1">$</span>name</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">email</span> = <span class="pl-s1"><span class="pl-c1">$</span>email</span>;
    }

    <span class="pl-c">// ...</span>
}

<span class="pl-c">// Chưa tốt vì Employees "có" thuế. </span>
<span class="pl-c">// EmployeeTaxData không phải là một loại của Employee</span>

<span class="pl-k">class</span> <span class="pl-v">EmployeeTaxData</span> <span class="pl-k">extends</span> <span class="pl-v">Employee</span> 
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>ssn</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>salary</span>;
    
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>email</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>ssn</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>salary</span>)
    {
        <span class="pl-smi">parent</span>::<span class="pl-en">__construct</span>(<span class="pl-s1"><span class="pl-c1">$</span>name</span>, <span class="pl-s1"><span class="pl-c1">$</span>email</span>);

        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">ssn</span> = <span class="pl-s1"><span class="pl-c1">$</span>ssn</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">salary</span> = <span class="pl-s1"><span class="pl-c1">$</span>salary</span>;
    }

    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Employee 
{
    private $name;
    private $email;

    public function __construct(string $name, string $email)
    {
        $this->name = $name;
        $this->email = $email;
    }

    // ...
}

// Chưa tốt vì Employees &quot;có&quot; thuế. 
// EmployeeTaxData không phải là một loại của Employee

class EmployeeTaxData extends Employee 
{
    private $ssn;
    private $salary;
    
    public function __construct(string $name, string $email, string $ssn, string $salary)
    {
        parent::__construct($name, $email);

        $this->ssn = $ssn;
        $this->salary = $salary;
    }

    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">EmployeeTaxData</span> 
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>ssn</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>salary</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>ssn</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>salary</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">ssn</span> = <span class="pl-s1"><span class="pl-c1">$</span>ssn</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">salary</span> = <span class="pl-s1"><span class="pl-c1">$</span>salary</span>;
    }

    <span class="pl-c">// ...</span>
}

<span class="pl-k">class</span> <span class="pl-v">Employee</span> 
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>name</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>email</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>taxData</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>name</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>email</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span> = <span class="pl-s1"><span class="pl-c1">$</span>name</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">email</span> = <span class="pl-s1"><span class="pl-c1">$</span>email</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setTaxData</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>ssn</span>, <span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>salary</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">taxData</span> = <span class="pl-k">new</span> <span class="pl-v">EmployeeTaxData</span>(<span class="pl-s1"><span class="pl-c1">$</span>ssn</span>, <span class="pl-s1"><span class="pl-c1">$</span>salary</span>);
    }

    <span class="pl-c">// ...</span>
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class EmployeeTaxData 
{
    private $ssn;
    private $salary;

    public function __construct(string $ssn, string $salary)
    {
        $this->ssn = $ssn;
        $this->salary = $salary;
    }

    // ...
}

class Employee 
{
    private $name;
    private $email;
    private $taxData;

    public function __construct(string $name, string $email)
    {
        $this->name = $name;
        $this->email = $email;
    }

    public function setTaxData(string $ssn, string $salary)
    {
        $this->taxData = new EmployeeTaxData($ssn, $salary);
    }

    // ...
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-tránh-viết-fluent-interfaces" class="anchor" aria-hidden="true" href="#tránh-viết-fluent-interfaces"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Tránh viết fluent interfaces</h3>
<p><a href="https://en.wikipedia.org/wiki/Fluent_interface" rel="nofollow">Fluent interface</a> là một API hướng đối tượng có mục đích cải thiện tính dễ đọc của source code bằng cách
sử dụng <a href="https://en.wikipedia.org/wiki/Method_chaining" rel="nofollow">Method chaining</a>.</p>
<p>Trong một số ngữ cảnh, thường là khi xây dựng object nơi mà pattern này giảm tính rườm rà của code (ví dụ <a href="https://phpunit.de/manual/current/en/test-doubles.html" rel="nofollow">PHPUnit Mock Builder</a>
hoặc <a href="http://docs.doctrine-project.org/projects/doctrine-dbal/en/latest/reference/query-builder.html" rel="nofollow">Doctrine Query Builder</a>),
sẽ gây ra một số thiệt hại như sau:</p>
<ol>
<li>Phá vỡ <a href="https://en.wikipedia.org/wiki/Encapsulation_%28object-oriented_programming%29" rel="nofollow">Encapsulation</a></li>
<li>Phá vỡ <a href="https://en.wikipedia.org/wiki/Decorator_pattern" rel="nofollow">Decorators</a></li>
<li>Khó tạo <a href="https://en.wikipedia.org/wiki/Mock_object" rel="nofollow">mock</a> hơn trong test suite</li>
<li>Khiến cho khó đọc "sự khác nhau giữa các file" hơn khi commit code</li>
</ol>
<p>Để biết thêm thông tin chi tiết, vui lòng đọc <a href="https://ocramius.github.io/blog/fluent-interfaces-are-evil/" rel="nofollow">bài viết</a>
được viết bởi <a href="https://github.com/Ocramius">Marco Pivetta</a>.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Car</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>make</span> = <span class="pl-s">'Honda'</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>model</span> = <span class="pl-s">'Accord'</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>color</span> = <span class="pl-s">'white'</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setMake</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>make</span>): <span class="pl-smi">self</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">make</span> = <span class="pl-s1"><span class="pl-c1">$</span>make</span>;

        <span class="pl-c">// NOTE: Returning this for chaining</span>
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setModel</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>model</span>): <span class="pl-smi">self</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">model</span> = <span class="pl-s1"><span class="pl-c1">$</span>model</span>;

        <span class="pl-c">// NOTE: Returning this for chaining</span>
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setColor</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>color</span>): <span class="pl-smi">self</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">color</span> = <span class="pl-s1"><span class="pl-c1">$</span>color</span>;

        <span class="pl-c">// NOTE: Returning this for chaining</span>
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">dump</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-en">var_dump</span>(<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">make</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">model</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">color</span>);
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>car</span> = (<span class="pl-k">new</span> <span class="pl-v">Car</span>())
  -&gt;<span class="pl-en">setColor</span>(<span class="pl-s">'pink'</span>)
  -&gt;<span class="pl-en">setMake</span>(<span class="pl-s">'Ford'</span>)
  -&gt;<span class="pl-en">setModel</span>(<span class="pl-s">'F-150'</span>)
  -&gt;<span class="pl-en">dump</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Car
{
    private $make = 'Honda';
    private $model = 'Accord';
    private $color = 'white';

    public function setMake(string $make): self
    {
        $this->make = $make;

        // NOTE: Returning this for chaining
        return $this;
    }

    public function setModel(string $model): self
    {
        $this->model = $model;

        // NOTE: Returning this for chaining
        return $this;
    }

    public function setColor(string $color): self
    {
        $this->color = $color;

        // NOTE: Returning this for chaining
        return $this;
    }

    public function dump(): void
    {
        var_dump($this->make, $this->model, $this->color);
    }
}

$car = (new Car())
  ->setColor('pink')
  ->setMake('Ford')
  ->setModel('F-150')
  ->dump();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Car</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>make</span> = <span class="pl-s">'Honda'</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>model</span> = <span class="pl-s">'Accord'</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>color</span> = <span class="pl-s">'white'</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setMake</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>make</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">make</span> = <span class="pl-s1"><span class="pl-c1">$</span>make</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setModel</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>model</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">model</span> = <span class="pl-s1"><span class="pl-c1">$</span>model</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setColor</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>color</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">color</span> = <span class="pl-s1"><span class="pl-c1">$</span>color</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">dump</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-en">var_dump</span>(<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">make</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">model</span>, <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">color</span>);
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>car</span> = <span class="pl-k">new</span> <span class="pl-v">Car</span>();
<span class="pl-s1"><span class="pl-c1">$</span>car</span>-&gt;<span class="pl-en">setColor</span>(<span class="pl-s">'pink'</span>);
<span class="pl-s1"><span class="pl-c1">$</span>car</span>-&gt;<span class="pl-en">setMake</span>(<span class="pl-s">'Ford'</span>);
<span class="pl-s1"><span class="pl-c1">$</span>car</span>-&gt;<span class="pl-en">setModel</span>(<span class="pl-s">'F-150'</span>);
<span class="pl-s1"><span class="pl-c1">$</span>car</span>-&gt;<span class="pl-en">dump</span>();</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Car
{
    private $make = 'Honda';
    private $model = 'Accord';
    private $color = 'white';

    public function setMake(string $make): void
    {
        $this->make = $make;
    }

    public function setModel(string $model): void
    {
        $this->model = $model;
    }

    public function setColor(string $color): void
    {
        $this->color = $color;
    }

    public function dump(): void
    {
        var_dump($this->make, $this->model, $this->color);
    }
}

$car = new Car();
$car->setColor('pink');
$car->setMake('Ford');
$car->setModel('F-150');
$car->dump();
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-solid" class="anchor" aria-hidden="true" href="#solid"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>SOLID</h2>
<p><strong>SOLID</strong> là từ viết tắt được đưa ra bởi Michael Feathers cho 5 nguyên lý đầu tiên của Robert Martin, 5 nguyên tắc cơ bản của lập trình hướng đối tượng.</p>
<ul>
<li><a href="#single-responsibility-principle-srp">S: Nguyên lý trách nhiệm duy nhất (SRP)</a></li>
<li><a href="#openclosed-principle-ocp">O: Nguyên lý Đóng/Mở (OCP)</a></li>
<li><a href="#liskov-substitution-principle-lsp">L: Nguyên lý thay thế Liskov (LSP)</a></li>
<li><a href="#interface-segregation-principle-isp">I: Nguyên lý phân tách interface (ISP)</a></li>
<li><a href="#dependency-inversion-principle-dip">D: Nguyên lý đảo ngược dependencies (DIP)</a></li>
</ul>
<h3><a id="user-content-nguyên-lý-trách-nhiệm-duy-nhất-srp" class="anchor" aria-hidden="true" href="#nguyên-lý-trách-nhiệm-duy-nhất-srp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Nguyên lý trách nhiệm duy nhất (SRP)</h3>
<p>Như đã đề cập trong cuốn Clean Code, "Không nên có nhiều hơn một lý do để thay đổi class".
Viết một class với thật nhiều chức năng thì quá sướng. Vấn đề là class không có khái niệm liên kết và nó có khá nhiều lý do để thay đổi.
Nếu quá nhiều chức năng trong một class thì khi thay đổi gì đó mình không biết được hết những ảnh hưởng của nó đến các chức năng khác trong các module liên quan.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">UserSettings</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>user</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">User</span> <span class="pl-s1"><span class="pl-c1">$</span>user</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">user</span> = <span class="pl-s1"><span class="pl-c1">$</span>user</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">changeSettings</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>settings</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">verifyCredentials</span>()) {
            <span class="pl-c">// ...</span>
        }
    }

    <span class="pl-k">private</span> <span class="pl-k">function</span> <span class="pl-en">verifyCredentials</span>(): <span class="pl-smi">bool</span>
    {
        <span class="pl-c">// ...</span>
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class UserSettings
{
    private $user;

    public function __construct(User $user)
    {
        $this->user = $user;
    }

    public function changeSettings(array $settings): void
    {
        if ($this->verifyCredentials()) {
            // ...
        }
    }

    private function verifyCredentials(): bool
    {
        // ...
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">UserAuth</span> 
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>user</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">User</span> <span class="pl-s1"><span class="pl-c1">$</span>user</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">user</span> = <span class="pl-s1"><span class="pl-c1">$</span>user</span>;
    }
    
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">verifyCredentials</span>(): <span class="pl-smi">bool</span>
    {
        <span class="pl-c">// ...</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">UserSettings</span> 
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>user</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>auth</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">User</span> <span class="pl-s1"><span class="pl-c1">$</span>user</span>) 
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">user</span> = <span class="pl-s1"><span class="pl-c1">$</span>user</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">auth</span> = <span class="pl-k">new</span> <span class="pl-v">UserAuth</span>(<span class="pl-s1"><span class="pl-c1">$</span>user</span>);
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">changeSettings</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>settings</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">auth</span>-&gt;<span class="pl-en">verifyCredentials</span>()) {
            <span class="pl-c">// ...</span>
        }
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class UserAuth 
{
    private $user;

    public function __construct(User $user)
    {
        $this->user = $user;
    }
    
    public function verifyCredentials(): bool
    {
        // ...
    }
}

class UserSettings 
{
    private $user;
    private $auth;

    public function __construct(User $user) 
    {
        $this->user = $user;
        $this->auth = new UserAuth($user);
    }

    public function changeSettings(array $settings): void
    {
        if ($this->auth->verifyCredentials()) {
            // ...
        }
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-nguyên-lý-đóngmở-ocp" class="anchor" aria-hidden="true" href="#nguyên-lý-đóngmở-ocp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Nguyên lý Đóng/Mở (OCP)</h3>
<p>Như đã đề cập bởi Bertrand Meyer, "thực thể phần mềm (lớp, modules, hàm,
etc...) nên cho phép mở rộng, nhưng không cho phép sửa đổi." Điều đó có nghĩa là gì? Nguyên lý này đơn giản là nên cho phép người dùng
thêm mới mà không được thay đổi code hiện tại.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">abstract</span> <span class="pl-k">class</span> <span class="pl-v">Adapter</span>
{
    <span class="pl-k">protected</span> <span class="pl-c1"><span class="pl-c1">$</span>name</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getName</span>(): <span class="pl-smi">string</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">AjaxAdapter</span> <span class="pl-k">extends</span> <span class="pl-v">Adapter</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>()
    {
        <span class="pl-smi">parent</span>::<span class="pl-en">__construct</span>();

        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span> = <span class="pl-s">'ajaxAdapter'</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">NodeAdapter</span> <span class="pl-k">extends</span> <span class="pl-v">Adapter</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>()
    {
        <span class="pl-smi">parent</span>::<span class="pl-en">__construct</span>();

        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">name</span> = <span class="pl-s">'nodeAdapter'</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">HttpRequester</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>adapter</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">Adapter</span> <span class="pl-s1"><span class="pl-c1">$</span>adapter</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">adapter</span> = <span class="pl-s1"><span class="pl-c1">$</span>adapter</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">fetch</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span>adapterName</span> = <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">adapter</span>-&gt;<span class="pl-en">getName</span>();

        <span class="pl-k">if</span> (<span class="pl-s1"><span class="pl-c1">$</span>adapterName</span> === <span class="pl-s">'ajaxAdapter'</span>) {
            <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">makeAjaxCall</span>(<span class="pl-s1"><span class="pl-c1">$</span>url</span>);
        } <span class="pl-k">elseif</span> (<span class="pl-s1"><span class="pl-c1">$</span>adapterName</span> === <span class="pl-s">'httpNodeAdapter'</span>) {
            <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-en">makeHttpCall</span>(<span class="pl-s1"><span class="pl-c1">$</span>url</span>);
        }
    }

    <span class="pl-k">private</span> <span class="pl-k">function</span> <span class="pl-en">makeAjaxCall</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>
    {
        <span class="pl-c">// request and return promise</span>
    }

    <span class="pl-k">private</span> <span class="pl-k">function</span> <span class="pl-en">makeHttpCall</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>
    {
        <span class="pl-c">// request and return promise</span>
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="abstract class Adapter
{
    protected $name;

    public function getName(): string
    {
        return $this->name;
    }
}

class AjaxAdapter extends Adapter
{
    public function __construct()
    {
        parent::__construct();

        $this->name = 'ajaxAdapter';
    }
}

class NodeAdapter extends Adapter
{
    public function __construct()
    {
        parent::__construct();

        $this->name = 'nodeAdapter';
    }
}

class HttpRequester
{
    private $adapter;

    public function __construct(Adapter $adapter)
    {
        $this->adapter = $adapter;
    }

    public function fetch(string $url): Promise
    {
        $adapterName = $this->adapter->getName();

        if ($adapterName === 'ajaxAdapter') {
            return $this->makeAjaxCall($url);
        } elseif ($adapterName === 'httpNodeAdapter') {
            return $this->makeHttpCall($url);
        }
    }

    private function makeAjaxCall(string $url): Promise
    {
        // request and return promise
    }

    private function makeHttpCall(string $url): Promise
    {
        // request and return promise
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">interface</span> <span class="pl-v">Adapter</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">request</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>;
}

<span class="pl-k">class</span> <span class="pl-v">AjaxAdapter</span> <span class="pl-k">implements</span> <span class="pl-v">Adapter</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">request</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>
    {
        <span class="pl-c">// request and return promise</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">NodeAdapter</span> <span class="pl-k">implements</span> <span class="pl-v">Adapter</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">request</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>
    {
        <span class="pl-c">// request and return promise</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">HttpRequester</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>adapter</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">Adapter</span> <span class="pl-s1"><span class="pl-c1">$</span>adapter</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">adapter</span> = <span class="pl-s1"><span class="pl-c1">$</span>adapter</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">fetch</span>(<span class="pl-smi">string</span> <span class="pl-s1"><span class="pl-c1">$</span>url</span>): <span class="pl-smi">Promise</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">adapter</span>-&gt;<span class="pl-en">request</span>(<span class="pl-s1"><span class="pl-c1">$</span>url</span>);
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="interface Adapter
{
    public function request(string $url): Promise;
}

class AjaxAdapter implements Adapter
{
    public function request(string $url): Promise
    {
        // request and return promise
    }
}

class NodeAdapter implements Adapter
{
    public function request(string $url): Promise
    {
        // request and return promise
    }
}

class HttpRequester
{
    private $adapter;

    public function __construct(Adapter $adapter)
    {
        $this->adapter = $adapter;
    }

    public function fetch(string $url): Promise
    {
        return $this->adapter->request($url);
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-nguyên-lý-thay-thế-liskov-lsp" class="anchor" aria-hidden="true" href="#nguyên-lý-thay-thế-liskov-lsp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Nguyên lý thay thế Liskov (LSP)</h3>
<p>Nguyên lý này được định nghĩa như sau "Nếu S là phụ thuộc của T, thì object của T có thể <strong>được thay thế</strong> bởi object của S
(nghĩa là object của S có thể thay thế object của T) mà không làm thay đổi các thuộc tính của chương trình(tính đúng đắn, công việc thực hiện,...)"</p>
<p>Để dễ hiểu hơn, nếu bạn có một class cha và một class con,
sau đó class cha và class con có thể được sử dụng hoán đổi cho nhau mà không sai kết quả trả về.
Có thể vẫn còn khó hiểu, hãy xem ví dụ cơ bản Square-Rectangle bên dưới.</p>
<p>Trong toán học, hình vuông là hình chữ nhật, nhưng nếu bạn sử dụng quan hệ "is-a" qua kế thừa, bạn sẽ gặp rắc rối.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Rectangle</span>
{
    <span class="pl-k">protected</span> <span class="pl-c1"><span class="pl-c1">$</span>width</span> = <span class="pl-c1">0</span>;
    <span class="pl-k">protected</span> <span class="pl-c1"><span class="pl-c1">$</span>height</span> = <span class="pl-c1">0</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">render</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>area</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ...</span>
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setWidth</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>width</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">width</span> = <span class="pl-s1"><span class="pl-c1">$</span>width</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setHeight</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>height</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">height</span> = <span class="pl-s1"><span class="pl-c1">$</span>height</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getArea</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">width</span> * <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">height</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">Square</span> <span class="pl-k">extends</span> <span class="pl-v">Rectangle</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setWidth</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>width</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">width</span> = <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">height</span> = <span class="pl-s1"><span class="pl-c1">$</span>width</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">setHeight</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>height</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">width</span> = <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">height</span> = <span class="pl-s1"><span class="pl-c1">$</span>height</span>;
    }
}

<span class="pl-c">/**</span>
<span class="pl-c"> * @param Rectangle[] $rectangles</span>
<span class="pl-c"> */</span>
<span class="pl-k">function</span> <span class="pl-en">renderLargeRectangles</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>rectangles</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>rectangles</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>-&gt;<span class="pl-en">setWidth</span>(<span class="pl-c1">4</span>);
        <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>-&gt;<span class="pl-en">setHeight</span>(<span class="pl-c1">5</span>);
        <span class="pl-s1"><span class="pl-c1">$</span>area</span> = <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>-&gt;<span class="pl-en">getArea</span>(); <span class="pl-c">// Lỗi rồi: Đoạn này sẽ trả về 25, nhưng 20 mới là kết quả đúng.</span>
        <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>-&gt;<span class="pl-en">render</span>(<span class="pl-s1"><span class="pl-c1">$</span>area</span>);
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>rectangles</span> = [<span class="pl-k">new</span> <span class="pl-v">Rectangle</span>(), <span class="pl-k">new</span> <span class="pl-v">Rectangle</span>(), <span class="pl-k">new</span> <span class="pl-v">Square</span>()];
<span class="pl-en">renderLargeRectangles</span>(<span class="pl-s1"><span class="pl-c1">$</span>rectangles</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Rectangle
{
    protected $width = 0;
    protected $height = 0;

    public function render(int $area): void
    {
        // ...
    }

    public function setWidth(int $width): void
    {
        $this->width = $width;
    }

    public function setHeight(int $height): void
    {
        $this->height = $height;
    }

    public function getArea(): int
    {
        return $this->width * $this->height;
    }
}

class Square extends Rectangle
{
    public function setWidth(int $width): void
    {
        $this->width = $this->height = $width;
    }

    public function setHeight(int $height): void
    {
        $this->width = $this->height = $height;
    }
}

/**
 * @param Rectangle[] $rectangles
 */
function renderLargeRectangles(array $rectangles): void
{
    foreach ($rectangles as $rectangle) {
        $rectangle->setWidth(4);
        $rectangle->setHeight(5);
        $area = $rectangle->getArea(); // Lỗi rồi: Đoạn này sẽ trả về 25, nhưng 20 mới là kết quả đúng.
        $rectangle->render($area);
    }
}

$rectangles = [new Rectangle(), new Rectangle(), new Square()];
renderLargeRectangles($rectangles);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">abstract</span> <span class="pl-k">class</span> <span class="pl-v">Shape</span>
{
    <span class="pl-k">abstract</span> <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getArea</span>(): <span class="pl-smi">int</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">render</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>area</span>): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ...</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">Rectangle</span> <span class="pl-k">extends</span> <span class="pl-v">Shape</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>width</span>;
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>height</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>width</span>, <span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>height</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">width</span> = <span class="pl-s1"><span class="pl-c1">$</span>width</span>;
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">height</span> = <span class="pl-s1"><span class="pl-c1">$</span>height</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getArea</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">width</span> * <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">height</span>;
    }
}

<span class="pl-k">class</span> <span class="pl-v">Square</span> <span class="pl-k">extends</span> <span class="pl-v">Shape</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>length</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">int</span> <span class="pl-s1"><span class="pl-c1">$</span>length</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">length</span> = <span class="pl-s1"><span class="pl-c1">$</span>length</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">getArea</span>(): <span class="pl-smi">int</span>
    {
        <span class="pl-k">return</span> <span class="pl-en">pow</span>(<span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">length</span>, <span class="pl-c1">2</span>);
    }
}

<span class="pl-c">/**</span>
<span class="pl-c"> * @param Rectangle[] $rectangles</span>
<span class="pl-c"> */</span>
<span class="pl-k">function</span> <span class="pl-en">renderLargeRectangles</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>rectangles</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>rectangles</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>area</span> = <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>-&gt;<span class="pl-en">getArea</span>(); 
        <span class="pl-s1"><span class="pl-c1">$</span>rectangle</span>-&gt;<span class="pl-en">render</span>(<span class="pl-s1"><span class="pl-c1">$</span>area</span>);
    }
}

<span class="pl-s1"><span class="pl-c1">$</span>shapes</span> = [<span class="pl-k">new</span> <span class="pl-v">Rectangle</span>(<span class="pl-c1">4</span>, <span class="pl-c1">5</span>), <span class="pl-k">new</span> <span class="pl-v">Rectangle</span>(<span class="pl-c1">4</span>, <span class="pl-c1">5</span>), <span class="pl-k">new</span> <span class="pl-v">Square</span>(<span class="pl-c1">5</span>)];
<span class="pl-en">renderLargeRectangles</span>(<span class="pl-s1"><span class="pl-c1">$</span>shapes</span>);</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="abstract class Shape
{
    abstract public function getArea(): int;

    public function render(int $area): void
    {
        // ...
    }
}

class Rectangle extends Shape
{
    private $width;
    private $height;

    public function __construct(int $width, int $height)
    {
        $this->width = $width;
        $this->height = $height;
    }

    public function getArea(): int
    {
        return $this->width * $this->height;
    }
}

class Square extends Shape
{
    private $length;

    public function __construct(int $length)
    {
        $this->length = $length;
    }

    public function getArea(): int
    {
        return pow($this->length, 2);
    }
}

/**
 * @param Rectangle[] $rectangles
 */
function renderLargeRectangles(array $rectangles): void
{
    foreach ($rectangles as $rectangle) {
        $area = $rectangle->getArea(); 
        $rectangle->render($area);
    }
}

$shapes = [new Rectangle(4, 5), new Rectangle(4, 5), new Square(5)];
renderLargeRectangles($shapes);
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-nguyên-lý-phân-tách-interface-isp" class="anchor" aria-hidden="true" href="#nguyên-lý-phân-tách-interface-isp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Nguyên lý phân tách interface (ISP)</h3>
<p>ISP đề cập rằng "Không nên ép người dùng phải phụ thuộc vào interface mà họ không sử dụng."</p>
<p>Để hiểu ý nghĩa của nguyên tắc này, hãy nhìn vào những class yêu cầu một số lượng lớn các object cần phải inject vào để sử dụng.
Không yêu cầu người dùng phải inject số lượng lớn các tùy chọn là một lợi thế, bởi vì hầu hết chúng không cần thiết.
Hãy coi chúng là tùy chọn(có thể không dùng) để giúp cho interface bớt phình to.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">interface</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">eat</span>(): <span class="pl-smi">void</span>;
}

<span class="pl-k">class</span> <span class="pl-v">Human</span> <span class="pl-k">implements</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ....working</span>
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">eat</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ...... eating in lunch break</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">Robot</span> <span class="pl-k">implements</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">//.... working much more</span>
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">eat</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">//.... robot can't eat, but it must implement this method</span>
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="interface Employee
{
    public function work(): void;

    public function eat(): void;
}

class Human implements Employee
{
    public function work(): void
    {
        // ....working
    }

    public function eat(): void
    {
        // ...... eating in lunch break
    }
}

class Robot implements Employee
{
    public function work(): void
    {
        //.... working much more
    }

    public function eat(): void
    {
        //.... robot can't eat, but it must implement this method
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<p>Không phải tất cả worker đều là employee, nhưng employee là một worker.</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">interface</span> <span class="pl-v">Workable</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>;
}

<span class="pl-k">interface</span> <span class="pl-v">Feedable</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">eat</span>(): <span class="pl-smi">void</span>;
}

<span class="pl-k">interface</span> <span class="pl-v">Employee</span> <span class="pl-k">extends</span> <span class="pl-v">Feedable</span>, <span class="pl-v">Workable</span>
{
}

<span class="pl-k">class</span> <span class="pl-v">Human</span> <span class="pl-k">implements</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ....working</span>
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">eat</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">//.... eating in lunch break</span>
    }
}

<span class="pl-c">// robot can only work</span>
<span class="pl-k">class</span> <span class="pl-v">Robot</span> <span class="pl-k">implements</span> <span class="pl-v">Workable</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ....working</span>
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="interface Workable
{
    public function work(): void;
}

interface Feedable
{
    public function eat(): void;
}

interface Employee extends Feedable, Workable
{
}

class Human implements Employee
{
    public function work(): void
    {
        // ....working
    }

    public function eat(): void
    {
        //.... eating in lunch break
    }
}

// robot can only work
class Robot implements Workable
{
    public function work(): void
    {
        // ....working
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h3><a id="user-content-nguyên-lý-đảo-ngược-dependencies-dip" class="anchor" aria-hidden="true" href="#nguyên-lý-đảo-ngược-dependencies-dip"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Nguyên lý đảo ngược dependencies (DIP)</h3>
<p>Nguyên lý này đề cập 2 vấn đề cơ bản:</p>
<ol>
<li>Module cấp cao không nên phụ thuộc vào module cấp thấp. Cả hai nên phụ thuộc vào abstract.</li>
<li>Abstract không nên phụ thuộc vào chi tiết, mà phải ngược lại.</li>
</ol>
<p>Hơi khó hiểu một chút đúng không? Nhưng nếu bạn làm việc với PHP frameworks (ví dụ Symfony), bạn sẽ thấy nguyên tắc này được áp dụng trên Dependency
Injection(DI). Một lợi ích lớn của việc này là chúng giảm sự trùng lặp giữa các modules. Trùng lặp thì tất nhiên Chưa tốt vì
chúng khiến code khó refactor.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">class</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ....working</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">Robot</span> <span class="pl-k">extends</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">//.... working much more</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">Manager</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>employee</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">Employee</span> <span class="pl-s1"><span class="pl-c1">$</span>employee</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">employee</span> = <span class="pl-s1"><span class="pl-c1">$</span>employee</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">manage</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">employee</span>-&gt;<span class="pl-en">work</span>();
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="class Employee
{
    public function work(): void
    {
        // ....working
    }
}

class Robot extends Employee
{
    public function work(): void
    {
        //.... working much more
    }
}

class Manager
{
    private $employee;

    public function __construct(Employee $employee)
    {
        $this->employee = $employee;
    }

    public function manage(): void
    {
        $this->employee->work();
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">interface</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>;
}

<span class="pl-k">class</span> <span class="pl-v">Human</span> <span class="pl-k">implements</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">// ....working</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">Robot</span> <span class="pl-k">implements</span> <span class="pl-v">Employee</span>
{
    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">work</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-c">//.... working much more</span>
    }
}

<span class="pl-k">class</span> <span class="pl-v">Manager</span>
{
    <span class="pl-k">private</span> <span class="pl-c1"><span class="pl-c1">$</span>employee</span>;

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">__construct</span>(<span class="pl-smi">Employee</span> <span class="pl-s1"><span class="pl-c1">$</span>employee</span>)
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">employee</span> = <span class="pl-s1"><span class="pl-c1">$</span>employee</span>;
    }

    <span class="pl-k">public</span> <span class="pl-k">function</span> <span class="pl-en">manage</span>(): <span class="pl-smi">void</span>
    {
        <span class="pl-s1"><span class="pl-c1">$</span><span class="pl-smi">this</span></span>-&gt;<span class="pl-c1">employee</span>-&gt;<span class="pl-en">work</span>();
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="interface Employee
{
    public function work(): void;
}

class Human implements Employee
{
    public function work(): void
    {
        // ....working
    }
}

class Robot implements Employee
{
    public function work(): void
    {
        //.... working much more
    }
}

class Manager
{
    private $employee;

    public function __construct(Employee $employee)
    {
        $this->employee = $employee;
    }

    public function manage(): void
    {
        $this->employee->work();
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-nguyên-lý-đừng-lặp-lại-chính-mình-dry" class="anchor" aria-hidden="true" href="#nguyên-lý-đừng-lặp-lại-chính-mình-dry"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Nguyên lý đừng lặp lại chính mình (DRY)</h2>
<p>Đọc hiểu về nguyên lý <a href="https://en.wikipedia.org/wiki/Don%27t_repeat_yourself" rel="nofollow">DRY</a></p>
<p>Tốt nhất nên chống lặp code ngay khi có thể. Vì lặp code không tốt tí nào, khi bạn muốn thay đổi logic bạn cần phải sửa nhiều chỗ.</p>
<p>Hãy tưởng tượng bạn đang vận hành một nhà hàng và bạn theo dõi lượng hàng tồn kho của bạn: cà chua, hành, tỏi, gia vị,...
Nếu bạn có nhiều danh sách để quản lý chúng, bạn cần cập nhật tất cả các danh sách đó mỗi khi bạn bán một đĩa thức ăn.
Nhưng nếu như bạn chỉ có 1 danh sách, thì chỉ cần cập nhật ở một nơi!</p>
<p>Thỉnh thoảng vẫn có lặp code bởi vì bạn có hai hoặc nhiều hơn những thứ khác nhau, có nhiều điểm chung, nhưng sự khác nhau
giữa chúng buộc bạn phải chia ra 2 hàm làm rất nhiều việc.
Để xóa bỏ lặp code, cần tạo ra một abstract có thể xử lý sự khác biệt giữa chúng với chỉ 1 hàm/module/lớp.</p>
<p>Tạo ra được abstract tốt rất quan trọng và khó, đó là lý do tại sao bạn nên dựa theo các nguyên lý <a href="#solid">SOLID</a> được đưa ra tại mục <a href="#l%E1%BB%9Bp">Lớp</a>.
Abstract củ chuối có thể sẽ tệ hại hơn là lặp code, hãy cẩn thận!
Nếu có thể tạo một abstract tốt, hãy tạo nó! Đừng lặp lại code, nếu không bạn sẽ phải rất cực khổ mỗi khi muốn sửa đổi gì đó.</p>
<p><strong>Chưa tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">showDeveloperList</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>developers</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>developers</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>developer</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>expectedSalary</span> = <span class="pl-s1"><span class="pl-c1">$</span>developer</span>-&gt;<span class="pl-en">calculateExpectedSalary</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>experience</span> = <span class="pl-s1"><span class="pl-c1">$</span>developer</span>-&gt;<span class="pl-en">getExperience</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>githubLink</span> = <span class="pl-s1"><span class="pl-c1">$</span>developer</span>-&gt;<span class="pl-en">getGithubLink</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>data</span> = [
            <span class="pl-s1"><span class="pl-c1">$</span>expectedSalary</span>,
            <span class="pl-s1"><span class="pl-c1">$</span>experience</span>,
            <span class="pl-s1"><span class="pl-c1">$</span>githubLink</span>
        ];

        <span class="pl-en">render</span>(<span class="pl-s1"><span class="pl-c1">$</span>data</span>);
    }
}

<span class="pl-k">function</span> <span class="pl-en">showManagerList</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>managers</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>managers</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>manager</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>expectedSalary</span> = <span class="pl-s1"><span class="pl-c1">$</span>manager</span>-&gt;<span class="pl-en">calculateExpectedSalary</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>experience</span> = <span class="pl-s1"><span class="pl-c1">$</span>manager</span>-&gt;<span class="pl-en">getExperience</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>githubLink</span> = <span class="pl-s1"><span class="pl-c1">$</span>manager</span>-&gt;<span class="pl-en">getGithubLink</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>data</span> = [
            <span class="pl-s1"><span class="pl-c1">$</span>expectedSalary</span>,
            <span class="pl-s1"><span class="pl-c1">$</span>experience</span>,
            <span class="pl-s1"><span class="pl-c1">$</span>githubLink</span>
        ];

        <span class="pl-en">render</span>(<span class="pl-s1"><span class="pl-c1">$</span>data</span>);
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function showDeveloperList(array $developers): void
{
    foreach ($developers as $developer) {
        $expectedSalary = $developer->calculateExpectedSalary();
        $experience = $developer->getExperience();
        $githubLink = $developer->getGithubLink();
        $data = [
            $expectedSalary,
            $experience,
            $githubLink
        ];

        render($data);
    }
}

function showManagerList(array $managers): void
{
    foreach ($managers as $manager) {
        $expectedSalary = $manager->calculateExpectedSalary();
        $experience = $manager->getExperience();
        $githubLink = $manager->getGithubLink();
        $data = [
            $expectedSalary,
            $experience,
            $githubLink
        ];

        render($data);
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Tốt:</strong></p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">showList</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>employees</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>employees</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>employee</span>) {
        <span class="pl-s1"><span class="pl-c1">$</span>expectedSalary</span> = <span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">calculateExpectedSalary</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>experience</span> = <span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">getExperience</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>githubLink</span> = <span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">getGithubLink</span>();
        <span class="pl-s1"><span class="pl-c1">$</span>data</span> = [
            <span class="pl-s1"><span class="pl-c1">$</span>expectedSalary</span>,
            <span class="pl-s1"><span class="pl-c1">$</span>experience</span>,
            <span class="pl-s1"><span class="pl-c1">$</span>githubLink</span>
        ];

        <span class="pl-en">render</span>(<span class="pl-s1"><span class="pl-c1">$</span>data</span>);
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function showList(array $employees): void
{
    foreach ($employees as $employee) {
        $expectedSalary = $employee->calculateExpectedSalary();
        $experience = $employee->getExperience();
        $githubLink = $employee->getGithubLink();
        $data = [
            $expectedSalary,
            $experience,
            $githubLink
        ];

        render($data);
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Rất tốt:</strong></p>
<p>Sử dụng một phiên bản gọn hơn</p>
<div class="highlight highlight-text-html-php position-relative overflow-auto"><pre><span class="pl-k">function</span> <span class="pl-en">showList</span>(<span class="pl-smi">array</span> <span class="pl-s1"><span class="pl-c1">$</span>employees</span>): <span class="pl-smi">void</span>
{
    <span class="pl-k">foreach</span> (<span class="pl-s1"><span class="pl-c1">$</span>employees</span> <span class="pl-k">as</span> <span class="pl-s1"><span class="pl-c1">$</span>employee</span>) {
        <span class="pl-en">render</span>([
            <span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">calculateExpectedSalary</span>(),
            <span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">getExperience</span>(),
            <span class="pl-s1"><span class="pl-c1">$</span>employee</span>-&gt;<span class="pl-en">getGithubLink</span>()
        ]);
    }
}</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="function showList(array $employees): void
{
    foreach ($employees as $employee) {
        render([
            $employee->calculateExpectedSalary(),
            $employee->getExperience(),
            $employee->getGithubLink()
        ]);
    }
}
" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path fill-rule="evenodd" d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 010 1.5h-1.5a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-1.5a.75.75 0 011.5 0v1.5A1.75 1.75 0 019.25 16h-7.5A1.75 1.75 0 010 14.25v-7.5z"></path><path fill-rule="evenodd" d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0114.25 11h-7.5A1.75 1.75 0 015 9.25v-7.5zm1.75-.25a.25.25 0 00-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25v-7.5a.25.25 0 00-.25-.25h-7.5z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-text-success d-none m-2">
    <path fill-rule="evenodd" d="M13.78 4.22a.75.75 0 010 1.06l-7.25 7.25a.75.75 0 01-1.06 0L2.22 9.28a.75.75 0 011.06-1.06L6 10.94l6.72-6.72a.75.75 0 011.06 0z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
<h2><a id="user-content-các-ngôn-ngữ-khác" class="anchor" aria-hidden="true" href="#các-ngôn-ngữ-khác"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Các ngôn ngữ khác</h2>
<ul>
<li><g-emoji class="g-emoji" alias="cn" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f1e8-1f1f3.png">🇨🇳</g-emoji> <strong>Trung Quốc:</strong>
<ul>
<li><a href="https://github.com/php-cpm/clean-code-php">php-cpm/clean-code-php</a></li>
</ul>
</li>
<li><g-emoji class="g-emoji" alias="ru" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f1f7-1f1fa.png">🇷🇺</g-emoji> <strong>Nga:</strong>
<ul>
<li><a href="https://github.com/peter-gribanov/clean-code-php">peter-gribanov/clean-code-php</a></li>
</ul>
</li>
<li><g-emoji class="g-emoji" alias="es" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f1ea-1f1f8.png">🇪🇸</g-emoji> <strong>Tây Ban Nha:</strong>
<ul>
<li><a href="https://github.com/fikoborquez/clean-code-php">fikoborquez/clean-code-php</a></li>
</ul>
</li>
<li><g-emoji class="g-emoji" alias="brazil" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f1e7-1f1f7.png">🇧🇷</g-emoji> <strong>Bồ Đào Nha:</strong>
<ul>
<li><a href="https://github.com/fabioars/clean-code-php">fabioars/clean-code-php</a></li>
<li><a href="https://github.com/jeanjar/clean-code-php/tree/pt-br">jeanjar/clean-code-php</a></li>
</ul>
</li>
<li><g-emoji class="g-emoji" alias="thailand" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f1f9-1f1ed.png">🇹🇭</g-emoji> <strong>Thái Lan:</strong>
<ul>
<li><a href="https://github.com/panuwizzle/clean-code-php">panuwizzle/clean-code-php</a></li>
</ul>
</li>
<li><g-emoji class="g-emoji" alias="fr" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f1eb-1f1f7.png">🇫🇷</g-emoji> <strong>Pháp:</strong>
<ul>
<li><a href="https://github.com/errorname/clean-code-php">errorname/clean-code-php</a></li>
</ul>
</li>
</ul>
<p><strong><a href="#m%E1%BB%A5c-l%E1%BB%A5c"><g-emoji class="g-emoji" alias="arrow_up" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2b06.png">⬆</g-emoji> Về mục lục</a></strong></p>
</article>
        </div>
