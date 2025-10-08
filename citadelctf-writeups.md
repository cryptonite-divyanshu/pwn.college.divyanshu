## 1. Zahard's Welcome

Got from the rules tab in discord

## 2. The Robot's Trail

USED inspect element to get the text file initially and then traversed through the files to get the flag

## 3. Coco Conjecture

Ran python script to solve

## 4. schlagenheim

Changed value of first 4 bits using hex edit to change their value to convert into midi file and viewed with compatible software

## 5. XOR Slide 

Deciphered the XOR encryption

## 6. The Sound of Music

Found flag parts on below links 

'''
https://rateyourmusic.com/~citadweller
https://www.last.fm/user/citadweller
https://open.spotify.com/playlist/37eiwS3xaRXOsg4F5RmSsY
'''

## 7. Echoes and Pings 

Saw the pcap file data to find the image part and extracted it to get the picture

## 8. The Ripper 

Found it was bcrypt hash from $2a$ at the start. Used john --format=bcrypt hash.txt --wordlist=wordlist.txt to crack encryption.

## 9. AetherCorp NetprobeX

USED prompt injection

8.8.8.8%0Afind / -name 'key' 2>/dev/null
8.8.8.8%0Aless /var/lib/aethercorp/archive/.secrets/blacksite_key.

## 10. BRATCHA 

Tried various combinations to get this
https://pastebin.com/sqxnxBhZ

## 11. A Memory's a Heavy Burden 

Google reverse img search
