# HASHING PYTHON

## Basic Hashing

```python
import hashlib
import os

password = '1234!3#'
salt = os.urandom(32)
hashed_password = hashlib.pbkdf2_hmac('sha256', password.encode('utf-8'), salt, 100000)

```

## Hashing Algorithms

### MD 5

```python
import hashlib

# Create a hash object using MD5 algorithm
hash_object = hashlib.md5()

# Update the hash object with a message
hash_object.update(b"Hello, world!")

# Get the hexadecimal digest of the hash
hex_dig = hash_object.hexdigest()

print(hex_dig)

```

### SHA-256

```python
import hashlib

# Create a hash object using SHA-256 algorithm
hash_object = hashlib.sha256()

# Update the hash object with a message
hash_object.update(b"Hello, world!")

# Get the hexadecimal digest of the hash
hex_dig = hash_object.hexdigest()

print(hex_dig)

```

## Python hashing Technologies

```python
import scrypt
import os

# Generar una salt aleatoria
# 16 bytes es una longitud común para la sal
salt = os.urandom(16)  

# Hash de la contraseña
password = b"password1234#$"
hashed_password = scrypt.hash(password, salt)

# Verificar la contraseña 
password_to_verify = b"password1234#$"
if scrypt.hash(password_to_verify, salt) == hashed_password:
    print("Password is correct")
else:
    print("Invalid password")


```

```python
import bcrypt

# Hash a password
password = b"password1234#$"  
salt = bcrypt.gensalt()
hashed_password = bcrypt.hashpw(password, salt)

# Verify a password
password_to_verify = b"password1234#$"
if bcrypt.checkpw(password_to_verify, hashed_password):
    print("Password is correct")
else:
    print("Invalid password")

```












