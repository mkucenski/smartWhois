# smartJSONwhois

The idea here is to create an intelligent interface to the world of "WHOIS" that digs deep to get the most accurate/specific information and returns results in a normalized, JSON format.

## Features

The features I am trying to mirror come from Hexillion (https://hexillion.com/whois/):

* "Automatically determines the correct domain to get records for when given an arbitrary domain name. For example, when given www.yahoo.com it determines that the name to send in the query to the whois server is yahoo.com. A trickier example: given athletic.shoe.shopping.seoul.kr, the correct query domain is shopping.seoul.kr."
* "Automatically finds and queries the correct Whois server for IP addresses, gTLD domains, and ccTLD domains"
* "Works with both thick and thin Whois registries—follows referral chains, doing multiple queries as needed to get the most specific results"
* "Normalizes end-of-line characters in server responses (changes all single CRs and LFs to CRLF pairs)"
* "Normalizes the character sets of Whois records to Unicode"
* "Separates header and footer text (terms of service, advertisements) from record text"
* "Parses record text into consistent, well-defined fields"
* "Returns an indication of whether a domain is available (i.e., whether the query found a matching record)"
* "Is regularly tested and updated for accuracy"
* "Includes parsing support for the 5 major regional registries (ARIN, RIPE, APNIC, LACNIC, AFRINIC)."
* "Includes parsing support for over 90% of .com, .net, and .org domains. See the coverage details."

While the regional registries provide a certain level of detail for IP addresses, domain names require a more comprehensive list of whois servers (ref. https://hexillion.com/whois/coverage.htm).

## ICANN gTLD Registry List

* Available at: https://www.icann.org/resources/pages/listing-2012-02-25-en
	* This list shows verisign as controlling the .com gTLD; how much data does Verisign keep, and how do we dig deeper (e.g. GoDaddy...)
* gTLD list: http://data.iana.org/TLD/tlds-alpha-by-domain.txt

## RWhois???
* http://projects.arin.net/rwhois/
* https://www.arin.net/resources/request/reassignments_rwhois.html
* https://en.wikipedia.org/wiki/WHOIS#RWhois
* 