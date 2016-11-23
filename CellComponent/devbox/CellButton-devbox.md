#### 버튼 항상 표시

버튼은 컬럼의 `alwaysShowButton`을 true로 설정해 항상 보이게 할 수 있습니다. 

<a class="btn primary small round lowercase" id="btnButtonAlwaysShowButton">버튼 항상 표시</a>

```js
gridView.setColumnProperty("EmployeeID", "alwaysShowButton", "true");
gridView.setColumnProperty("OrderID", "alwaysShowButton", "true");
gridView.setColumnProperty("CustomerID", "alwaysShowButton", "true");
```
<p></p>

#### 데이터 셀에 버튼을 표시하는 방법

- `always`: 항상 표시 
- `default`: hovering, focused상태에서 표시 
- `visible`: focused상태만 표시
- `hidden`: 표시하지 않음

<a class="btn primary small round lowercase" id="btnButtonAlways">항상 표시</a>

```js
gridView.setColumnProperty("EmployeeID", "buttonVisibility", "always");
gridView.setColumnProperty("OrderID", "buttonVisibility", "always");
gridView.setColumnProperty("CustomerID", "buttonVisibility", "always");
```

<a class="btn primary small round lowercase" id="btnButtonDefault">hovering, 포커스 상태만 표시</a>

```js
gridView.setColumnProperty("EmployeeID", "buttonVisibility", "default");
gridView.setColumnProperty("OrderID", "buttonVisibility", "default");
gridView.setColumnProperty("CustomerID", "buttonVisibility", "default");
```

<a class="btn primary small round lowercase" id="btnButtonVisible">포커스 상태만 표시</a>

```js
gridView.setColumnProperty("EmployeeID", "buttonVisibility", "visible");
gridView.setColumnProperty("OrderID", "buttonVisibility", "visible");
gridView.setColumnProperty("CustomerID", "buttonVisibility", "visible");
```

<a class="btn primary small round lowercase" id="btnButtonHidden">표시 안함</a>

```js
gridView.setColumnProperty("EmployeeID", "buttonVisibility", "hidden");
gridView.setColumnProperty("OrderID", "buttonVisibility", "hidden");
gridView.setColumnProperty("CustomerID", "buttonVisibility", "hidden");
```

#### 버튼 클릭 이벤트

팝업 메뉴 버튼 클릭 이벤트

- [onMenuItemClicked](http://help.realgrid.com/api/GridBase/onMenuItemClicked/)

```js
gridView.onMenuItemClicked = function (grid, data) {
    alert(data.label);
};
```
셀버튼 클릭 이벤트

- [onCellButtonClicked](http://help.realgrid.com/api/GridBase/onCellButtonClicked/)

```js
gridView.onCellButtonClicked = function (grid, itemIndex, column) {
    alert("CellButton Clicked: itemIndex=" + itemIndex + ", fieldName=" + column.fieldName);
};
```

이미지 버튼 클릭 이벤트

- [onImageButtonClicked](http://help.realgrid.com/api/GridBase/onImageButtonClicked/)

```js
gridView.onImageButtonClicked = function (grid, itemIndex, column, buttonIndex, name) {
    alert("onImageButtonClicked: " + itemIndex + ", " + column.name+", " + buttonIndex + ", " + name);
};
```

<script>
  $('#btnButtonAlwaysShowButton').click(function() {
    gridView.setColumnProperty("EmployeeID", "alwaysShowButton", "true");
    gridView.setColumnProperty("OrderID", "alwaysShowButton", "true");
    gridView.setColumnProperty("CustomerID", "alwaysShowButton", "true");
  });

  $('#btnButtonAlways').click(function() {
    gridView.setColumnProperty("EmployeeID", "buttonVisibility", "always");
    gridView.setColumnProperty("OrderID", "buttonVisibility", "always");
    gridView.setColumnProperty("CustomerID", "buttonVisibility", "always");
  });

  $('#btnButtonDefault').click(function() {
    gridView.setColumnProperty("EmployeeID", "buttonVisibility", "default");
    gridView.setColumnProperty("OrderID", "buttonVisibility", "default");
    gridView.setColumnProperty("CustomerID", "buttonVisibility", "default");
  });

  $('#btnButtonVisible').click(function() {
    gridView.setColumnProperty("EmployeeID", "buttonVisibility", "visible");
    gridView.setColumnProperty("OrderID", "buttonVisibility", "visible");
    gridView.setColumnProperty("CustomerID", "buttonVisibility", "visible");
  });

  $('#btnButtonHidden').click(function() {
    gridView.setColumnProperty("EmployeeID", "buttonVisibility", "hidden");
    gridView.setColumnProperty("OrderID", "buttonVisibility", "hidden");
    gridView.setColumnProperty("CustomerID", "buttonVisibility", "hidden");
  });

</script>