* prev

```
var currentTab = gBrowser.mTabContainer.selectedIndex;
gBrowser.mTabContainer.advanceSelectedTab(-1);
var newTab = gBrowser.mTabContainer.selectedIndex;
if(currentTab == newTab) {
   var count = gBrowser.mTabContainer.childNodes.length;
   gBrowser.mTabContainer.selectedIndex = count - 1;
}
```

* next

```
var tab = gBrowser.mCurrentTab;
if(tab.nextSibling) {
   gBrowser.mTabContainer.advanceSelectedTab(1);
} else {
  gBrowser.mTabContainer.selectedIndex = 0;
}
```

