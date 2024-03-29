# Thirdlane Phone Directory Config Generator


- [x] implement Yealink config generator
- [ ] automatically detect server domain address. Currently implemented via config.yml
- [ ] automatically detect mysqlDB IP. Currently implemented via config.yml
- [ ] automatically detect filename for company.xml
- [ ] implement Polycom config generator
- [ ] add generated link to phone config

Thirdlane Phone Directory Config Generator is used to generate phone directory configuration file for phones.

### On Yealinks:
Directory -> Remote Phone Book
http://thirdlane.mydomain.com/provisioning/CONTACTS/yealink_directory/yea_phonebook_f9fa6e37380c532a33297aa288484b00.xml CompanyName

## Installation

### On Centos-based systems

copy binaries to the folder ...

``` bash
if [ ! -d /usr/local/utils/thirdlane_modules ]; then mkdir -p /usr/local/utils/thirdlane_modules; fi
cd /usr/local/utils/thirdlane_modules
git clone git@github.com:improcom/thirdlane.git thirdlane_directory_generator
chmod +x thirdlane_directory_generator/phone_directory_config_generator
cd thirdlane_directory_generator
#Edit config.yml as necessary.
rm -rf phone_directory_config_generator && git reset --hard && git pull && chmod +x phone_directory_config_generator && ./phone_directory_config_generator
```