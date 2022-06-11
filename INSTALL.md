# Installing Sage

## With an Active Anaconda Distribution (Linux, macOS, Windows Subsystem for Linux)

### 0. Setup

First, make sure you have a working ```conda``` installation. In a Unix terminal, run:

```
$ which conda
```

If this command returns a path, you are good to go. If not, stop here and install ```conda``` before continuing, or use one of the other options.

### 1. Install ```mamba```

```mamba``` is an alternative package manager for Anaconda that replaces the ```conda``` command. It is faster in many cases than the default ```conda```, and importantly, makes it much easier to install ```sage```.

Start by adding the ```conda-forge``` channel to Anaconda:

```
conda config --add channels conda-forge
```

Next, set the channel-priority setting to strict:

```
conda config --set channel_priority strict
```
Last, run the install:

```
conda install mamba
```

__Note:__ If this install fails, it may be because your version of Anaconda is not compatible with mamba. This can open a can of worms, especially if you do not want to switch Anaconda distributions. If this happens to you, reach out to Philip to explore solutions for your particular setup.

### 2. Install ```sage``` (and useful packages) in a new environment

```
mamba create -n sage sage jupyter numpy
```

### 3. Activate the environment

```
mamba activate sage
```

## As a Standalone App (Windows and macOS only)

_Note: I have not yet tested this on macOS._

### 0. Download the installer

- [Link for Windows](https://github.com/sagemath/sage-windows/releases)
- [Link for macOS](https://github.com/3-manifolds/Sage_macOS/releases)

### 1. Run the installer

(Hopefully self-explanatory, but let me know if you have issues)

### 2. Test installation

You should now have an app called "SageMath #.# Notebook" which opens a browser window showing a Jupyter notebook.
