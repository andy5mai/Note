### p.2-21
  若執行 /test/index.html 卻未在根目錄看到 index.html    
  則會在 /META-INF/resources 底下找尋 index.html    
  
### p.2-22
  取得 /WEB-INF 的資源    
  ServletContext 的 getResource() 或 getResourceAsStream() 或透過 RequestDispatcher 請求調派    
  
  若 URL 以 / 結尾，確實存在該目錄，則須傳回該目錄下的歡迎頁面    
  web.xml 可定義該歡迎頁面
```
  <welcome-file-list>
    <welcome-file>index.html</welcome-file>
    <welcome-file>default.jsp</welcome-file>
  </welcome-file-list>
```
    
  找不到會到 META-INF/resources 找，若不存在該目錄，則會使用 servlet (如果存在的話)
  
### p.2-23
  web-fragment.xml    
  額外 JAR file 部署    
  
### p.3-12
  post 時可執行 HttpServletRequest.setCharacterEncoding() 在 getParameter() 前設定編碼方式，以得到正確的參數數值    
  但 get 時執行 HttpServletRequest.setCharacterEncoding() 就無效了，因為 get 是 http 伺服器在處理 url，而不是 web 容器    
  可透過 new String(HttpServletRequest.getParameter("paramName").getBytes("ISO-8859-1"), "UTF-8") 來取得正確的值    
  
### p.3-15
  可使用 HttpServletRequest.getReader() 或 getInputStream() 來讀取本體    
  同一時間只能呼叫其中一個，否則會拋出 IllegalStateException    
  ```    
  BufferedReader reader = request.getReader();
  String input = null;
  String requestBody = "";
  while((input = reader.readLine()) != null) {
    requestBody = requestBody + input + "<br>";
  }
  ```

      
  在 Servlet 3.0 中，可以使用 getPart() 或 getParts() 來處理檔案上傳事宜
  
### p.3-22
  @MultipartConfig 標籤可用來設定 Servlet 處理上傳檔案的相關資訊，如：    
#### fileSizeThreshold :     
整數值設定，上傳檔案大小超過設定會先寫入暫存檔，預設為 0    
#### location :     
字串設定，設定寫入檔案時的目錄，如果有設定這個屬性，則暫存檔就是寫到指定的目錄，也可搭配 Part 的 write() 方法使用，預設為空字串    
#### maxFile :     
限制上傳檔案大小，預設為 -1L，表示不限制大小    
#### maxRequestSize :     
限制 multipart/form-data 請求個數，預設為 -1L，表示不限個數    

### p.3-23
  multipart/form-data 發送的每個內容區段，都會有以下的標頭資訊：    
```
  Content-Disposition: form-data; name="filename"; filename="caterpillar.jpg"
  Content-Type: image/jpeg
```    
Part 有個方便的 write() 方法，可將上傳檔案指定檔名寫入磁碟中，write() 可指定檔名，寫入路徑是相對於 @MultipartConfig 的 location 設定的路徑    

如果是多個檔案上傳，則是 getParts() 方法，由於上傳按鈕也是其中一個 part 物件，所以用 Part.getName() 來取得名稱加以判斷