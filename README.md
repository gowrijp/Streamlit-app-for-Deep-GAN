# Streamlit-app-for-Deep-GAN

- Nvidia's PG-GAN used to synthesize photorealistic human faces. 
- Then using Shaobo Guan's TL-GAN model, we’ll create an app that gives us the ability to tweak GAN-synthesized celebrity faces by attributes like age, smileyness, male likeness, and hair color.
- This demo depends on Tensorflow 1, which does not support Python 3.7 or 3.8, so you’ll need Python 3.6. On Windows, the Anaconda Navigator allows you to pick your Python version with a point-and-click interface.
- In Navigator, click the Environments tab, then click the Create button. The Create new environment dialog box appears.
- In the Environment name field, type a descriptive name for your environment.
- In the Packages list select “Python” and in the Python version list select the version you want to use and click create.
- Select open terminal from our activated env   

There’s one issue though : the TensorFlow session object can mutate internally as we use it to run different computations. Ordinarily, we don’t want cached objects to mutate, as that can lead to unexpected results. So when Streamlit detects such mutations, it issues a warning to the user. However, in this case we happen to know that it’s OK if the TensorFlow session object mutates, so we bypass the warning by setting allow_output_mutation=True

