
wr=open('H:\aug.txt','w')


aug= [38,36,31,27,38,24,29,29,30,24,33,27,32,24,36,31,41,30,26,34,26,30,31,26,36,23,31,28,31,32,28]

wr.write(f'aug= [38,36,31,27,38,24,29,29,30,24,33,27,32,24,36,31,41,30,26,34,26,30,31,26,36,23,31,28,31,32,28]\n')

augu = False
napok=len(aug)
if napok == 31:
   augu = True
   print(f'Ez egy hónap adata')
   wr.write(f'Ez egy hónap adata.\n')
else:
    print(f'Ez nem egy hónap adata')
    wr.write(f'Ez nem egy hónap adata.\n')

Legnagyobb=aug[0]
Legkisebb=aug[0]
számláló=0
for x in aug:
    if x > Legnagyobb:
        Legnagyobb =x
    elif x < Legkisebb:
        Legkisebb = x  
    if x > 31:
        számláló +=1

print(f'Legnagyobb: {Legnagyobb}')
wr.write(f'Legnagyobb: {Legnagyobb}.\n')
print(f'Legkisebb: {Legkisebb}')
wr.write(f'Legkisebb: {Legkisebb}.\n')

Legnagyobb1=max(aug)
Legkisebb1=min(aug)

print(f'Legnagyobb: {Legnagyobb1}')
print(f'Legkisebb:{Legkisebb1}')

print(f'Ennyiszer volt a C° magassab mint 31: {számláló}')
wr.write(f'Ennyiszer volt a C° magassab mint 31: {számláló}.\n')

n = len(aug)
ker = 34
 
i = 0
while i < n and aug[i] != ker:
    i = i + 1
 
if(i < n):
    print(f'Augusztus 20-án {ker} °C volt.')
    wr.write(f'Augusztus 20-án {ker} °C volt.\n')
    
összeg = 0
for num in aug:
    összeg = összeg + num
 
print(f'Augusztus átlag hőmérséklete: {összeg/napok:2.0f}')
wr.write(f'Augusztus átlag hőmérséklete: {összeg/napok:2.0f}.\n')

hőingadozás=Legnagyobb-Legkisebb
print(f"A hőingadozás ekkora volt {hőingadozás}.")
wr.write(f"A hőingadozás ekkora volt {hőingadozás}.\n")


wr.close()
# Lehet e augusztus havi hóméséklet
# A legnagyobb hóméséklet
# A legkisebb hóméséklet
# Hány alkalommal volt a hőmeséklet 31 fok felett?
# mekkora volt a hómérséklet augusztus 20.-án?
# mekkora volt az átlag hőmérséklet?
# mekkora volt a hőingadoszás?
# Fájl írás