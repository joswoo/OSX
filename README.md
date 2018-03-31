# OSX(High Sierra)

## Install Xcode
- After Install

        $ sudo xcodebuild -license

        $ sudo xcode-select --install

## Homebrew
- Install
        
        $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

        $ brew update

        $ vi ~/.bash_profile

    Add this below code
    ```
    # Homebrew
    export PATH=/usr/local/bin:$PATH
    ```
    After save and quit
    
        $ source ~/.bash_profile

- Uninstall
        
        $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"

- Remove all installed packages

        $ brew remove --force $(brew list) --ignore-dependencies

        $ brew cleanup

## Python

        $ brew install python2

        $ brew linkapps python2

        $ brew install python3

        $ brew linkapps python3

To confirm that we are using the Homebrew version of Python

        $ which python
> /usr/bin/python

        $ which python2
> /usr/local/bin/python2

        $ which python3
> /usr/local/bin/python3


Check the Python version

        $ python -V

        $ python2 -V

        $ python3 -V

Upgrade pip

        $  sudo easy_install --upgrade pip2
        
        $  sudo easy_install --upgrade pip3

Check the pip version

        $ pip -V

        $ pip2 -V

        $ pip3 -V

## Numpy

        $ pip2 install numpy

        $ pip3 install numpy

## OpenCV

        $ brew install opencv3 --with-contrib --with-python2 --without-python
        $ pip install -U numpy

        $ brew install opencv3 --with-contrib --with-python3 --without-python
        $ pip3 install -U numpy
        
        $ python
        > >> import cv2
        > >> cv2.__version__

## TensorFlow
- Install

        $  sudo easy_install --upgrade pip2

        $  sudo easy_install --upgrade pip3

        $ sudo easy_install --upgrade six

        $ pip2 install tensorflow

        $ pip3 install tensorflow

        $ sudo pip3 install --upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.4.0-py2-none-any.whl

- Uninstall

        $ pip2 uninstall tensorflow

        $ pip3 uninstall tensorflow

## iPython

        $ pip2 install ipython

        $ pip3 install ipython

## Jupyter

        $ pip2 install jupyter

        $ pip3 install jupyter
        
## Virtualenv

        $ virtualenv -p python3 이름
        
        $ vi ~/.zshrc
        
        > 맨 아래에 추가 `alias 이름=". ~/이름/bin/activate"`
        
        

### Launch Jupyter over network

1. In a terminal, log in to the server and launch Jupyter notebook.

    $ ssh [ID]@[SERVER ADDRESS]

    $ cd [GO TO THE FOLDER YOU'RE WORKING ON] 

    [GO TO THE FOLDER YOU'RE WORKING ON] $ jupyter notebook --no-browser


> Look at this window
    http://`localhost:8888`/~~~~~~~

2.In a new terminal, establish a SSH tunnel between your local machine and the remote server. 

Please match the notebook with `localhost:`

    $ ssh -N -L localhost:8888:localhost:8888 [ID]@[SERVER ADDRESS]

Type your password and keep this window opened.

In a web browse and open the address provided by the notebook.
