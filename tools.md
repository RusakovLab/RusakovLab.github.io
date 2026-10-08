---
layout: page
title: TOOLS
order: 10
---

### Computational Tools

   <hr>
   <br> 
   **OPEN SOURCE COMMITMENT:** Our software packages are open for you to download, install, and explore under the permissive 3-clause BSD license. 
   <br>
   <hr>
   <br>

1. [**ASTRO**]({% link astro.md %}) is a computational platform for constructing and exploring realistic multi-compartmental astrocyte models that can be biophysically interrogated in NEURON computational environment, on the scale from nanometers to the entire cell morphology. ASTRO generates stochastically cell nanoscopic protrusions based on their real-world parameters and enables dynamic interactions between the modelled astrocyte and the surrounding 3D tissue environment.
 
   **Documentation:** 
   [PDF file]({% link assets/ASTRO_User_Guide_v7.pdf %}).<br>
<!-- ðŸ"„ Featured Publication: [_Disentangling astroglial physiology with a realistic cell model in silico._](https://www.nature.com/articles/s41467-018-05896-w)
   <br>Savtchenko LP, Bard L, Jensen TP, Reynolds JP, Kraev I, Medvedev N, Stewart MG, Henneberger C, Rusakov DA.<br>
   *Nat Commun. 2018 Sep 3;9(1):3554. doi: 10.1038/s41467-018-05896-w.* -->

   <hr>
2. [**ARACHNE**]({% link arachne.md %}) is designed to model multi-cell spiking networks of neurons and astrocytes. In ARACHNE environment, the network organisation, optimisation, and execution benefit from pre-set, optimised parallel algorithms for remote computations and a friendly user interface operated from your own computer. A neuroscientist without IT background should be able to incorporate the representative variety of biophysical mechanisms pertinent to nerve and astroglial cells, within a single network model.

   **Documentation:** 
   [PDF file]({% link assets/ARACHNE_UserManual.pdf %}).<br>
<!-- ðŸ"„ Featured Publication: [_ARACHNE: A neural-neuroglial network builder with remotely controlled parallel computing._](https://pubmed.ncbi.nlm.nih.gov/28362877/)
   <br>Aleksin SG, Zheng K, Rusakov DA, Savtchenko LP.<br>
   *PLoS Comput Biol. 2017 Mar 31;13(3):e1005467. doi: 10.1371/journal.pcbi.1005467.* -->

   <hr>
