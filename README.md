![tmsh2iapp main diagram](https://github.com/f5devcentral/f5-tmsh2iapp/wiki/images/tmsh2iapp_main_diagram.png)

# f5-tmsh2iapp
 tmsh2iapp is an iApp generator using existing configurations as a template. The resulting iApps are **fully parametrizable**. It also generates Ansible playbooks & roles, Heat templates and iWorkflow JSON files to deploy them 
 
The purpose of this project is to make as easy as possible deploying services in the F5, 
automate and orchestrate them with third party SDN/NFV/Automation/Orchestration products.

One of the goals of the tool is that it's use is as simply as possible: iApp development knowlege is **not required**
but some fluency in tmsh syntax is recommended.

# Main characteristics of tmsh2iapp

* Allows creating an iApp using a **declarative** tmsh-like syntax (these are called .t2i files)
* It has been used with **LTM, ASM (limited support in v12 full support in v13+), APM, AFM and PEM modules**.
* Baseline .t2i files can be created easily with the BIG-IP GUI
* Helps deploying the iApp by creating sample Ansible roles & playbooks, Heat templates and iWorkflow JSON files
* Input varialbles can be **JSON lists** (ie: multiple-choice/multiple-select **survey variables in Ansible Tower**)
* Can easily create **iApps that contain base configurations (self-IPs, VLANs, etc...) that can be deployed in a BIG-IP cluster and config-sync'ed assigning per-BIG-IP values appropiately**.
* It can be used in any computer with perl installed -- including the BIG-IP
* It supports **passing parameters as JSON lists** (useful for handling multiple-choice/multiple-select survey variables in Ansible Tower or any other YAML based automation)
* It is not BIG-IP version specific but it is being tested with BIG-IP 11.6-13.1
* Supports **route-domains and partitions**
* Supports LTM policies
* It allows **importing (from external files or URL) the following configuration objects**:
    * apache-ssl-cert          SSL certificates management
    * asm-policy
    * browser-capabilities-db  browser capabilities DB file management
    * dashboard-viewset
    * data-group               External Data Group files management
    * device-capabilities-db   Device capabilities DB file management
    * external-monitor         External Monitor files management
    * ifile                    iFile files management
    * lwtunneltbl              LW4o6 table files management
    * ssl-cert                 SSL certificates management
    * ssl-crl                  SSL CRL files management
    * ssl-csr                  SSL Certificate Signing Request
    * ssl-key                  SSL certificate keys management


# Alternatives to tmsh2iapp

The world is full of choices! Please consier these:

* BIG-IQ 6.0 supports creation of configuration templates, several BIG-IP modules are supported too. It also provides ansible modules for deploying.
* ![Application Services 3 (AS3)](http://clouddocs.f5.com/products/extensions/f5-appsvcs-extension/3/) provides another F5 supported way deploying configurations in a declarative fashion. 

These two are excellent alternatives and they are officially supported by F5. On the other hand official F5 support of tmsh2iapp is limited to the API usage that tmsh2iapp makes use of BIG-IP. This non-official open-source project will provide support on a best effort basis.

tmsh2iapp plus points are:
* tmsh2iapp doesn't intend to know much about the intended configuration: configuration parsing is left up to the BIG-IP. This makes tmsh2iapp simpler to maintain and more flexible with respect of what configuration can accept and which BIG-IP versions are supported.
* tmsh2iapp iApps doesn't require an intermediary device - in the case of BIG-IQ - or intermediary REST nodejs worker (aka API Services Gateway) - in the case of AS3.

# Using tmsh2iapp

**Download the tool from ![this link](https://raw.githubusercontent.com/f5devcentral/f5-tmsh2iapp/master/tmsh2iapp.pl).**

**Please refer to ![project's wiki page](https://github.com/f5devcentral/f5-tmsh2iapp/wiki/) for documentation, examples and guidelines of use.**

This tool is not supported by F5 support. If you find an issue, we would love to hear about it. Please let us know by [filling an issue](https://github.com/f5devcentral/f5-tmsh2iapp/issues) in this repository. Tell us as much as you can about what you found, how you found it, your environment, etc.. We also welcome you to file feature requests as issues.

If you have any question post it in https://devcentral.f5.com/questions. Note there is also a [Frequently Asked Questions page](https://github.com/f5devcentral/f5-tmsh2iapp/wiki/02-%7C-FAQ)
We would love to hear your experiences with this tool, please share them in [this link of devcentral](https://devcentral.f5.com/codeshare/tmsh2iapp-iapp-generator-create-iapps-in-minutes-1065).

**tmsh2iapp is released to the community under the [Apache v2 license](http://www.apache.org/licenses/LICENSE-2.0.txt)**. It is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.


