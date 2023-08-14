# ----------------
# LOCAL RULES
# ----------------
# This file intentionally does not come with signatures.  Put your local
# additions here.
# alert tcp any any <> any 21 (msg:"FTP detected";content:"cannot log in";sid:1000001;rev:1)
# alert tcp any 21 <> any any (msg:"FTP detected";content:"cannot log in";sid:1000002;rev:2)
alert tcp any any <> any 21 (msg:"FTP detected";sid:1000001;rev:1)
alert tcp any 21 <> any any (msg:"FTP detected";sid:1000002;rev:2)
