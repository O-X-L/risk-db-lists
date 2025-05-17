# Open IP, Network & ASN Risk-Database - Simple Lists

This data will be and stay open-source!

In this repository we publish useful IP-/Network-/ASN-Lists that are generated from our [Risk Database](https://github.com/O-X-L/risk-db)!

If you find this project useful - leave a star and consider to also report abusers to the API!

Main repository: [O-X-L/risk-db](https://github.com/O-X-L/risk-db)

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

### ASN / Internet Providers

**Kinds**:
* `asn/hosting.txt`
* `asn/vpn.txt`
* `asn/isp.txt`
* `asn/crawler.txt`
* `asn/scanner.txt`

Note: You can also query those IP-Lists via the API: [Hosting](https://risk.oxl.app/api/list/asn/hosting), [VPN](https://risk.oxl.app/api/list/asn/vpn), [Crawler](https://risk.oxl.app/api/list/asn/crawler), [Scanner](https://risk.oxl.app/api/list/asn/scanner), [ISP](https://risk.oxl.app/api/list/asn/isp)

**Most reported**:
* `asn/top_100.txt`
* `asn/top_1000.txt`
* `asn/top_10000.txt`

----

### Networks

Networks are processed in blocks: `IP4 /24` (*256 IPs*) and `IP6 /56` (*256 /64 blocks*)

**Kinds**:
* `network/hosting.txt` (*from ASN*)
* `network/vpn.txt` (*from ASN*)
* `network/crawler.txt` (*from ASN*)
* `network/scanner.txt` (*from ASN*)
* `network/dynamic.txt` (*from IPs*)

**Most reported IPs**: (*network reputation*)
* `network/top_100_ips.txt`
* `network/top_1000_ips.txt`
* `network/top_10000_ips.txt`

**Most reported**:
* `network/top_100.txt`
* `network/top_1000.txt`
* `network/top_10000.txt`

----

### IPs

**Kinds**:
* `ip/hosting.txt` (*from ASN*)
* `ip/vpn.txt` (*from ASN*)
* `ip/crawler.txt` (*from ASN*)
* `ip/scanner.txt` (*from ASN*)
* `ip/dynamic.txt`
* `ip/proxy.txt`
* `ip/tor.txt`

**Most reported**:
* `ip/top_10000.txt`
* `ip/top_100000.txt`
* `ip/top_1000000.txt`

----

## License

**[BSD-3-Clause](https://opensource.org/license/bsd-3-clause)**

Free to use.

If you are nice, you can **optionally** mention that you use this IP data:

```html
<p>IP address data powered by <a href="https://risk.oxl.app">OXL</a></p>
```
