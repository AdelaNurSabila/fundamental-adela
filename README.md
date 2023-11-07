function excelColumnTitleToNumber(judulKolom) {
    var hasil = 0;
    
    for (var i = 0; i < judulKolom.length; i++) {
      var karakter = judulKolom[i];
      var nilaiKarakter = karakter.charCodeAt(0) - 64;
      hasil = hasil * 26 + nilaiKarakter;
    }
    
    return hasil;
  }
  
  // Contoh penggunaan: //
  var nomorKolom = excelColumnTitleToNumber("AB");
  console.log(nomorKolom); // Output: 28//
  

  /*kak maaf ga ngerti ini pake chatgpt :( 
     bingungnya di for (var i = 0; i < judulKolom.length; i++) 
     kenapa tetep pake i++? 
     terus kenapa charCodeAt(0) - 64 */





/*Given a non-empty array of integers nums, every element appears twice except for one. Find that
single one.
● Example 1:
○ Input: nums = [2,2,1]
○ Output: 1
● Example 2:
○ Input: nums = [4,1,2,1,2]
○ Output: 4
● Example 3:
○ Input: nums = [1]
○ Output: 1 */


function cariAngkaTunggal(nums) {
    let hasilXOR = 0;
  
    for (let angka of nums) {
      hasilXOR ^= angka;
    }
  
    return hasilXOR;
  }
  
  // Contoh penggunaan:
  const nums1 = [2, 2, 1];
  console.log(cariAngkaTunggal(nums1)); // Output: 1
  
  const nums2 = [4, 1, 2, 1, 2];
  console.log(cariAngkaTunggal(nums2)); // Output: 4
  
  const nums3 = [1];
  console.log(cariAngkaTunggal(nums3)); // Output: 1


  //lumayan ngerti, masih pake chatgpt, karna saya kira pake random number haha //






  /* Given two strings s and t, return true if t is an anagram of s, and false otherwise.*/

  // fuction kedua string 
 function anagram(s,t) {

    // jika panjang string t tidak sama dengan string s maka false 
   
    if (s.length !== t.length){
        return false ;
    }

    // Sort the characters in both strings and compare them. (masih kurang ngerti)
  const sortedS = s.split('').sort().join('');
  const sortedT = t.split('').sort().join('');

  return sortedS === sortedT;
}

// Example usage:
console.log(anagram("anagram", "nagaram")); // Output: true
console.log(anagram("rat", "car")); // Output: false


function climbStairs(n) {
    // Base cases for n = 1 and n = 2
    if (n === 1) {
      return 1; // Only one way to climb 1 step (1 step at a time).
    }
    if (n === 2) {
      return 2; // Two ways to climb 2 steps (1 step + 1 step or 2 steps at once).
    }
    
    // For n > 2, the number of ways to climb to the top is the sum of ways for (n-1) and (n-2).
    return climbStairs(n - 1) + climbStairs(n - 2);
  }
  
  // Example usage:
  console.log(climbStairs(2)); // Output: 2
  console.log(climbStairs(5)); // Output: 8
  
  
