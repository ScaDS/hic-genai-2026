# Setting up Jupyter4NFDI environment

Sign in using your Helmholtz ID to [https://hub.nfdi-jupyter.de/](https://hub.nfdi-jupyter.de/). 

1. Choose "Guest access" as your home institution.

![](images/jup4nfdi_1.png)

2. **If you are working at Leipzig University**, do **NOT** login via your employer (this doesn't work due to the IT outage). Choose "Github", "ORCID" or "Google" instead.

![](images/jup4nfdi_2.png)

3. Read policies and accept them.
4. Configure your JupyterLab and click on `Start`

![](images/jup4nfdi_3.png)

5. Wait about 2 minutes.
6. When JupyterLab opens, create a new notebook.

![](images/jup4nfdi_4.png)

In the new notebook, execute this code to install python libraries:
```
pip install bia-bob numpy scipy pandas scikit-learn scikit-image seaborn cellpose stackview
```

![](images/jup4nfdi_5.png)

7. Wait about 10 minutes.
8. Do **NOT** continue working in this notebook.
10. Close the notebook.
11. Reload the page in the browser.

## Testing the installation

11. Start a new notebook.
12. Enter this code and see if graphical user interface with the slider appears:

```
import stackview
import numpy as np

image = np.random.random((10,100,100))

stackview.slice(image)
```

![](images/jup4nfdi_6.png)

13. Start a new notebook.
14. Enter the following code. When asked, paste your Blablador API key and hit ENTER.

```
from bia_bob import config_blablador, bob

config_blablador()
```

![](images/jup4nfdi_7.png)

Afterwards, try to communicate with `%%bob` like this:

```
%%bob
Print hello world
```

If `%%bob` answers with a reasonable code-snippet, your installation was successful. 

![](images/jup4nfdi_8.png)

