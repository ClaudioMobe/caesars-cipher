# Cifrado César
Esta función de JavaScript cifra y descifra el Cifrado César, en el cual las letras se desplazan 13 lugares en el abecedario. Por ejemplo, A&lt;->N
    
    function rot13(str) {
    const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'; 
    let decrypted= ''
    for (let i=0; i<str.length; i++){
      let indexOfThisLetter= alphabet.indexOf(str[i]);
      if(indexOfThisLetter === -1){
        decrypted= decrypted + str[i]
      }else if (indexOfThisLetter<26-13){
        decrypted= decrypted + alphabet[indexOfThisLetter+13];
      } else {
        decrypted= decrypted + alphabet[indexOfThisLetter-13];
      }
    }
    return decrypted;
    }

      rot13("SERR PBQR PNZC"); //FREE CODE CAMP
      rot13("SERR CVMMN!"); //FREE PIZZA!
      rot13("SERR YBIR?"); //FREE LOVE?
      rot13("GUR DHVPX OEBJA SBK WHZCF BIRE GUR YNML QBT."); //THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG.
