# Relightable Gaussian Splatting for Virtual Production using Image-based Illumination
(CC BYs 4.0 license)

**[Project Page](https://azzarelli.github.io/relightingpage/index.html) | [Paper (arXiv)](https://arxiv.org/abs/2605.09024) | [Paper (ACM Digital Library)](TBD)**


## SIGGRAPH Asia 2026 - Technical (Conference) Papers


by [Adrian Azzarelli](https://azzarelli.github.io/), [Nantheera (Pui) Anantrasirichai](https://pui-nantheera.github.io/), [James Pollock](https://www.linkedin.com/in/james-w-pollock/), [David (Dave) R Bull](https://david-bull.github.io/)

[Visual Information, University of Bristol](https://vilab.blogs.bristol.ac.uk/) x [Lux Aeterna VFX](https://www.lavfx.com/)




# Code Installation and Run

*Just use Claude to install and understand the run-CLI-pattern...*

This has been tested on Nvidia RTX 3090 w/ py3.10 pt2.4 and cu11.8, Nvidia RTX 4090 w/ py3.10 pt2.4 and cu12.4 and Nvidia H100 w/ py3.10 pt2.4 and cu12.4.

**Steps:**
1. Create a conda environment with `conda create -n VP3DGS python=3.10` (pytorch version requires compatibility with `gsplat`; I use py310 and gsplat=1.53)

2. Install pytorch (requires compatibility with `gsplat`; I use pt24)

3. Download `gsplat` either via `pip install gsplat` or with wheel (I used `gsplat-1.5.3+pt24cu124-cp310-cp310-linux\_x86\_64.whl`)

4. Run `pip install -r requirements.txt`

5. Use `bash run.sh SRC NAME ARGS` to run the method



`SRC` should be the file path to the data folder. This should end with e.g. ".../scene1" or ".../scene2" or ".../scene3".



`Name` is the experiment name



`ARGS` is the dataset-subset we want to train. Choose from `\[1, 2, 3]`. See DATA_Instruction.md for more infor.


For viewing the results, `ARGS= "view \[checkpoint iteration]"`, where `\[checkpoint iteration]` should be replaced by the checkpoint iteration you want to view/load.


# Training Viewer

- View the scene from the training and testing views
- Change the render flags to view depth, XYZ, or any of the other AOVs
- Provides active testing and rendering stats
- Drag the slider to change the background image
- Switch on/off viewing the final relit scene - Note that if this is activated then the other render flags will not work


# Post-Training Viewer

- To pose the background mesh, hit the button and drag the corners of the input texture 
- Insert a path to a background video and play/save the resulting render
- Save the current frame

# Citation

```
@article{azzarelli2026relightable,
    author={Azzarelli, Adrian and Anantrasirichai, Nantheera and Pollock, James and Bull, David R.},
    title={Relightable Gaussian Splatting for Virtual Production Using Image-Based Illumination},
    journal={arXiv preprint arXiv:2605.09024},
    year={2026}
}
```





