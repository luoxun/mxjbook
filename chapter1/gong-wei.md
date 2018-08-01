# 工位

---

### 根据工位ID返回工位详细信息

* **Uri:**  
  `/station/warehouse/{warehouseid}/stationid/{stationid}`

* **Methon:**  
  ** **`GET`

* **Response**

```js
{
    "code": 200,
    "message": "",
    "data":
    {
        "station_id":"xxx",  //工位ID
        "station_type":"xx", //流动工位 固定工位
        "station_id":"xxxx", //工位编号
        'station_number':"xxxx", //工位号
        'station_group':"xxxxx", //工位组
        "device_id":"xxxx" //工位设备id
        "device_number":"xxxx" //工位设备id

    }
}
```

### 新增工位

* **Uri:**  
  `/station/warehouse/{warehouseid}/fixation/`

* **Methon:**  
  ** **`POST`

* **Request**

  ```js
  {"
  "station_id":"xxxx", //工位编号
  "station_number":"xxxx", //工位号
  "station_group":"xxxxx", //工位组
  "binddevice":"xxxx", // 绑定设置
  "isbindlayer":'xxx" //绑定后工位地图
  "maplongitude":"34" //工位经度
  "maplatitude":"193.3" //工位 纬度
  "stion_type":"1"  //工位类型 1.固定工位,2流动工位
  }
  ```

* **Response**
  ```js
  {
  "code": 200,
  "message": "",
  "details": null,
  "data":
  {
    "station_id":"xxxxxxx" //流动工位ID
    "station_type":"1"
  }
  ```

\`\`\`