3. [**BRAINCELL**]({% link braincell.md %}) is a platform that combines theoretical aspects of computational neuroscience with real-world aspects of cell and tissue physiology of the brain, including the capacity to replicate some common experimental designs. The immersive modelling environment enables neuroscientists and neurologists to investigate brain cellular mechanisms and assess the physiological effects of experimental or therapeutic interventions. Its key features include stochastic generation of nano-morphology and function, stop-save-go control of simulation runs, dynamic extracellular and inter-cellular interactions, adaptive import of cell morphologies.     

   **Installation:** 
   
   *Update BRAINCELL* (Windows W10/W11 64-bit installers; choose one):
   [BrainCell-2026.03_x86_64_Neuron_9_Setup.exe]({% link assets/BrainCell-2026.03_x86_64_Neuron_9_Setup.exe %}) – bundled with NEURON 9.0.2 and Python 3.11<br>
   [BrainCell-2026.03_x86_64_Neuron_8_Setup.exe]({% link assets/BrainCell-2026.03_x86_64_Neuron_8_Setup.exe %}) – bundled with NEURON 8.2.2 and Python 3.11<br>
   No Anaconda or separate NEURON installation is required. Only one of the two versions can be installed at a time.<br>
   **Important note:** To run the Setup you will require password which you can find after
   **[[Registration at our FORUM]](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**.<br>
 
   **Installation instructions:**
   - [Quick Installation Guide](https://forum.neuroalgebra.net){:target="_blank"} (recommended - covers all platforms and scenarios) - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**
   - [Windows installation instructions]({% link assets/BrainCell Installation Guide Windows v2.docx %})
   - [Linux/macOS/Windows installation instructions]({% link assets/BrainCell Installation Guide 3 OS v2.docx %})
   - [Windows Sandbox testing guide](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**

   **Documentation:** 
   [PDF file]({% link assets/BRAINCELL_User_Guide.pdf %}), or in Word format
   [BRAINCELL_User_Guide.docx]({% link assets/BRAINCELL_User_Guide.docx %})
   (alternatively, check [experimental PDF->HTML conversion]({% link brdoc.md %})).
   
   **AI Agent Resources:**
   Get started with BRAINCELL using our comprehensive guides:

   - [Setup & Installation AI Guide]({% link /assets/BrainCell_Agent_Setup_Manual.html %}) – A step-by-step technical walkthrough for AI initial configuration.

   - [End-User AI Manual]({% link /assets/BrainCell_Agent_User_Manual.html %}) – Best practices and daily operations for the BRAINCELL AI Agent.
   
   
 
   **Additional Resources:**
   - [GitHub Repository](https://github.com/RusakovLab/BrainCell){:target="_blank"}
   - [Forum Support & Downloads](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**
   - [Installation Package Download](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**
   - [Third-Party Notices]({{ '/assets/THIRD_PARTY_NOTICES.md' | relative_url }}) – licences for bundled components
   - [Python Requirements]({{ '/assets/requirements.txt' | relative_url }}) – tested package versions

   <br>
   <hr>
4. **CLOUD COMPUTATION PLUGIN:** we are currently working with
   [Neuroscience Gateway - a portal for computational Neuroscience](https://www.nsgportal.org/overview.html)
   to enable computations on their [HPC](https://en.wikipedia.org/wiki/High-performance_computing) 
   supercomputer. When the integration is complete, registered Neuroalgebra users will be able to benefit from 
   the HPC power and run our tools on a supercomputer cluster in the cloud.

   **Installation:** 
   Please inquire about the current status of our cloud computation package in a discussion group on our forum.
   To register at the forum follow this link:
   **[[Registration at our FORUM]](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**.

<br>

---
---
---

## BrainCell Installation Guide

### Choose Your Category

**Category 1:** NEURON + Python already working → [Quick Setup](#category-1--quick-setup)  
**Category 2:** Clean system (nothing installed) → [Fresh Install](#category-2--fresh-install)  
**Category 3:** Partial installation or problems → [Clean Reinstall](#category-3--clean-reinstall)

---

### Category 1 – Quick Setup
*You already have NEURON and Python working*

1. Download `cloudpackage-v1.zip` from [forum](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**
2. Create folder: `C:\braincell` (Windows) or `~/braincell` (Mac/Linux)
3. **Unblock the ZIP:** Right-click → Properties → ☑️ Unblock → Apply (Windows only)
4. Extract ZIP to your folder
5. **Windows:** Unblock `init.bat`, then double-click it
6. **Mac/Linux:** The graphical environment is not yet available on these platforms. To run an exported model, compile the mechanisms with `nrnivmodl` (put the MOD files from `Mechanisms/Common/MOD_files` and `Mechanisms/Neuron/MOD_files` – or `Mechanisms/Astrocyte/MOD_files` for astrocyte models – into one folder and run `nrnivmodl` there; the `nrnmech.dll` files in the package are Windows-only), then launch via `nrniv -python <exported_model>.hoc`

**Done!** BrainCell window opens (Windows only).

---

### Category 2 – Fresh Install
*Nothing installed yet*

#### Windows (Easiest Method)

**All-in-One Installer (Recommended):**
1. Download [BrainCell-2026.03_x86_64_Neuron_9_Setup.exe]({% link assets/BrainCell-2026.03_x86_64_Neuron_9_Setup.exe %}) (NEURON 9.0.2) or [BrainCell-2026.03_x86_64_Neuron_8_Setup.exe]({% link assets/BrainCell-2026.03_x86_64_Neuron_8_Setup.exe %}) (NEURON 8.2.2)
2. Password available after [forum registration](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}
3. Run the installer
4. Follow installation prompts
5. **Done!** Launch BrainCell from Start Menu or Desktop

**Time:** 15-30 minutes

---

**Manual Installation (Alternative):**

1. Install [Anaconda 2023.09](https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Windows-x86_64.exe) ([all versions](https://repo.anaconda.com/archive/), SHA256: `810da8bff79c10a708b7af9e8f21e6bb47467261a31741240f27bd807f155cb9`)
   - BrainCell is tested with Anaconda3 2023.09-0 (Python 3.11.5). Download it from the official Anaconda archive; do not use third-party mirrors.
   - Choose "Just Me"
   - ☑️ Add Anaconda to PATH
   - Restart Windows
2. Install [NEURON 8.2.2](https://github.com/neuronsimulator/nrn/releases/tag/8.2.2)
   - Use default options
   - Restart Windows
3. Follow [Category 1 steps](#category-1--quick-setup)

**Time:** 30-60 minutes

---

#### macOS

1. Install the Xcode Command Line Tools (needed by `nrnivmodl` to compile mechanisms): `xcode-select --install`
2. Install [Anaconda 2023.09](https://repo.anaconda.com/archive/) (Python 3.11): `Anaconda3-2023.09-0-MacOSX-arm64.pkg` for Apple Silicon or `Anaconda3-2023.09-0-MacOSX-x86_64.pkg` for Intel Macs. Newer Anaconda releases ship a Python that NEURON 8.2.2 does not support.
3. Install NEURON and the Python packages into Anaconda:

```bash
pip install neuron==8.2.2
pip install -r https://neuroalgebra.net/assets/requirements.txt
```

4. Follow [Category 1 steps](#category-1--quick-setup)

**Time:** 30-60 minutes

---

#### Linux

```bash
# Install Anaconda
wget https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh
bash Anaconda3-2023.09-0-Linux-x86_64.sh
source ~/.bashrc

# Compiler for nrnivmodl (Ubuntu/Debian)
sudo apt-get install build-essential

# Install NEURON and Python packages into Anaconda
pip install neuron==8.2.2
pip install -r https://neuroalgebra.net/assets/requirements.txt

# Follow Category 1 steps
```

**Time:** 30-60 minutes

---

### Category 3 – Clean Reinstall
*Partial installation or not working*

#### ⚠️ Critical: Remove Everything First

**Windows:**
1. Uninstall NEURON and Anaconda (Settings → Apps)
2. Delete folders: `C:\nrn`, `C:\Users\[You]\anaconda3`
3. **Restart Windows**

**macOS:**
```bash
rm -rf ~/anaconda3 ~/.conda /Applications/NEURON  # /Applications/NEURON only if installed from the .pkg
```
Restart Mac

**Linux:**
```bash
rm -rf ~/anaconda3 ~/.conda  # removes Anaconda together with pip-installed NEURON
```
Restart

#### Now Follow Category 2

After removing everything, follow [Category 2 Fresh Install](#category-2--fresh-install).

**Recommended:** Use the all-in-one installer for Windows: [BrainCell-2026.03_x86_64_Neuron_9_Setup.exe]({% link assets/BrainCell-2026.03_x86_64_Neuron_9_Setup.exe %}) (NEURON 9.0.2) or [BrainCell-2026.03_x86_64_Neuron_8_Setup.exe]({% link assets/BrainCell-2026.03_x86_64_Neuron_8_Setup.exe %}) (NEURON 8.2.2).

**Time:** 45-75 minutes

---

### Testing in Windows Sandbox (Reviewers & Advanced Users)

For those with Windows 10/11 Pro, you can test BrainCell in an isolated environment without affecting your main system:

1. **Enable Windows Sandbox:**
   - Press **Win + R**
   - Type: `optionalfeatures`
   - Check ☑️ **Windows Sandbox**
   - Click **OK** and restart

2. **Follow detailed sandbox testing guide:**
   [Windows Sandbox Setup Guide](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**

**Benefits:**
- Clean testing environment
- No impact on main system
- Easy repeatability
- Complete reset between sessions

---

### Support & Resources

- **Forum:** [https://forum.neuroalgebra.net](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**
- **GitHub:** [https://github.com/RusakovLab/BrainCell](https://github.com/RusakovLab/BrainCell){:target="_blank"}
- **Installation Downloads:** [Forum Topic](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**
- **Sandbox Testing:** [Forum Guide](https://forum.neuroalgebra.net){:target="_blank"} - **[Registration required](https://forum.neuroalgebra.net/ucp.php?mode=register){:target="_blank"}**

---

### System Requirements

**Minimum:**
- RAM: 4 GB (8 GB recommended)
- Disk Space: 5 GB free
- Processor: 64-bit

**Operating Systems:**
- Windows 10/11 (64-bit) — graphical environment, full functionality
- macOS / Linux — running exported models only (GUI support in development)

---

**BrainCell Version:** 2026.03  
**Installation Guide Last Updated:** March 2026
