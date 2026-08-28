---
layout: page
title: SUPPORT
order: 30
---

## Online Assistance

If you require assistance, please join our community forum by following these steps:

1. Register at our forum (REGISTER▸)
2. Login (FORUM▸)

Once registered, you will gain access to a range of features, including searching for solutions, asking questions, starting discussions, reporting bugs, requesting new features, and receiving support.

Registered users may also gain early access to the latest versions of our tools, 
ahead of releases on GitHub, and detailed instructions for setting up the cloud computation package
(available for download from [**TOOLS**]({% link tools.md %})). 


## Additional Support Resources

- **Technical Support Email**: For direct support, contact our technical team any time by pressing this button:
<span class="about-email" onclick="openEmailClient()">Email</span>.
- **Online User Guide and FAQ**: Access our detailed user guide and frequently asked questions, 
which provide valuable insights and troubleshooting tips for common issues, 
BrainCell ([BRAINCELL User Guide]({% link assets/BRAINCELL_User_Guide.pdf %})), 
ARACHNE ([Arachne User Guide]({% link assets/ARACHNE_UserManual.pdf %})), 
ASTRO ([ASTRO User Guide]({% link assets/ASTRO_User_Guide_v7.pdf %})).
- **Tutorial Videos**: Watch step-by-step videos on our YouTube channel to help you get started
and advance through complex setups ([YouTube User Guide](https://www.youtube.com/watch?v=sCMdTD4Q2OA)).
- **Community-Source Knowledge Base**: Contribute to and learn from a vast repository of 
user-generated content, from custom scripts to innovative use cases.

We are committed to providing ongoing updates and enhancements based on user feedback. 

<script>
function openEmailClient() {
  function oES() {
    var empty = '' + ' ' + String.fromCharCode(32); 
    return empty.trim();
  }

  function genEmail() {
    var user = 'sav'+oES()+'tch'+oES()+'enko';
    var s1 = String.fromCharCode(64);
    var s2 = String.fromCharCode(46);
    var domain = 'ya'+oES()+'hoo' + s2 + 'com';
    return user + s1 + oES() + domain;
  }

  window.location.href = 'mailto:' + genEmail();
}
</script>

