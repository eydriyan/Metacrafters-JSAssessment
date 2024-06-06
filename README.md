# NFT Collection Project

This project demonstrates a simple implementation of a Non-Fungible Token (NFT) minting system using JavaScript. It allows for minting NFTs with specific metadata, listing all minted NFTs, and getting the total number of minted NFTs.

Features
- Minting NFTs: Create NFTs with custom metadata including name, eye color, shirt type, and bling.
- Listing NFTs: Display the metadata of all minted NFTs.
- Total Supply: Retrieve the total number of NFTs minted.

Prerequisites
Ensure you have a working environment for running JavaScript.

Code Explanation
1. An array to store the NFT objects.
const NFTs = [];

2. The mintNFT function creates an NFT object with the given metadata and adds it to the NFTs array.
function mintNFT (_name, _eyeColor, _shirtType, _bling) {
    const NFT = {
        "name": _name,
        "eyeColor": _eyeColor,
        "shirtType": _shirtType,
        "bling": _bling
    }
    NFTs.push(NFT);
    console.log("Minted: " + _name);
}

3. The listNFTs function logs the metadata of each NFT stored in the NFTs array.
function listNFTs () {
    for(let i = 0; i < NFTs.length; i++) {
        console.log("\nID: \t\t" + (i + 1))
        console.log("Name: \t\t" + NFTs[i].name);
        console.log("Eye Color: \t" + NFTs[i].eyeColor);
        console.log("Shirt Type: " + NFTs[i].shirtType);
        console.log("Bling: \t\t" + NFTs[i].bling);
    }
}

4. The getTotalSupply function logs the total number of NFTs in the NFTs array.
function getTotalSupply() {
    console.log("\n" + NFTs.length);
}

Example Usage
// Mint some NFTs
mintNFT("Bob", "Blue", "Hoodie", "Gold Chain");
mintNFT("Charlie", "Hazel", "Tank Top", "Platinum Ring");
mintNFT("Dave", "Gray", "Jacket", "Ruby Brooch");
mintNFT("Fay", "Amber", "Blouse", "Emerald Bracelet");

// List all NFTs
listNFTs();

// Get total supply of NFTs
getTotalSupply();
