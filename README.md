# 1. General Information
From 16/10/2023 to 19/10/2023, the department of experimental psychology at Ghent University will be hosting talks and workshops on EEG methods, with a special focus on machine learning methods and their application in a scientific context. The program will be a mix of online talks offered by the [CuttingGardens](https://cuttinggardens2023.org/) organization, and locally invited speakers. We offer a series of tutorials on [MNE-python](https://mne.tools/stable/index.html). Materials and instructions for these workshops can be found in this repository. ![Timetable of talks and workshops](https://cuttinggardens2023.org/wp-content/uploads/2023/09/Ghent-timetable-3.png)

# 2. Preparation for the tutorials
If you wish to participate in the tutorials, please run through these instructions to make sure you have the required python prerequisites and data sets ready on your own machine. This way you can fully focus on the usage of MNE-python during the tutorials, without having to wait for any installation to complete. If you run into any problems while following the steps outlined below, feel free to contact sven.wientjes@ugent.be. Problems are common, so please do not hesitate to reach out.

### 2.1. Install MNE
- Download [Anaconda Navigator](https://www.anaconda.com/download) by surfing to the linked page and clicking the green "Download" button. ![DownloadButton](https://github.com/eeg-ugent/Ghent_CuttingGardens2023/assets/36112808/af304350-d4ea-47a2-9e0f-456617e67c92)
- Open the "Anaconda Prompt (anaconda3)" program now installed on your machine. This is not the Anaconda Navigator! The Anaconda Prompt should open a command terminal where you can type basic commands.
- We will create a dedicated environment for using MNE. You can do this by running `conda create -n MNE-EEG python=3.11`. You can replace the name `MNE-EEG` with whatever you want. We will use Python 3.11, which is the latest version of python at the time of writing. This will quickly install some basic packages and ask you for permission to do so by showing `Proceed ([y]/n)?`. You can continue by running the letter `y`.
- Activate this new environment by running `conda activate MNE-EEG`. The `(base)` you could see before each line in your terminal should now have switched to saying `(MNE-EEG)`. 
- MNE has a lot of "dependencies", which are other packages you need to have before MNE can work. We will first install an efficient package manager called "mamba" that will help us install the dependencies of MNE very quickly. You can install this by running `conda install --channel=conda-forge --name=base mamba`.
- Then, install MNE by running `mamba create --override-channels --channel=conda-forge --name=MNE-EEG mne`.

### 2.2. Run MNE in Spyder
- ...
