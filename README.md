/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's
const nftCollection = [];
// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function createDigitalAsset(name, description, value, marketplace) {
  const digitalCollectible = {
    name,
    description,
    value,
    marketplace
  };
  nftCollection.push(digitalCollectible);
  console.log(`${digitalCollectible.name} has been successfully minted!`);
}
// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function displayNFTGallery() {
  nftCollection.forEach((nft) => {
    console.log(`
      ***********Digital Collectible**************
      Name: ${nft.name}
      Description: ${nft.description}
      Value: ${nft.value} $
      Marketplace: ${nft.marketplace}
    `);
  });
}
function getNFTInventory() {
  console.log(`Total number of digital collectibles in the gallery: ${nftCollection.length}`);
}
// Mint some NFTs
createDigitalAsset('Proof 1', 'NFT from metacrafters',123, 'Crypto Punks');
createDigitalAsset('Proof 2', 'NFT from metacrafters', 456, 'The Merge ');
createDigitalAsset('Proof 3', 'NFT from metacrafters', 789, 'Art NFTs');
// Display the NFT gallery
displayNFTGallery();
// Get the total number of NFTs in the gallery
getNFTInventory();
