# Bright Data 数据中心代理

[![促销](https://github.com/bright-cn/Awesome-Web-Scraping/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/proxy-types/datacenter-proxies?promo=github15)

## 概览
利用 Bright Data 庞大的[数据中心代理网络](https://www.bright.cn/proxy-types/datacenter-proxies)，以无与伦比的规模和速度实现可靠的数据采集和网页爬虫。

- **超过 770,000 个数据中心 IP**
- **[共享](https://www.bright.cn/solutions/shared-proxies)和[专用](https://www.bright.cn/solutions/dedicated-proxies) IP 选项**
- **平均响应时间约 0.24 秒**
- **支持 HTTP(S) 和 [SOCKS5](https://www.bright.cn/solutions/socks5-proxies)**
- **免费国家/地区级定位**

## 主要功能
- **全球覆盖**：访问遍布 [98 个国家/地区](https://www.bright.cn/locations)的数据中心 IP。
- **高成功率**：抓取任务成功率最高可达 99.9%。
- **快速可靠**：网络正常运行时间达 99.99%，连接速度快。
- **灵活定制**：根据你的需求选择共享或专用 IP。
- **无限扩展**：支持并发会话，无任何限制。

## 定价方案
- **按量付费**：$0.6/GB，无需月度承诺。
- **月度订阅 - 共享**：
  - **10 个 IP**：$1.40/IP，$14/月 + 增值税。
  - **100 个 IP**：$1.00/IP，$100/月 + 增值税。
  - **500 个 IP**：$0.95/IP，$475/月 + 增值税。
  - **1,000 个 IP**：$0.90/IP，$900/月 + 增值税。
  - **企业方案**：为大规模数据采集量身定制解决方案。

- **月度订阅 - 专用**：
  - **10 个 IP**：$2.20/IP，$22/月 + 增值税。
  - **100 个 IP**：$1.70/IP，$170/月 + 增值税。
  - **500 个 IP**：$1.50/IP，$750/月 + 增值税。
  - **1,000 个 IP**：$1.30/IP，$1300/月 + 增值税。
  - **企业方案**：为大规模数据采集量身定制解决方案。


- **月度订阅 - 按 GB 付费**：
  - $0.51/GB，$499/月 + 增值税。
  - $0.45/GB，$999/月 + 增值税。
  - $0.42/GB，$1999/月 + 增值税。
  - **企业方案**：为大规模数据采集量身定制解决方案。

注册即可获得与首次充值金额等额的赠金，最高 $500！

## 数据中心代理入门
1. **开始免费试用**：无需信用卡。
2. **集成**：通过 API 或 Bright Data 控制面板管理 IP 和配置。
3. **支持的语言**：提供 Python、Java、C#、Node.js 和 Shell 快速入门指南。

## 代码示例

### Python

```python
import sys

# Replace '[your customerID]', 'datacenter', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-datacenter", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-datacenter", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
    })
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-residential:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## 集成
我们的数据中心代理兼容热门自动化工具，包括：

- [**Puppeteer**](https://www.bright.cn/integration/puppeteer)
- [**Selenium**](https://www.bright.cn/integration/selenium)
- [**Playwright**](https://www.bright.cn/integration/playwright)
- [**AdsPower**](https://www.bright.cn/integration/adspower)
- [**MultiLogin**](https://www.bright.cn/integration/multilogin)

## 使用场景
数据中心代理的常见应用：

- [**电子商务**](https://www.bright.cn/use-cases/ecommerce)：跟踪定价和商品库存情况。
- [**社交媒体**](https://www.bright.cn/use-cases/social-media-for-marketing)：监测趋势和互动情况。
- [**房地产**](https://www.bright.cn/use-cases/real-estate)：采集房源数据。
- [**旅游**](https://www.bright.cn/use-cases/travel)：比较不同地点的旅游优惠。

## 常见问题

### 什么是数据中心代理？
数据中心代理提供分配给服务器的 IP，让你能够更改自己的 IP 和位置，以用于网页爬虫和其他场景。

### 数据中心代理有哪些优势？
数据中心代理速度快且经济实惠，非常适合简单的数据采集任务、账号管理以及绕过基本的地理限制。

### 企业如何使用数据中心代理？
从竞品分析到数字资产保护，数据中心代理可支持各行各业的广泛任务。

### Bright Data 的数据中心代理位于哪些地方？
我们的代理覆盖全球 98 个地点，并在[美国](https://www.bright.cn/locations/united-states)、[加拿大](https://www.bright.cn/locations/ca)、[英国](https://www.bright.cn/locations/gb)、[德国](https://www.bright.cn/locations/de)和[法国](https://www.bright.cn/locations/fr)拥有大量 IP。

### 数据中心代理速度快吗？
是的，数据中心代理的路由路径短，可提供快速连接，非常适合对时效性要求高的应用。

### 我应该使用共享数据中心代理还是专用数据中心代理？
如果需要独享访问，请使用专用代理；对于常规抓取和测试任务，如果需要经济实惠的解决方案，请使用共享代理。
