# bitcoin_demo
  A bitcoin block chain demo with Golang, contains full base function, eg : mining, transaction, wallet(privake key, public key, address), signature, verify and so on.
  
# Useage
  1. Generate key pair
  2. Create block chain
  3. Send transaction
  4. Get balance
  5. Print blocks or transaction
  
 For example: 
 
      api := API{}
      api.GenKeyPair()
      api.GenKeyPair()
      api.GenKeyPair()
      api.GenKeyPair()
      addrList := api.listAddress()
      addr1 := addrList[0]
      addr2 := addrList[1]
      addr3 := addrList[2]
      addr4 := addrList[3]
      api.createBlockChain(addr1)
      fmt.Println("send----------------------")

      api.send(addr1, addr2, 10, addr1)
      api.send(addr1, addr3, 10, addr1)
      api.send(addr1, addr4, 10, addr1)

      api.send(addr2, addr3, 1, addr1)
      api.send(addr2, addr4, 1, addr1)
      api.send(addr3, addr4, 1, addr1)

      fmt.Println("getbalance ----------------------")
      api.getBalance(addr1)
      api.getBalance(addr2)
      api.getBalance(addr3)
      api.getBalance(addr4)

      fmt.Println("printAllBlocks blocks----------------------")
      api.printAllBlocks()

      fmt.Println("printAllBlocks tx ----------------------")
      api.printTx()
      fmt.Println("over")
