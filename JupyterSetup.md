# Install Jupyter
  
## Mac os
	1. Install python 3.6 
  
	2. Check pip3 version (>19.0)
  
	$ pip3 --version
	pip 20.0.2 from /Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/pip (python 3.6)

	3. Install tensorflow
	$ pip3 install tensorflow
	# check tensorflow
	$ python3
	Python 3.6.0 (v3.6.0:41df79263a11, Dec 22 2016, 17:23:13) 
	[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
	Type "help", "copyright", "credits" or "license" for more information.
	>>> import tensorflow as tf
	>>> tf.test.
	tf.test.assert_equal_graph_def(    tf.test.is_built_with_cuda(       
	tf.test.Benchmark(                 tf.test.is_built_with_gpu_support(
	tf.test.benchmark_config(          tf.test.is_built_with_rocm(       
	tf.test.compute_gradient(          tf.test.is_gpu_available(         
	tf.test.create_local_cluster(      tf.test.main(                     
	tf.test.gpu_device_name(           tf.test.TestCase(  
	

	4. Install others
	$ pip3 install numpy pandas matplotlib sklearn
	# install notebook
	$ pip3 install notebook
	
	# start notebook
	$ jupyter notebook
	[I 16:10:30.903 NotebookApp] Writing notebook server cookie secret to /Users/tiapeng/Library/Jupyter/runtime/notebook_cookie_secret
	[I 16:10:31.024 NotebookApp] Serving notebooks from local directory: /Users/tiapeng
	[I 16:10:31.024 NotebookApp] The Jupyter Notebook is running at:
	[I 16:10:31.025 NotebookApp] http://localhost:8888/?token=115b644033dff66d18b9d59cbda78b5816d4556c1cee42f3
	[I 16:10:31.025 NotebookApp]  or http://127.0.0.1:8888/?token=115b644033dff66d18b9d59cbda78b5816d4556c1cee42f3
	[I 16:10:31.025 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
	[C 16:10:31.029 NotebookApp] 
	    
	    To access the notebook, open this file in a browser:
	        file:///Users/tiapeng/Library/Jupyter/runtime/nbserver-71510-open.html
	    Or copy and paste one of these URLs:
	        http://localhost:8888/?token=115b644033dff66d18b9d59cbda78b5816d4556c1cee42f3
	     or http://127.0.0.1:8888/?token=115b644033dff66d18b9d59cbda78b5816d4556c1cee42f3
![image](https://user-images.githubusercontent.com/3377450/229104215-13129885-2cc6-4391-9309-5ff7e307050e.png)



### Error
$ jupyter notebook

[I 16:33:30.264 NotebookApp] KernelRestarter: restarting kernel (1/5), new random ports
Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/application/current.py", line 6, in <module>
    from contextvars import ContextVar
ModuleNotFoundError: No module named 'contextvars'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/runpy.py", line 193, in _run_module_as_main
    "__main__", mod_spec)
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/runpy.py", line 85, in _run_code
    exec(code, run_globals)
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/ipykernel_launcher.py", line 15, in <module>
    from ipykernel import kernelapp as app
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/ipykernel/__init__.py", line 2, in <module>
    from .connect import *
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/ipykernel/connect.py", line 13, in <module>
    from IPython.core.profiledir import ProfileDir
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/IPython/__init__.py", line 56, in <module>
    from .terminal.embed import embed
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/IPython/terminal/embed.py", line 16, in <module>
    from IPython.terminal.interactiveshell import TerminalInteractiveShell
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/IPython/terminal/interactiveshell.py", line 19, in <module>
    from prompt_toolkit.enums import DEFAULT_BUFFER, EditingMode
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/__init__.py", line 16, in <module>
    from .application import Application
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/application/__init__.py", line 1, in <module>
    from .application import Application
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/application/application.py", line 38, in <module>
    from prompt_toolkit.buffer import Buffer
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/buffer.py", line 28, in <module>
    from .application.current import get_app
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/application/current.py", line 8, in <module>
    from prompt_toolkit.eventloop.dummy_contextvars import ContextVar  # type: ignore
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/eventloop/__init__.py", line 1, in <module>
    from .async_generator import generator_to_async_generator
  File "/Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages/prompt_toolkit/eventloop/async_generator.py", line 5, in <module>
    from typing import AsyncGenerator, Callable, Iterable, TypeVar, Union
ImportError: cannot import name 'AsyncGenerator'



Fix:
$ pip3 install -U prompt-toolkit==2.0.10
Collecting prompt-toolkit==2.0.10
  Downloading prompt_toolkit-2.0.10-py3-none-any.whl (340 kB)
     |████████████████████████████████| 340 kB 836 kB/s 
Requirement already satisfied, skipping upgrade: six>=1.9.0 in /Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages (from prompt-toolkit==2.0.10) (1.14.0)
Requirement already satisfied, skipping upgrade: wcwidth in /Library/Frameworks/Python.framework/Versions/3.6/lib/python3.6/site-packages (from prompt-toolkit==2.0.10) (0.1.8)
Installing collected packages: prompt-toolkit
  Attempting uninstall: prompt-toolkit
    Found existing installation: prompt-toolkit 3.0.3
    Uninstalling prompt-toolkit-3.0.3:
      Successfully uninstalled prompt-toolkit-3.0.3
Successfully installed prompt-toolkit-2.0.10
LM-SHB-24502178:~ tiapeng$ jupyter notebook
![image](https://user-images.githubusercontent.com/3377450/229104307-c6909411-d341-4369-a6ae-74cc253bd932.png)
  
  

  
