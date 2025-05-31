# Open IP, Network & ASN Risk-Database - Simple Lists

This data will be and stay open-source!

In this repository we publish useful IP-/Network-/ASN-Lists that are generated from our [Risk Database](https://github.com/O-X-L/risk-db)!

If you find this project useful - leave a star and consider to also report abusers to the API!

Main repository: [O-X-L/risk-db](https://github.com/O-X-L/risk-db)

----

## Contribute

If you have ideas for additional useful lists we could build:

* Start [a discussion](https://github.com/O-X-L/risk-db-lists/discussions)
* Or E-Mail us: [risk-db@oxl.at](mailto:risk-db@oxl.at)

----

## Reporting, Processing & Processed Data

You can find the processed data and source-code for the reporting/processing of data here: [O-X-L/risk-db](https://github.com/O-X-L/risk-db)

You can find the raw report-data here: [O-X-L/risk-db-archive](https://github.com/O-X-L/risk-db-archive)

----

## Usage

You **SHOULD NOT** just drop any requests from these sources.

There might be legit users using a VPN that would match as false-positive.

You might want to **flag** traffic from those sources and restrict their access like:

* Lower the rate-limits
* Show (more) captcha's on forms
* Lower lifetime of session cookies
* Add that flag to your logs so you can use it to analyze the traffic
* Deny access to administrative locations

Be aware that we cannot verify if reports are false-positives. We currently only keep track of simple reporter-reputation metrics.

----

## Lists

The `top_*.csv` files are in format: `<reported>,<report-count>`

Download URLs: `https://raw.githubusercontent.com/O-X-L/risk-db-lists/refs/heads/main/<asn|net|ip|other>/<file>` or `https://risk.oxl.app/file/list/<asn|net|ip|other>/<file>`

### ASN / Internet Providers

**Kinds**:
* `asn/kind_hosting.txt`
* `asn/kind_vpn.txt`
* `asn/kind_isp.txt`
* `asn/kind_crawler.txt`
* `asn/kind_scanner.txt`
* `asn/kind_education.txt`

Note: You can also query those IP-Lists via the API: [Hosting](https://risk.oxl.app/api/list/asn/hosting), [VPN](https://risk.oxl.app/api/list/asn/vpn), [Crawler](https://risk.oxl.app/api/list/asn/crawler), [Scanner](https://risk.oxl.app/api/list/asn/scanner), [ISP](https://risk.oxl.app/api/list/asn/isp)

**Most reported**:
* `asn/top_100.txt` & `.csv`
* `asn/top_1000.txt` & `.csv`
* `asn/top_10000.txt` & `.csv`

----

### Networks

Networks are processed in blocks: `IP4 /24` (*256 IPs*) and `IP6 /56` (*256 /64 blocks*)

**Kinds**:
* `net/kind_hosting.txt` (*from ASN*)
* `net/kind_vpn.txt` (*from ASN*)
* `net/kind_crawler.txt` (*from ASN*)
* `net/kind_scanner.txt` (*from ASN*)
* `net/kind_isp.txt` (*from ASN*)
* `net/kind_education.txt` (*from ASN*)
* `net/kind_dynamic.txt` (*from IPs*)

**Most reported IPs**: (*network reputation*)
* `net/top_100_ips_4.txt` & `top_100_ips_6.txt` & `.csv`
* `net/top_1000_ips_4.txt` & `top_1000_ips_6.txt` & `.csv`
* `net/top_10000_ips_4.txt` & `top_10000_ips_6.txt` & `.csv`

**Most reported**:
* `net/top_100.txt` & `.csv`
* `net/top_1000.txt` & `.csv`
* `net/top_10000.txt` & `.csv`

----

### IPs

**Kinds**:
* `ip/kind_hosting.txt` (*from ASN*)
* `ip/kind_vpn.txt` (*from ASN*)
* `ip/kind_crawler.txt` (*from ASN*)
* `ip/kind_scanner.txt` (*from ASN*)
* `ip/kind_isp.txt` (*from ASN*)
* `ip/kind_education.txt` (*from ASN*)
* `ip/kind_dynamic.txt`
* `ip/kind_proxy.txt`
* `ip/kind_tor.txt` (*Note: you can find the full list of tor-exit-nodes here:* [check.torproject.org](https://check.torproject.org/torbulkexitlist))

**Most reported**:
* `ip/top_1000.txt` & `.csv`
* `ip/top_10000.txt` & `.csv`
* `ip/top_100000.txt` & `.csv`

----

### Other Info

**HTTP User-Agents**
* `other/user_agents.txt`

**JA4-Fingerprints with User-Agent**
* `other/ja4_user_agents.csv`  (format: `JA4,user-agent-1|user-agent-2`)

**PTRs**
* `other/ptrs.csv`


----

## License

**[BSD-3-Clause](https://opensource.org/license/bsd-3-clause)**

Free to use.

If you are nice, you can **optionally** mention that you use this IP data:

```html
<p>IP address data powered by <a href="https://risk.oxl.app">OXL</a></p>
```
