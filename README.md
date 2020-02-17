# leaflets_search
Search box on leaflets map
前提要引入leaflets.js
### 第一步： 引入
     <script src="./leaflet.customsearchbox.min.js"></script>
     <link href="./searchbox.min.css" rel="stylesheet" /> 
     
### 第二步： 
    //地图搜索框和实现的功能
    var searchboxControl=createSearchboxControl();
    var control = new searchboxControl({
        sidebarTitleText: 'Header',  
    });
    control._searchfunctionCallBack = function (searchkeywords)
    { //searchkeywords是用户输入的数据
        if (!searchkeywords) {searchkeywords = "The search call back is clicked !!"}
        //这里进行接口的连接，查询
        _this.axios.get(...)
      }
 ### 第三步：
       //根据经纬度定位到具体的某个设备
      map.setView([接口返回的lat, 接口返回的lng], 15);//这里是地图跳转
      L.marker([lat,lng],{icon: myIcon}).addTo(map)//这里是设置定位的图标
      })
      
 ### 第四步： 
    map.addControl(control);//把控件添加到地图中
