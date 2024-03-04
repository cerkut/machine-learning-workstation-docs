# Main page

This space contains guides and other resources related to the ML workstation at the Copenhagen campus. 

The preferred way of getting managed GPU access at AAU is through [CLAAUDIA](https://www.researcher.aau.dk/contact/claaudia). For selected projects, you may be granted access to the local workstation with your {AAU_EMAIL_USERNAME}, which is the part of your AAU MAIL before the @ sign (mine is cer).

Then **on the campus** you can access to the jupyter server with 

`ssh -NfL localhost:4098:localhost:80 cer@172.30.207.25`

and opening a browser with the following address: http://localhost:4098/user/cer/lab 

Remember to use your {AAU_EMAIL_USERNAME} instead of `cer` above. The first time you'll connect, you'll have to give a password of your choice. If you want to access to the server outside of the campus, you will have to setup a [VPN](https://aalborg-university.gitbook.io/machine-learning-workstation/connection/connection-through-vpn) or [ssh with AAU two factor authorization](https://aalborg-university.gitbook.io/machine-learning-workstation/connection/connect-to-the-machine).

The following sections will guide you through connecting to the machine, using the GPUs, and exchange data. Moreover, a list of useful links is provided, including [CLAAUDIA](https://www.researcher.aau.dk/contact/claaudia) GPU acccess. You will find a cuda-enabled conda installation at the hub, but can install your preferred custom packages with 

`pip install --user scikit-learn`

For any question about the platform, please contact [Cumhur Erkut](mailto:cer@create.aau.dk). For questions, suggestions, and corrections related to the content of this documentation, refer to [this page](https://github.com/miccio-dk/machine-learning-workstation-docs/issues).

