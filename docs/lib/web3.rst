========================================
Interacting with NeoPlace smart contract
========================================

Instantiate the web3 provider
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Instantiate the web3 provider for the Desktop version (Metamask or Mist) or Mobile version::

    //init web3 provider
    constructor(private transactionWeb3: TransactionWeb3Service) {
      this.transactionWeb3.initDesktop(); // for Desktop version
      this.transactionWeb3.initMobile("[your ethereum private key]", "[rpcUrl]") // for Mobile version
    }

Available methods
~~~~~~~~~~~~~~~~~

::

    this.transactionWeb3.buyItem
                        .send
                        .sendAdditionalFunds
                        .unlockFunds
                        .getPurchases
                        .getSales
                        .getTransaction

Buy an item
~~~~~~~~~~~
::

  this.transactionWeb3.buyItem(
    <your ethereum address>,
    <seller ethereum address>,
    <item_id>,
    <type_item>,
    <shipping_address>,
    <picture_ipfs_hash>,
    <additional_information>,
    <price_in_ETH>).subscribe(value => {
        console.log("transaction hash", value.tx);
    })

Unlock funds
~~~~~~~~~~~~
::

  this.transactionWeb3Service.unlockFunds(
    <item_id>,
    <your_ethereum_address>).subscribe(value => {
    console.log("transaction hash", value.tx);
  }, error => {
    this.loader.close();
  });

Send some eth with the smart contract
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
::

      this.transactionWeb3Service.send(
        <your_ethereum_address>,
        <target_etherum_address>,
        <amount_in_ETH to send>).subscribe(res => {
        console.log("transaction hash", value.tx);
      })