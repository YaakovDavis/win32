---
Description: Create a signed certificate trust list (CTL) and save it to a certificate store.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Creating, Signing, and Storing a CTL
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Creating, Signing, and Storing a CTL

The following procedures create a signed [*certificate trust list*](https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb) (CTL) and save it to a [*certificate store*](https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb).

**To create and sign a CTL**

1.  Create an array of items to be stored in the [*CTL*](https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb). In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.
2.  Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-_ctl_info) structure that includes the array of items just created.
3.  Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-_cmsg_signed_encode_info) structure.
4.  Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.

**To add a CTL to a certificate store**

1.  Get a pointer to a signed and encoded CTL.
2.  Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 


