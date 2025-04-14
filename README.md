# phishing-detect
List of malicious domains targeting Web3 users.

For checking why a given domain was blocked, there is a third-party search tool maintained by ChainPatrol.

Contributions
To keep a tidy file, use the CLI or library functions to modify the list.

Adding new domains
yarn add:blocklist crypto-phishing-site.tld
yarn add:allowlist legitimate-site.tld
addDomains(config, "blocklist", ["crypto-phishing-site.tld"]);
addDomains(config, "allowlist", ["legitimate-site.tld"]);
Removing existing domains
yarn remove:blocklist legitimate-site.tld
yarn remove:allowlist malicious-site.tld
removeDomains(config, "blocklist", ["legitimate-site.tld"]);
removeDomains(config, "allowlist", ["crypto-phishing-site.tld"]);

Auditing submissions & removals
Running the command below will pull all pull requests associated to example.com.

git log -S "example.com" -- src/config.json
