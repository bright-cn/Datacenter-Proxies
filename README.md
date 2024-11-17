# Bright Data 数据中心代理

[![Promo](https://github.com/bright-cn/Datacenter-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://bright.cn/proxy-types/datacenter-proxies?promo=github15)

## 概述
利用 Bright Data 广泛的[数据中心代理网络](https://bright.cn/proxy-types/datacenter-proxies)，以无与伦比的规模和速度进行可靠的数据收集和网页抓取。

- **770,000+ 数据中心 IP**
- 提供[共享](https://bright.cn/solutions/shared-proxies)和[独享](https://bright.cn/solutions/dedicated-proxies) IP 选项
- **~0.24 秒平均响应时间**
- 支持 **HTTP(S)** 和 [**SOCKS5**](https://bright.cn/solutions/socks5-proxies)
- **免费国家级定位**

## 关键功能
- **全球覆盖**：访问分布在[98 个国家](https://bright.cn/locations)的数据中心 IP。
- **高成功率**：在抓取任务中可达到 99.9% 的成功率。
- **快速可靠**：99.99% 的网络正常运行时间和快速连接速度。
- **自定义选项**：根据需求选择共享或独享 IP。
- **无限扩展**：支持无限并发会话。

## 价格计划
- **按量付费**：无需月度承诺，$0.6/GB。
- **月度订阅 - 共享**：
  - **10 个 IP**：$1.40/IP，$14/月 + VAT。
  - **100 个 IP**：$1.00/IP，$100/月 + VAT。
  - **500 个 IP**：$0.95/IP，$475/月 + VAT。
  - **1,000 个 IP**：$0.90/IP，$900/月 + VAT。
  - **企业计划**：为大规模数据收集提供定制解决方案。

- **月度订阅 - 独享**：
  - **10 个 IP**：$2.20/IP，$22/月 + VAT。
  - **100 个 IP**：$1.70/IP，$170/月 + VAT。
  - **500 个 IP**：$1.50/IP，$750/月 + VAT。
  - **1,000 个 IP**：$1.30/IP，$1300/月 + VAT。
  - **企业计划**：为大规模数据收集提供定制解决方案。

- **月度订阅 - 按流量计费**：
  - $0.51/GB，$499/月 + VAT。
  - $0.45/GB，$999/月 + VAT。
  - $0.42/GB，$1999/月 + VAT。
  - **企业计划**：为大规模数据收集提供定制解决方案。

注册即可享受首笔存款美元对美元奖励，最高可达 $500！

## 数据中心代理快速入门
1. **开始免费试用**：无需信用卡。
2. **集成**：通过 API 或 Bright Data 控制面板管理 IP 和配置。
3. **支持的语言**：提供 Python、Java、C#、Node.js 和 Shell 的快速入门指南。

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
我们的数据中心代理与以下流行的自动化工具兼容：

- [**Puppeteer**](https://bright.cn/integration/puppeteer)
- [**Selenium**](https://bright.cn/integration/selenium)
- [**Playwright**](https://bright.cn/integration/playwright)
- [**AdsPower**](https://bright.cn/integration/adspower)
- [**MultiLogin**](https://bright.cn/integration/multilogin)

## 使用案例
数据中心代理的常见应用：

- [**电子商务**](https://bright.cn/use-cases/ecommerce)：跟踪价格和产品库存。
- [**社交媒体**](https://bright.cn/use-cases/social-media-for-marketing)：监控趋势和用户互动。
- [**房地产**](https://bright.cn/use-cases/real-estate)：收集房产列表数据。
- [**旅游**](https://bright.cn/use-cases/travel)：比较各地的旅游优惠。

## 常见问题解答

### 什么是数据中心代理？
数据中心代理提供分配给服务器的 IP，允许您更改 IP 和位置，用于网页抓取和其他用途。

### 数据中心代理的优势是什么？
数据中心代理速度快且经济高效，非常适合简单的数据收集任务、账户管理以及绕过基本的地理限制。

### 企业如何使用数据中心代理？
从竞争分析到数字资产保护，数据中心代理支持各种行业的广泛任务。

### Bright Data 的数据中心代理分布在哪里？
我们的代理覆盖 98 个全球位置，IP 分布集中在 [美国](https://bright.cn/locations/united-states)、[加拿大](https://bright.cn/locations/ca)、[英国](https://bright.cn/locations/gb)、[德国](https://bright.cn/locations/de) 和 [法国](https://bright.cn/locations/fr)。

### 数据中心代理速度快吗？
是的，数据中心代理通过最少的路由提供快速连接，非常适合时间敏感的应用场景。

### 我应该选择共享还是独享的数据中心代理？
如果需要独占访问，请选择独享代理；如果需要成本效益高的解决方案来满足常见抓取和测试任务，请选择共享代理。
