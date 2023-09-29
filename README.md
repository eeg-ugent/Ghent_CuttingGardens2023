# 1. General Information
From 16/10/2023 to 19/10/2023, the department of experimental psychology at Ghent University will be hosting talks and workshops on EEG methods, with a special focus on machine learning methods and their application in a scientific context. The program will be a mix of online talks offered by the [CuttingGardens](https://cuttinggardens2023.org/) organization, and locally invited speakers. We offer a series of tutorials on [MNE-python](https://mne.tools/stable/index.html). Materials and instructions for these workshops can be found in this repository. ![Timetable of talks and workshops](https://cuttinggardens2023.org/wp-content/uploads/2023/09/Ghent-timetable-3.png)

# 2. Preparation for the tutorials
If you wish to participate in the tutorials, please run through these instructions to make sure you have the required python prerequisites and data sets ready on your own machine. This way you can fully focus on the usage of MNE-python during the tutorials, without having to wait for any installation to complete. If you run into any problems while following the steps outlined below, feel free to contact sven.wientjes@ugent.be. Problems are common, so please do not hesitate to reach out.

### 2.1. Install MNE
- Download [Anaconda Navigator](https://www.anaconda.com/download) by surfing to the linked page and clicking the green "Download" button. ![DownloadButton](https://github.com/eeg-ugent/Ghent_CuttingGardens2023/assets/36112808/af304350-d4ea-47a2-9e0f-456617e67c92)
- Open the "Anaconda Prompt (anaconda3)" program now installed on your machine. This is not the Anaconda Navigator! The Anaconda Prompt should open a command terminal where you can type basic commands.
- We will create a dedicated environment for using MNE. You can do this by running `conda create -n MNE-EEG python=3.9`. You can replace the name `MNE-EEG` with whatever you want. We will use Python 3.9, which is not the latest version but is stable with most packages we will be using. Anaconda will quickly install some basic packages and ask you for permission to do so by showing `Proceed ([y]/n)?`. You can continue by running the letter `y`.
- Activate this new environment by running `conda activate MNE-EEG`. The `(base)` you could see before each line in your terminal should now have switched to saying `(MNE-EEG)`. 
- Install MNE and all its core dependencies into this new environment by running `conda install -n MNE-EEG mne-base`.
  - (Note: Some recent issues with anaconda which I ran into myself can give you an error "OpenSSL appears to be unavailable on this machine". The solution can be found [here](https://github.com/conda/conda/issues/11795#issuecomment-1680167888).)

### 2.2. Run MNE in Spyder
- During our tutorials, we will be using [Spyder](https://www.spyder-ide.org/), which is an "integrated development environment (IDE)". An IDE allows you to easily write long scripts, while executing code on the fly, and visualizing data currently loaded in memory. This is very convenient when working with EEG data.
- To make our MNE-EEG environment work in Spyder, we have to install the relevant "spyder kernel" in our environment. You can do this by opening a new "Anaconda Prompt (anaconda3)" terminal. Then, navigate to the MNE-EEG environment by running `conda activate MNE-EEG`. We can install the kernel by running `conda install -n MNE-EEG spyder-kernels=2.1`.
- The actual spyder program itself is installed automatically in the `(base)` environment. We can open it by navigating back to base by running `conda activate base` and then running `spyder`.
  - When you want to open spyder in the future, you can open a new "Anaconda Prompt (anaconda3)" terminal. Make sure you are in the `(base)` environment, otherwise run `conda activate base`. From there, you can always open spyder by running `spyder`.
- We have to select the MNE-EEG environment in order to be able to use mne within Spyder:
  - Open the settings menu by navigating to "Tools" -> "Preferences" ![afbeelding](https://github.com/eeg-ugent/Ghent_CuttingGardens2023/assets/36112808/1a9926f3-9b9b-4ced-a783-463d14b91519)
  - Select the MNE-EEG environment as the python interpreter by selecting "Use the following Python interpreter:" and from the dropdown menu, select the option saying "MNE-EEG". ![afbeelding](https://github.com/eeg-ugent/Ghent_CuttingGardens2023/assets/36112808/5226f8c1-d702-43f9-8738-a9569e29f7de)
  - Click on "Apply" and then "OK".
  - Close and reopen Spyder.
- You can test whether mne is currently working in Spyder by running `import mne` in the Spyder console.
  - (Note: If the Spyder console gives an error saying "your python environment doesn't have the `spyder-kernels` module...", you can install the required version of the spyder kernel by opening a new "Anaconda Prompt (anaconda3)", running `conda activate MNE-EEG`, and installing the correct version `conda install -n MNE-EEG spyder-kernels=...`, replacing the `...` with the version as listed by Spyder. ![afbeelding](https://github.com/eeg-ugent/Ghent_CuttingGardens2023/assets/36112808/0b3efcff-a78a-4bf7-af11-4786025f69c2)




