* PHP 專案裡面看不到 PHP Include Path、PHP Language Library、JavaScript Resources ?
  + 試試和正常的專案相比較 .project 檔案，取代    

        &lt; natures &gt;  
            
	         <nature> org.eclipse.wst.common.project.facet.core.nature </nature>
             <nature> org.eclipse.php.core.PHPNature </nature>
             <nature> org.eclipse.wst.jsdt.core.jsNature </nature>

        &lt; /natures &gt;
    
    區段

* 關於 Java 專案的 local debug，先搞清楚要執行的 class 和參考的 jar 在哪，另外讀取資源的部份，如果程式裡使用 "classpath" 就要在 Classpath 的頁籤中指定置放該資源的資料夾

* 如果 debug 時未顯示正確的 source，表示未指定正確 source Lookup path，以 Java 來說需指定到 package 的層級位置