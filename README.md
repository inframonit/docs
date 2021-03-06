
![logo.inframonit.com](https://logo.inframonit.com/1/cover.png)

# [docs.inframonit.com](https://docs.inframonit.com/) [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/main/ABOUT/MENU.md) 

+ [Blog - www.inframonit.com](https://www.inframonit.com/)
+ [Code - bash.inframonit.com](https://bash.inframonit.com/)
+ [Example use cases - examples.inframonit.com](http://examples.inframonit.com)
+ [Logotyp: logo.inframonit.com](https://logo.inframonit.com/)

+ [LICENSE](LICENSE)

## About inframonit [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/main/ABOUT/ABOUT.md)

this is part of apidsl for inframonit ecosystem to help You manage the applications

Monitoring includes:
1. Internet domains and subdomains,
2. Servers of the client and partners, e.g. dns (nazwa.pl, OVH, Cloudflare)
3. SaaS services of the client and its partners

Examples of faults detected by InfraMonit:
1. Lack of availability of websites and subpages
2. Unable to log in
3. It is not possible to send a contact message from the form
4. No purchase in the store
5. Extended shipment of goods,
6. Unavailability of goods
7. Failure of payment systems



# Monitor your positions in SERP
Track your positions in Search Engine Result Pages for chosen keywords every day. How is your situation in Google compared to yesterday or two days ago? Keep an eye on ranking fluctuations and, if necessary, be ready to take action!

# Keep track of your competitors in Google
After you run the analysis of your own domain, take a better look at the competitive websites. The more you know about their actions, the better conclusions you can draw for yourself!


+ hourly checking of any infrastructure with:
    + apisch + multisitemap
    + apipong
    + webpageshot

+ current information about infrastructure
    + registrar
    + dns records
    + ns, cloudflare,digitalocean
    + servers
    + parkings


With multisitemap it's possible to check the infrastructure nad compare every hour what kind of differents are comming and doing some event
what can help fix bugs or create ticket and send information to support team



OFFER.
monitorowanie infrastruktury firm, tych lokalnych r??wnie?? ze skanowaniem mapy sieci i jej replikowaniem

MORE:
[Wielka rezygnacja specjalist??w ds. cyberbezpiecze??stwa - CRN](https://crn.pl/aktualnosci/wielka-rezygnacja-specjalistow-ds-cyberbezpieczenstwa/)



# Warstwa ochronna infrastruktury


ApiDSL mo??e by?? jednym z kierunk??w u??ycia mo??e by?? warstwa ochronna, cyberbezpiecze??stwa system??w informatycznych.

Bezpiecze??stwa dla system??w istniej??cych, gdy?? tak jak w samochodach opr??cz operacyjnych zada?? s?? te diagnostyczne

W sieciach z regu??y to zewn??trzne systemy diagnostyczne, w modelu SaaS

Druga warstwa, zaraz po warstwie logiki biznesowej aplikacji, 
niezale??na od wewn??trznych i zewn??trznych, co?? pomi??dzy, na niezale??nej inrastrukturze , jak firewall pomi??dzy intranetem i internetem

R??wnie?? podczas developmentu, jako warstwa s??u????ca do fizycznej diagnostyki ca??ej infrastruktury.




## Install inframonit [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/main/DOCS/INSTALL.md)


install dependencies from file: [apifork.txt](apifork.txt)

```bash
./apifork
```

install packages for apidsl from file: [apidsl.txt](apidsl.txt)

```bash
./apidsl.sh install
```

OR
install packages inside apidsl

```bash
cd apifork
./add https://github.com/letwhois/bash bash letwhois
./add https://github.com/reactphp/dns php reactphp
```



## Start inframonit [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/main/DOCS/START.md)


get whois data

```bash
./apidsl.sh 'letwhois.ns("softreck.com")'
```

get title
```bash
./apidsl.sh 'http("https://softreck.com").letpath.tag("title")'
```

```bash
cat domain.txt | ./letWhois.sh softreck.com
```

file domain.txt
```bash
softreck.com
```

OUTPUT:

    Softreck &#124; Leadership Through Software Development



## EXAMPLES [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/main/START/EXAMPLES.md)

Rozwi??zanie #apidsl s??u??y pisaniu komend do wcze??niej napisanych skrypt??w, bibliotek, aplikacji. Zamiast ??cie??ek do plik??w u??ywamy nazw jako funkcji z parametrem. Korzy????? re-u??ycie kodu, zamiast refaktoryzacji! APIDSL to jedno z rozwi??za?? w (pisanej jeszcze) ksi????ce #hipermodularyzacja

API + DSL = Application Programming Interface controlled over Domain Specific Language
#apidsl is available for testing
#hypermodularity #hyperprogramming #mvp #prototyping #programming #testing

### install

[minsungson/GitHub-cURL: A guide to installing files from GitHub repos in terminal using cURL](https://github.com/minsungson/GitHub-cURL)

help
```bash
./apidsl -h
```

init files and folders to start writing scripts
```bash
./apidsl init
```

```bash
./apifork install
```


```bash
./apifork update
```

## START

```js
load("domains.txt")
.split("/n")
.http()
.xpath("title")
.appendToFile("titles.txt")
```


### xpath from functions

```bash
./apidsl 'f.http("https://softreck.com").f.xpath("title")'
```


### tag from letpath

```bash
./apidsl 'f.http("https://softreck.com").letpath.tag("title")'
```


### nameservers

```apifork
https://github.com/letwhois/bash whois
```

```bash
./apidsl 'whois.ns("softreck.com")'
```



start using

```bash
./apidsl 'puppeteer.csv("premium.pl/login_user_screenshot.csv")'
```


```bash
./apidsl 'path.file("botreck.txt").split().puppeteer.csv()'
```

```bash
./apidsl 'puppeteer.csv("premium.pl/login_user_screenshot.csv").split().botreck.puppeter()'
```

### loop

```bash
./apidsl 'f.load("domains.txt").split("/n").f.http().f.xpath("title").f.appendToFile("titles.txt")'
```


## TODO [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/CONTRIBUTION/TODO.md)


## TODO

przygotowa?? scenariusze
UI
backend
remote deployment
uruchomi?? na RPI zero




## Contribution [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/flatedit/examples/edit/main/CONTRIBUTION/CONTRIBUTION.md)


### Update

apifork
```bash
curl https://raw.githubusercontent.com/apifork/bash/main/apifork.sh -o apifork
./apifork update
```

apipackage
```bash
curl https://raw.githubusercontent.com/apipackage/bash/main/apipackage.sh -o apipackage
./apipackage update
```

### Remove


apifork
```bash
./apifork remove
```

### Install

Install dependencies after created project
```bash
curl https://raw.githubusercontent.com/apifork/bash/main/apifork.sh -o apifork
echo "https://github.com/flatedit/bash.git flatedit" > "apifork.dev.txt"
./apifork install apifork.dev.txt
```


Install package list after created project
```bash
curl https://raw.githubusercontent.com/apipackage/bash/main/apipackage.sh -o apipackage
echo "https://github.com/letwhois/bash apidsl/apidsl/bash letwhois" >> "apipackage.txt"
./apipackage install
```

Edit documentation with flatedit
```bash
echo "./DOCS/MENU.md" >> "flatedit.txt"
echo "./DOCS/ABOUT.md" >> "flatedit.txt"
echo "./DOCS/FOOT.md" >> "flatedit.txt"
```

### Update documentation

```bash
 ./flatedit
```

### Config project file

The config file: **.apifork** can be another, e.g. **apifork.txt**

Just change the first line in  **.apifork** on **apifork.txt**
```bash
apifork.txt
```

### install

[minsungson/GitHub-cURL: A guide to installing files from GitHub repos in terminal using cURL](https://github.com/minsungson/GitHub-cURL)

```bash
./apifork install
```
OR

```bash
./apifork
```

### update

```bash
./apifork update
```


### remove

```bash
./apifork remove
```


## 5G Deployment [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/inframonit/docs/edit/main/CONTRIBUTION/DEPLOYMENT.md)

10 steps you must take in order to help ensure #5G deployment success for your organization.

## Ensure that devices meet 3GPP standards, industry regulations & your network requirements. 
Each release of the 5G standard introduces new capabilities that require new technologies. 
Ensure that your devices meet 3GPP standards, as well as any relevant industry regulations & your unique network requirements.

## Assess the cybersecurity hygiene of 5G devices.
The attack surface grows exponentially with billions of connected mobile devices, Internet of Things (IoT) devices & Wi-Fi networks & endpoints. 
Assess the cybersecurity posture of your 5G devices thoroughly & frequently.

## Verify device connectivity performance for an optimal user experience. 
5G devices will access different radio access technologies (RATs), including 5G New Radio (NR), 4G Long Term Evolution (LTE) & Wi-Fi. 
Operators need to evaluate real-world performance & handovers between radio networks. 
This real-world evaluation is known as the inter-RAT handover test.

## Check that radio access network (RAN) elements conform to specifications. 
Before release into the market, all 5G devices & base stations must meet a minimum level of performance. 
3GPP & the O-RAN Alliance define what & how to measure for compliance against the core specifications.

## Perform interoperability testing for seamless interaction. 
O-RAN brings the disaggregation of 5G base stations into various elements. 
Validating interoperability & performance against expected use models helps ensure seamless interaction.

## Stress your RAN & core networks with 5G traffic. 
Ensure that your RAN & core networks meet your high performance, low latency & robust reliability requirements under load.

## Ensure that your infrastructure runs in a virtual, cloudified environment. 
To migrate from 5G non-standalone (NSA) to standalone (SA), you need to take advantage of network functions virtualization infrastructure (NFVI) &
virtualized network functions (VNF), using virtualization, containerization & cloud technologies.

## Measure & analyze the air interface in the field. 
The physical layer standards in 5G NR Release 15 & beyond define a flexible air interface to support the many use cases expected in 5G. 
Field test your air interface to ensure that it performs as expected.

## Test your network with real devices to assess performance. 
Stress test your network with 5G user equipment (UE) traffic under different use case scenarios to ensure that it meets key performance metrics like high data throughput, reliability &low latency.

## Observe 5G traffic to ensure high QoE for subscribers. 
5G & O-RAN increase the number of interfaces in mobile networks & the specifications leave room for interpretation. 
Ensure complete observability using precise data correlation & analytics.


# Tags

+ scripts
+ language

---

+ [inframonit/bash](https://github.com/inframonit/bash)
