# IrisEmby
mihomo rules for Iris Emby

主线路（可尝试直连）
https://iris.niceduck.lol:443

海外备用（国际优化 CDN）
https://cdn.irisnb.com:443

4837 优化线路
https://iris4837.iris520.us:443

美国 4837
https://ak4837.iris520.us:443

美西反代
https://byteiris.iris520.us:443

CF 优选 IP（直连效果受地区和运营商影响）
http://cf.iris520.us:80

# Rules
```yaml
rule-providers:
  cn_domain: {type: http, behavior: domain, format: yaml, url: "https://fastly.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/cn.yaml", path: ./cn_domain.yaml, interval: 86400}
  cn_ip: {type: http, behavior: ipcidr, format: yaml, url: "https://fastly.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geoip/cn.yaml", path: ./cn_ip.yaml, interval: 86400}
  gfw: {type: http, behavior: domain, format: yaml, url: "https://fastly.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/gfw.yaml", path: ./gfw.yaml, interval: 86400}

rules:
  - RULE-SET,cn_domain,DIRECT
  - RULE-SET,cn_ip,DIRECT
  - RULE-SET,gfw,🚀 节点选择
  - MATCH,🚀 节点选择
```

# Acknowledgement
- [https://t.me/IrisEmby_Bot](https://t.me/IrisEmby_Bot)
- [https://t.me/Iris_notice](https://t.me/IrisEmby_Bot)
- [https://t.me/IrisEmby_Group](https://t.me/IrisEmby_Bot)
