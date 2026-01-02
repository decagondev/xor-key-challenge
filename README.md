# XOR Cipher Challenge: Recover the Hidden Answer

## Problem Statement

I've taken the answer to a famous trivia question and encrypted it using a classic **single-byte XOR cipher**. That means every byte of the original plaintext message was XORed with the same repeating key byte (a value between 0 and 255).

Your task is to recover the original plaintext message by brute-forcing all possible keys. The correct plaintext will be a short, readable English string that **directly answers** the question below.

### The Question

> **What is the name of the famous painting by Leonardo da Vinci that depicts a woman with a mysterious smile?**

### Ciphertext (hex)
```1d011d0f03410a171d4a0d17001d031d1d021d031d4a0e111d171d031d```


## Your Task

1. Convert the hex string into bytes.
2. Brute-force all possible keys from `0` to `255`.
3. For each key, decrypt the ciphertext by XORing every byte with the key.
4. Decode the result as ASCII text.
5. Find the one key that produces valid, readable English text (all lowercase letters and a space).
6. Submit **both**:
   - The decrypted plaintext (the name of the painting)
   - The key (as a decimal number **and** in hex, e.g., `79` or `0x4f`)

**The final answer / flag is the key value used to decrypt the message.**

The correct plaintext will be immediately obvious — it's short, meaningful, and directly answers the question.

## Rules & Hints

- Plaintext is only lowercase letters and one space.
- Length: 9 characters (including the space).
- Only one key will produce proper English text.
- Brute-forcing 256 possibilities is instant.
- You can solve it in any language or even manually.

## Resources
[XOR](https://en.wikipedia.org/wiki/XOR_gate)
