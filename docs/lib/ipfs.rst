=====================
Interacting with IPFS
=====================

Instantiate the IPFS class
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Instantiate the IPFS class::

    constructor(private ipfsService: IpfsService) {}

We use the *Infura* gateway.


Push data to IPFS
~~~~~~~~~~~~~~~~~
Add text data::

    this.ipfsService.addData("your text").then(resp => {
      console.log("ipfs hash: ", resp.hash);
    });

Add a file::

    this.ipfsService.addFile([your file]).then(reader => {
      this.ipfsService.saveToIpfs(reader).then(resp => {
        console.log("ipfs hash: ", resp.hash);
      })
    })