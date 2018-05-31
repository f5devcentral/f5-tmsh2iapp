![tmsh2iapp main diagram](https://github.com/f5devcentral/f5-tmsh2iapp/wiki/images/tmsh2iapp_main_diagram.png)

# f5-tmsh2iapp
 tmsh2iapp is an iApp generator using existing configurations as a template. The resulting iApps are **fully parametrizable**. It also generates Ansible playbooks & roles, Heat templates and iWorkflow JSON files to deploy them 
 
The purpose of this project is to make as easy as possible deploying services in the F5, 
automate and orchestrate them with third party SDN/NFV/Automation/Orchestration products.

One of the goals of the tool is that it's use is as simply as possible: iApp development knowlege is **not required**
but some fluency in tmsh syntax is recommended.

# Main characteristics of tmsh2iapp

* Allows creating an iApp using a **declarative** tmsh-like syntax (these are called .t2i files)
* It has been used with **LTM, ASM, APM, AFM and PEM modules**.
* Baseline .t2i files can be created easily with the BIG-IP GUI
* Helps deploying the iApp by creating sample Ansible roles & playbooks, Heat templates and iWorkflow JSON files
* Can easily create **iApps that contain base configurations (self-IPs, VLANs, etc...) that can be deployed in a BIG-IP cluster and config-sync'ed assigning per-BIG-IP values appropiately**.
* It can be used in any computer with perl installed -- including the BIG-IP
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


# Using tmsh2iapp

**Download the tool from ![this link](https://raw.githubusercontent.com/f5devcentral/f5-tmsh2iapp/master/tmsh2iapp.pl).**

**Please refer to ![project's wiki page](https://github.com/f5devcentral/f5-tmsh2iapp/wiki/) for documentation, examples and guidelines of use.**

This tool is not supported by F5 support. If you find an issue, we would love to hear about it. Please let us know by [filling an issue](https://github.com/f5devcentral/f5-tmsh2iapp/issues) in this repository. Tell us as much as you can about what you found, how you found it, your environment, etc.. We also welcome you to file feature requests as issues.

If you have any question post it in https://devcentral.f5.com/questions. Note there is also a [Frequently Asked Questions page](https://github.com/f5devcentral/f5-tmsh2iapp/wiki/Frequently-Asked-Questions) in the tmsh2iapp wiki.

We would love to hear your experiences with this tool, please share them in [this link of devcentral](https://devcentral.f5.com/codeshare/tmsh2iapp-iapp-generator-create-iapps-in-minutes-1065).

**tmsh2iapp is released to the community under the [Apache v2 license](http://www.apache.org/licenses/LICENSE-2.0.txt)**. It is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
