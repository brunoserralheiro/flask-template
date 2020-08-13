# flask-template
Python Flask template 


If you are using a Python 3 version, virtual environment support is included in it, so all you need to do to create one is this:

$ python3 -m venv venv

With this command, I'm asking Python to run the venv package, which creates a virtual environment named venv. The first venv in the command is the name of the Python virtual environment package, and the second is the virtual environment name that I'm going to use for this particular environment. If you find this confusing, you can replace the second venv with a different name that you want to assign to your virtual environment. In general I create my virtual environments with the name venv in the project directory, so whenever I cd into a project I find its corresponding virtual environment.

Note that in some operating systems you may need to use python instead of python3 in the command above. Some installations use python for Python 2.x releases and python3 for the 3.x releases, while others map python to the 3.x releases.

After the command completes, you are going to have a directory named venv where the virtual environment files are stored.

If you are using any version of Python older than 3.4 (and that includes the 2.7 release), virtual environments are not supported natively. For those versions of Python, you need to download and install a third-party tool called virtualenv before you can create virtual environments. Once virtualenv is installed, you can create a virtual environment with the following command:

$ virtualenv venv

Regardless of the method you used to create it, you should have your virtual environment created. Now you have to tell the system that you want to use it, and you do that by activating it. To activate your brand new virtual environment you use the following command:

$ source venv/bin/activate
(venv) $ _

If you are using a Microsoft Windows command prompt window, the activation command is slightly different:

$ venv\Scripts\activate
(venv) $ _

When you activate a virtual environment, the configuration of your terminal session is modified so that the Python interpreter stored inside it is the one that is invoked when you type python. Also, the terminal prompt is modified to include the name of the activated virtual environment. The changes made to your terminal session are all temporary and private to that session, so they will not persist when you close the terminal window. If you work with multiple terminal windows open at the same time, it is perfectly fine to have different virtual environments activated on each one.

Now that you have a virtual environment created and activated, you can finally install Flask in it:

(venv) $ pip install flask

 Flask is installed and ready to be used.
 
 
 
 =============
 
 
 (venv) $ flask run
 * Serving Flask app "microblog"
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)

After the server initializes it will wait for client connections. The output from flask run indicates that the server is running on IP address 127.0.0.1, which is always the address of your own computer. This address is so common that is also has a simpler name that you may have seen before: localhost. Network servers listen for connections on a specific port number. Applications deployed on production web servers typically listen on port 443, or sometimes 80 if they do not implement encryption, but access to these ports require administration rights. Since this application is running in a development environment, Flask uses the freely available port 5000. Now open up your web browser and enter the following URL in the address field:

    http://localhost:5000/

Alternatively you can use this other URL:

    http://localhost:5000/index
