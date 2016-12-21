```
    //原因：未使用 next() 前，iterator 指標並未指到東西，所以無法刪除

    ArrayList<String> listStrs = new ArrayList<String>();
    listStrs.add("123");
    listStrs.add("456");
    listStrs.add("789");
	
    Collection<String> colStrs = listStrs;
    Iterator<String> itStrs = colStrs.iterator();
	
    if (itStrs.hasNext()) itStrs.next(); itStrs.remove();
```