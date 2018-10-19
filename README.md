# resource
http://www.cellocation.com/
基站/WIFI位置数据库2018年9月更新
基站数据库V1 26785494条
基站数据库V2 140991977条
WIFI数据库 724999277条
#2
离线数据库
基站、WIFI、POI、经纬度解析数据库、LBS开发等商务合作请联系：
QQ：3372218865
邮箱：service@cellocation.com
电话：13121184781
#3
https://www.ipip.net/support/api.html#wifi
0x01 访问方法
curl "http://ipapi.ipip.net/location/geo?ip=123.121.9.220" -H "Token: 1234567890"
0x02 响应
{
    code: 0,
    data: {
        ip:"123.121.9.220",
        longitude: 116.51124,    // IP定位经度WGS84
        latitude: 39.917572,     // IP定位纬度WGS84
        radius: 50,             // IP覆盖半径
        credibility: 100,      // 可信度 最大值为100（即为百分百可信任）
        gps_district: { // 高精度数据到区县等
            country_code: "CN",
            country: "中国",
            province: "北京",
            city: "北京",
            district: "朝阳区",
            china_code: "110105"
        },
        gps_aoi: [ // 高精度数据到商圈小区学校等
            {
                country_code: "CN",
                country: "中国",
                province: "北京",
                city: "北京",
                district: "朝阳区",
                china_code: "110105",
                aoi_type: "住宅小区",
                aoi_name: "朝阳园"
            },
            {
                country_code: "CN",
                country: "中国",
                province: "北京",
                city: "北京",
                district: "朝阳区",
                china_code: "110105",
                aoi_type: "商圈",
                aoi_name: "青年路商圈"
            }
        ]
        location:{ // 没有高精度数据时候的返回结果
            country: "中国",
            province: "北京",
            city: "北京"
        }
    }
}
