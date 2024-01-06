# rock-paper-scissors-shoot

```
import random

def validate(your_hand):
  if your_hand < 0 or your_hand > 2:
    return False
  return True

def pick_hand(your_hand, your_name):
  hands = ['Batu', 'Gunting', 'Kertas']
  print(your_name + ' memilih: ' + hands[your_hand])

def judge(player, computer):
    if player == computer:
        return 'Permainan ini seri'
    elif player == 0 and computer == 1:
        return 'Kamu kalah'
    elif player == 1 and computer == 2:
        return 'Kamu kalah'    
    elif player == 2 and computer == 0:
        return 'Kamu kalah'
    else:
        return 'Selamat! Kamu menang' 

print('Yuk, kita mulai main!') 
player_name = input('Masukan nama kamu: ') 

print('Sekarang, pilih tangan: (0: Batu, 1: Kertas, 2: Gunting)')
player_hand = int(input('Pilih nomor 0 - 2: '))

if validate(player_hand):
    computer_hand = random.randint(0,2)
    
    pick_hand(player_hand, player_name)
    pick_hand(computer_hand, 'Komputer')
    
    # Tetapkan nilai return dari judge ke variable result 
    result = judge(player_hand, computer_hand)
    # Cetak variable result 
    print('Hasil: ' + result)
else:
    print('Oops, nomor yang kamu masukan salah!') 
    print('Silahkan mulai lagi dan masukan nomor yang benar!')
```
