### umoney_api
 U-Money -ийн автобусны чиглэл харах API 

| API                                                          | Description                                  | Auth | Method | CORS      |
|--------------------------------------------------------------|----------------------------------------------|------|--------|-----------|
| https://api.u-money.mn/travel/bus_line_detail/11400020/start | Автобусны кодыг [эндээс](info.json) хараарай | No   | POST   | Unchecked |

### Жишээ код 
```python 
def bus_info(bus_code, point):
    """ point нь start эсвэл end гэсэн утга авна """

    import requests

    r = requests.post("https://api.u-money.mn/travel/bus_line_detail/" + bus_code +  "/" + point)
    info = r.json()

    if info['result_code'] == '001':
        return info
    elif info['result_code'] == '002':
        return "Арай аймар ачааллуулаад байна !"
    else:
        return "Нэг л *аахгүй байна."

if __name__ == "__main__":
    print (bus_info("11400020", "start"))
    
```
### Үр дүн

<details>
  <summary> Үр дүн харах </summary>
  
```json
{
   "end_time_at_start_point":"21:46",
   "station_list":[
      {
         "station_name":"ШАРГА МОРЬТЫН ЭЦЭС-зуслан",
         "station_id":"000000350",
         "longitude":106.93177,
         "station_seq":1,
         "exist_bus":"N",
         "latitude":48.06906
      },
      {
         "station_name":"Шарга морьтын 5-р буудал",
         "station_id":"000001605",
         "longitude":106.92595,
         "station_seq":2,
         "exist_bus":"N",
         "latitude":48.06796
      },
      {
         "station_name":"Шарга морьтын 4-р буудал",
         "station_id":"000001607",
         "longitude":106.92189,
         "station_seq":3,
         "exist_bus":"N",
         "latitude":48.06566
      },
      {
         "station_name":"Шарга морьт 3",
         "station_id":"000000352",
         "longitude":106.91612,
         "station_seq":4,
         "exist_bus":"N",
         "latitude":48.06214
      },
      {
         "station_name":"Шарга морьт 2",
         "station_id":"000000353",
         "longitude":106.90878,
         "station_seq":5,
         "exist_bus":"N",
         "latitude":48.05878
      },
      {
         "station_name":"Шарга морьт 1",
         "station_id":"000000349",
         "longitude":106.9053,
         "station_seq":6,
         "exist_bus":"N",
         "latitude":48.05266
      },
      {
         "station_name":"Жигжидийн уулзвар",
         "station_id":"000000345",
         "longitude":106.90065,
         "station_seq":7,
         "exist_bus":"Y",
         "latitude":48.04772
      },
      {
         "station_name":"Яргайтын богино",
         "station_id":"000000342",
         "longitude":106.90313,
         "station_seq":8,
         "exist_bus":"N",
         "latitude":48.04296
      },
      {
         "station_name":"Яргайтын богино 1",
         "station_id":"000001264",
         "longitude":106.90529,
         "station_seq":9,
         "exist_bus":"N",
         "latitude":48.03875
      },
      {
         "station_name":"Яргайт",
         "station_id":"000000340",
         "longitude":106.9074,
         "station_seq":10,
         "exist_bus":"N",
         "latitude":48.03486
      },
      {
         "station_name":"Яргайт 1",
         "station_id":"000001262",
         "longitude":106.91126,
         "station_seq":11,
         "exist_bus":"N",
         "latitude":48.02909
      },
      {
         "station_name":"100 мод",
         "station_id":"000000338",
         "longitude":106.91328,
         "station_seq":12,
         "exist_bus":"N",
         "latitude":48.02489
      },
      {
         "station_name":"Сэтгүүлчдийн төгөл",
         "station_id":"000001266",
         "longitude":106.91534,
         "station_seq":13,
         "exist_bus":"N",
         "latitude":48.01941
      },
      {
         "station_name":"Шадивлан",
         "station_id":"000000335",
         "longitude":106.9177,
         "station_seq":14,
         "exist_bus":"N",
         "latitude":48.01522
      },
      {
         "station_name":"Шадивлан-1",
         "station_id":"000001296",
         "longitude":106.92089,
         "station_seq":15,
         "exist_bus":"N",
         "latitude":48.01132
      },
      {
         "station_name":"Ар согоот",
         "station_id":"000000333",
         "longitude":106.92437,
         "station_seq":16,
         "exist_bus":"N",
         "latitude":47.99991
      },
      {
         "station_name":"Салхит",
         "station_id":"000000331",
         "longitude":106.92567,
         "station_seq":17,
         "exist_bus":"N",
         "latitude":47.99331
      },
      {
         "station_name":"Салхит завсар-3",
         "station_id":"000001258",
         "longitude":106.92511,
         "station_seq":18,
         "exist_bus":"N",
         "latitude":47.98865
      },
      {
         "station_name":"Салхит завсар-2",
         "station_id":"000001256",
         "longitude":106.92361,
         "station_seq":19,
         "exist_bus":"N",
         "latitude":47.98344
      },
      {
         "station_name":"Салхит завсар-1",
         "station_id":"000001254",
         "longitude":106.92049,
         "station_seq":20,
         "exist_bus":"N",
         "latitude":47.98006
      },
      {
         "station_name":"Замын цагдаагийн пост",
         "station_id":"000000314",
         "longitude":106.91797,
         "station_seq":21,
         "exist_bus":"N",
         "latitude":47.97417
      },
      {
         "station_name":"7 БУУДАЛ",
         "station_id":"000000241",
         "longitude":106.91723,
         "station_seq":22,
         "exist_bus":"Y",
         "latitude":47.96827
      },
      {
         "station_name":"6 буудал",
         "station_id":"000000243",
         "longitude":106.91725,
         "station_seq":23,
         "exist_bus":"N",
         "latitude":47.96502
      },
      {
         "station_name":"Нэгдсэн үйлчилгээний төв",
         "station_id":"000001444",
         "longitude":106.91672,
         "station_seq":24,
         "exist_bus":"N",
         "latitude":47.96128
      },
      {
         "station_name":"7 Завсар",
         "station_id":"000000245",
         "longitude":106.91593,
         "station_seq":25,
         "exist_bus":"N",
         "latitude":47.95819
      },
      {
         "station_name":"5 буудал",
         "station_id":"000000247",
         "longitude":106.915,
         "station_seq":26,
         "exist_bus":"Y",
         "latitude":47.95455
      },
      {
         "station_name":"17-р сургууль",
         "station_id":"000000269",
         "longitude":106.91389,
         "station_seq":27,
         "exist_bus":"N",
         "latitude":47.94768
      },
      {
         "station_name":"32-ын тойрог",
         "station_id":"000000267",
         "longitude":106.91448,
         "station_seq":28,
         "exist_bus":"N",
         "latitude":47.94317
      },
      {
         "station_name":"Ногоон нуур буудал",
         "station_id":"000000300",
         "longitude":106.91599,
         "station_seq":29,
         "exist_bus":"Y",
         "latitude":47.93502
      },
      {
         "station_name":"4-р дэлгүүр",
         "station_id":"000000294",
         "longitude":106.91744,
         "station_seq":30,
         "exist_bus":"Y",
         "latitude":47.92716
      },
      {
         "station_name":"Монгол Улсын Их Сургууль",
         "station_id":"000000307",
         "longitude":106.92211,
         "station_seq":31,
         "exist_bus":"N",
         "latitude":47.92247
      },
      {
         "station_name":"МУБИС",
         "station_id":"000000287",
         "longitude":106.9233,
         "station_seq":32,
         "exist_bus":"N",
         "latitude":47.91972
      },
      {
         "station_name":"Өргөө амаржих газар",
         "station_id":"000000281",
         "longitude":106.92632,
         "station_seq":33,
         "exist_bus":"N",
         "latitude":47.918
      },
      {
         "station_name":"Бөхийн өргөө",
         "station_id":"000000369",
         "longitude":106.93362,
         "station_seq":34,
         "exist_bus":"N",
         "latitude":47.91839
      },
      {
         "station_name":"Зүүн 4 зам",
         "station_id":"000000371",
         "longitude":106.94104,
         "station_seq":35,
         "exist_bus":"N",
         "latitude":47.91885
      },
      {
         "station_name":"Хавдар судлалын эмнэлэг",
         "station_id":"000000401",
         "longitude":106.94377,
         "station_seq":36,
         "exist_bus":"N",
         "latitude":47.91484
      },
      {
         "station_name":"Улаанбаатар их сургууль",
         "station_id":"000000406",
         "longitude":106.94343,
         "station_seq":37,
         "exist_bus":"Y",
         "latitude":47.91104
      },
      {
         "station_name":"Их монгол хороолол",
         "station_id":"000001445",
         "longitude":106.94323,
         "station_seq":38,
         "exist_bus":"N",
         "latitude":47.90647
      },
      {
         "station_name":"Дүнжингарав Худалдааны төв",
         "station_id":"000000621",
         "longitude":106.94901,
         "station_seq":39,
         "exist_bus":"N",
         "latitude":47.90496
      }
   ],
   "result_code":"001",
   "line_name":"ХО:2 (ШАРГА МОРЬТЫН ЭЦЭС-зуслан-Дүнжингарав Худалдааны төв)",
   "line_id":"11400020",
   "weekday_interval":5,
   "start_time_at_end_point":"06:51",
   "holiday_interval":5,
   "start_time_at_start_point":"06:40",
   "line_type":"",
   "end_time_at_end_point":"23:01"
}
```
</details>


### To do
- [x] Автобус хайх

- [] Буудал хайх

- [] Хот хооронд чиглэл хайх

- [] Нислэг хайх 
