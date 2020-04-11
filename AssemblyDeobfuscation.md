### 1. Get working:
 https://github.com/0xd4d/dnSpy - to decode c# code for .dll's and .exe's written in c# and not secured properly  
 https://github.com/0xd4d/de4dot - deobfuscate well known obfuscators and some unknown ones also using special regex etc.  
### 2. lets start with Assembly
 we open Assembly-CSharp.dll in dnSpy  
 click File >> Save Module  
 in popup window change Filename to diffrent one i preffer to use Assembly-CSharpS.dll (where S stays for saved)  
 then we go t oMD Writer Options  
 in `Preserve Heap Offsets` and `Create Heap Even If Empty` select (tick) all options there  
 after setting the above just click `OK`  
### 3. Finding string reversal Token for de4dot
 Open Assembly-CSharpS.dll in dnSpy  
 then we opening that trees untill we see namespace `-` we open that as well and choose `ActionTrigger`  
 at the bottom part of that class we gonna see some encoded strings like `\uE864.\uE000(58172)`  
 we click on `\uE000` it moves us to function used to decode strings from CurrentDomain above that there is a commentary line where you can see Token for me its looking like: ```// Token: 0x0600B6FA RID: 46842 RVA: 0x001127BF File Offset: 0x001109BF``` we are focusing on the Token side we deleting 0x from that so we copying only `0600B6FA` part (its our delegate Token)  
### 4. After we found that key we open CMD in folder where we have de4dot
 use this in cmd to deobfuscate replacing {filePath} and {token} with proper staff  
```
de4dot.exe --un-name "!^<>[a-z0-9]$&!^<>[a-z0-9]__.*$&!^<.[a-zA-Z0-9]{1,}>[a-z0-9]__.*$&![A-Z][A-Z]\$<>[0-9]__[a-zA-Z0-9]{1,}$&^[a-zA-Z_<{$][a-zA-Z_0-9<>{}$.`-]*$" "{filePath}\Assembly-CSharpS.dll" --strtyp delegate --strtok {token}
```
**{filePath}** - is path to saved file  
**{token}** - is token we get in point 3.  
after pressing Enter it should deobfuscate whole assembly with abitily to edit almost everything   
