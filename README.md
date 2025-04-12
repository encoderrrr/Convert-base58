```sudo apt update```
```sudo apt install python3```


#With this command, we obtain the private key and save it. In the next command, you need to replace it

```cat /root/.config/solana/id.json```


**nano convert_key.py**

#Copy and paste the full text.

import base58

# The private key array should be placed here []
key_bytes = []  # Empty array - the user must insert their own array

key_bytes = bytes(key_bytes[:64])  # Only the first 64 bytes for the private key

private_key = base58.b58encode(key_bytes).decode('utf-8')
print("Private Key (Base58):", private_key)



#Creating a virtual environment.

```python3 -m venv ~/base58_env```

#Activating the virtual environment

```source ~/base58_env/bin/activate```


#Installing Base58 in the virtual environment

***pip install base58***
