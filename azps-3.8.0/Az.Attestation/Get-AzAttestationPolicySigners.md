---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicysigners
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicySigners.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicySigners.md
ms.openlocfilehash: 3553f59b75f16913a5147ed3c197853336ee1d82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958679"
---
# <span data-ttu-id="0ca05-101">Get-AzAttestationPolicySigners</span><span class="sxs-lookup"><span data-stu-id="0ca05-101">Get-AzAttestationPolicySigners</span></span>

## <span data-ttu-id="0ca05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ca05-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca05-103">從 Azure 證明中的租使用者取得受信任的原則簽名者。</span><span class="sxs-lookup"><span data-stu-id="0ca05-103">Gets the trusted policy signers from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0ca05-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ca05-104">SYNTAX</span></span>

### <span data-ttu-id="0ca05-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca05-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ca05-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca05-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca05-107">說明</span><span class="sxs-lookup"><span data-stu-id="0ca05-107">DESCRIPTION</span></span>
<span data-ttu-id="0ca05-108">Get-AzAttestationPolicySigners Cmdlet 會從 Azure 證明中的租使用者取得受信任的原則簽名者。</span><span class="sxs-lookup"><span data-stu-id="0ca05-108">The Get-AzAttestationPolicySigners cmdlet gets the trusted policy signers from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0ca05-109">示例</span><span class="sxs-lookup"><span data-stu-id="0ca05-109">EXAMPLES</span></span>

### <span data-ttu-id="0ca05-110">範例1</span><span class="sxs-lookup"><span data-stu-id="0ca05-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                          
CertificateCount : 0
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vcHNodGVzdC51cy5hdHRlc3QuYXp1cmUubmV0L2NlcnRzIiwgImtpZCI6ICJrdlB4aUJlemk4RGJsQVY0WE5nNG5wVjlocE5WTnRqS0NQTlZZUjRuRVJzPSIsICJ0eXAiOiAiSldUIn0.eyJhYXMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW119LCAiZXhwIjogMTU4NDM5NDgxOSwgImlhdCI6IDE1ODQzOTEyMTksICJpc3MiOiAiaHR0cHM6Ly9wc2h0ZXN0LnVzLmF0dGVzdC5henVyZS5uZXQiLCAibmJmIjogMTU4NDM5MTIxOX0.hXDejUE2Tfbnvy0RN4ONyxtg2NTEmHKz7wOJIY2YhF43MUJQYgh7TREE3BAMl93mQIO9px2HNvo_MSzNhDRmCMvZt6tUdC8Gw1xK40w2nqngvfmTONOcKskSXUVc1Igk2C47cuCQjB1W8t2qdCrwpR4UTEGdidyGlb7NFkAaFMOK119H1c0DQ7LSpY0bqodrVDW1DNa0LOFLxL3DwxqkRF-itk
duZJn9aqlkrgIPPSE_kdNUUURjpx3F6eCEONsdtu8zfj76v7Yb6Oyf70rh8EOyVdEu2wwmfg9ASZnooANwo7C6o68ESpfvi6DHPTyBsD0rgysVsNYtkS0tuXNj3A
Algorithm        : RS256
JKU              : https://pshtest.us.attest.azure.net/certs
Certificates     : {}
```

<span data-ttu-id="0ca05-111">針對資源群組 *psh-test-rg* 中的認證提供者 *pshtest* ，取得受信任的原則簽名者。</span><span class="sxs-lookup"><span data-stu-id="0ca05-111">Gets the trusted policy signers for the Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>  <span data-ttu-id="0ca05-112">請注意，此認證提供者沒有受信任的簽署人。</span><span class="sxs-lookup"><span data-stu-id="0ca05-112">Note that there are no trusted signers for this Attestation Provider.</span></span>

### <span data-ttu-id="0ca05-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0ca05-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -Name pshtest2 -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                         
CertificateCount : 1
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vcHNodGVzdDIudXMuYXR0ZXN0LmF6dXJlLm5ldC9jZXJ0cyIsICJraWQiOiAiL09KMXJ0U0hkbFJnR1VqMGVuTEl5bDhLeHQ3NHZYdmJLTW9VbmFZMlNJRT0iLCAidHlwIjogIkpXVCJ9.eyJhYXMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW3siYWxnIjogIlJTMjU2IiwgImt0eSI6ICJSU0EiLCAidXNlIjogInNpZyIsICJ4NWMiOiBbIk1JSURMRENDQWhTZ0F3SUJBZ0lJYStGTE1oT1ZkMFF3RFFZSktvWklodmNOQVFFTEJRQXdGekVWTUJNR0ExVUVBd3dNVFdGaFZHVnpkRU5sY25ReE1DQVhEVEl3TURNd016QXdNREF3TUZvWUR6SXdOekF3TXpBek1EQXdNREF3V2pBWE1SVXdFd1lEVlFRRERBeE5ZV0ZVWlhOMFEyVnlkREV3Z2dFaU1BMEdDU3FHU0liM0RRRUJBUVVBQTRJQkR3QXdnZ0VLQW9JQkFRQ3BidzRLeHJhME05OE9RNUMzQkk3Uk9BS2k4dnlRNTF5eWJoUi9saTJDd1Y4WkVJZmVZSEJMMFM5UC9naVQ2VTlZRkNtNEw3c2hGTm5kYTBJcG5zeTZSaFhCUnRYampZdVR1SlcxTk01SVh0OVFJMEtkUUNQbG5VVlNnb2UzdW9pQ0l6S25HU1Nka0MrU25nblVveDFsVnVRNEpLSmtLUXBubTFCekgzTGNzUEFnQUJwYTloVnlieG9XUHU4c2tEek1TSVFZVzMxemVYVkxZdlprZmxoTWttNFZLby9DUWpYNXJWTFNXeVZWa1YrOUhDQjlVQk1HMExiNmhldWZTQTVKTE5mR2taY0kwNHBHRmFqVzZnVUJkcmJnM2R4V0s5VzdKUVZYT05maEJ6NkE2bWM1a0wxRUtLNWhIc2dnekdYeEdLWmhwWU5JSDNiek52eTNrUUFQQWdNQkFBR2plakI0TUVZR0ExVWRJd1EvTUQyQUZIWnBTaFI4UUlRMGFzZy9Yb1NwR2hNOURGN25vUnVrR1RBWE1SVXdFd1lEVlFRRERBeE5ZV0ZVWlhOMFEyVnlkREdDQ0d2aFN6SVRsWGRFTUIwR0ExVWREZ1FXQkJSMmFVb1VmRUNFTkdySVAxNkVxUm9UUFF4ZTV6QVBCZ05WSFJNQkFmOEVCVEFEQVFIL01BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRQVFpWXpFeUtVbDlkSWVUVGZnTVpBWEo0V0NFZXpFN2FRcHd2QnU5Rkk0MXN4L1pzbEV2RVFvTDVWNTZTQVhQZCtTOWdlZnVJNjFuZ056OTl5RTlrZGgrOWxmVTJVTU1tdXFCdVFWaWI5RzBKakllYVNHM1J2OGVyRXNGMUUrbXhjbzRtVGVEdUdLUklmN1dHNnNYZjZ5b2N1U0FVaEV2emM5NzZTSUNJLzQxclZEVkg5bnFJdS9LUnZleHpWcFJqZ1EzWlVnMTMydmVnb2djNjc1UndreTJHckxrZDBJN015bGcwZVIyamd1ZndLcTVBbnZ1YTlzRFJyUUpLUCtqclpmcWpiOEpoZ2VsUEtLVXl4S1JIS1Z6QUxzQ3JHTkRQS0ozVDlsWUhmZmFuWE9JeEpnTDExcDNBMmVMUWtWN3BMdEpUenhrb1lDZFZKdTNmbDZJNWVsIl19XX0sICJleHAiOiAxNTg0Mzk1MTE5LCAiaWF0IjogMTU4NDM5MTUxOSwgImlzcyI6ICJodHRwczovL3BzaHRlc3QyLnVzLmF0dGVzdC5henVyZS5uZXQiLCAibmJmIjogMTU4NDM5MTUxOX0Irkd3eNG7jD-fJThxBKURjjSlsfbRgOnOvN_nI8ukH-VvpaYIKGgk74iuefWhPYQJr--mAUT2IaEqcBGXvRV6K4oDUXUHn7iCNL1aIWzQ4udTrFVChNTUjEH4x1tmyDLC04SBeoi_yP5R0Bfijb51qnKwSU6ppuKTTletpzFztib2MN_RUQidHjuaeivMECJPRu5Bit2DbLRObokMRRY-rftcxPf7rLr1mK_4WUbRjIKT_ic03qWcqY0lakwC3MdFV9xQsvCH7-sizgJShSIOIS9pHrRp6YIEyG8LoF6Kj9aL-imNTUZ2IjwxtDJOmnhXh56pYjzQNpW_bzQlOeNaA
Algorithm        : RS256
JKU              : https://pshtest2.us.attest.azure.net/certs
Certificates     : {{
                     "alg": "RS256",
                     "kty": "RSA",
                     "use": "sig",
                     "x5c": ["MIIDLDCCAhSgAwIBAgIIa+FLMhOVd0QwDQYJKoZIhvcNAQELBQAwFzEVMBMGA1UEAwwMTWFhVGVzdENlcnQxMCAXDTIwMDMwMzAwMDAwMFoYDzIwNzAwMzAzMDAwMDAwWjAXMRUwEwYDVQQDDAxNYWFUZXN0Q2VydDEwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCpbw4Kxra0M98OQ5C3BI7ROAKi8vyQ51yybhR/li2CwV8ZEIfeYHBL0S9P/giT6U9YFCm4L7shFNnda0Ipnsy6RhXBRtXjjYuTuJW1NM5IXt9QI0KdQCPlnUVSgoe3uoiCIzKnGSSdkC+SngnUox1lVuQ4JKJkKQpnm1BzH3LcsPAgABpa9hVybxoWPu8skDzMSIQYW31zeXVLYvZkflhMkm4VKo/CQjX5rVLSWyVVkV+9HCB9UBMG0Lb6heufSA5JLNfGkZcI04pGFajW6gUBdrbg3dxWK9W7JQVXONfhBz6A6mc5kL1EKK5hHsggzGXxGKZhpYNIH3bzNvy3kQAPAgMBAAGjejB4MEYGA1UdIwQ/MD2AFHZpShR8QIQ0asg/XoSpGhM9DF7noRukGTAXMRUwEwYDVQQDDAxNYWFUZXN0Q2VydDGCCGvhSzITlXdEMB0GA1UdDgQWBBR2aUoUfECENGrIP16EqRoTPQxe5zAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3DQEBCwUAA4IBAQAQiYzEyKUl9dIeTTfgMZAXJ4WCEezE7aQpwvBu9FI41sx/ZslEvEQoL5V56SAXPd+S9gefuI61ngNz99yE9kdh+9lfU2UMMmuqBuQVib9G0JjIeaSG3Rv8erEsF1E+mxco4mTeDuGKRIf7WG6sXf6yocuSAUhEvzc976SICI/41rVDVH9nqIu/KRvexzVpRjgQ3ZUg132vegogc675Rwky2GrLkd0I7Mylg0eR2jgufwKq5Anvua9sDRrQJKP+jrZfqjb8JhgelPKKUyxKRHKVzALsCrGNDPKJ3T9lYHffanXOIxJgL11p3A2eLQkV7pLtJTzxkoYCdVJu3fl6I5el"]
                   }}
```

<span data-ttu-id="0ca05-114">針對資源群組 *psh-test-rg* 中的認證提供者 *pshtest2* ，取得受信任的原則簽名者。</span><span class="sxs-lookup"><span data-stu-id="0ca05-114">Gets the trusted policy signers for the Attestation Provider *pshtest2* in Resource Group *psh-test-rg*.</span></span>  <span data-ttu-id="0ca05-115">請注意，此認證提供者只有一個受信任的簽章者。</span><span class="sxs-lookup"><span data-stu-id="0ca05-115">Note that there is one trusted signer for this Attestation Provider.</span></span>

## <span data-ttu-id="0ca05-116">參數</span><span class="sxs-lookup"><span data-stu-id="0ca05-116">PARAMETERS</span></span>

### <span data-ttu-id="0ca05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca05-117">-DefaultProfile</span></span>
<span data-ttu-id="0ca05-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ca05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca05-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ca05-119">-Name</span></span>
<span data-ttu-id="0ca05-120">指定認證提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ca05-120">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca05-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca05-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ca05-122">指定證明提供者的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0ca05-122">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca05-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca05-123">-ResourceId</span></span>
<span data-ttu-id="0ca05-124">指定證明提供者的 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="0ca05-124">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca05-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca05-125">CommonParameters</span></span>
<span data-ttu-id="0ca05-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ca05-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca05-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0ca05-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca05-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0ca05-128">INPUTS</span></span>

### <span data-ttu-id="0ca05-129">System.object</span><span class="sxs-lookup"><span data-stu-id="0ca05-129">System.String</span></span>

## <span data-ttu-id="0ca05-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0ca05-130">OUTPUTS</span></span>

### <span data-ttu-id="0ca05-131">PSPolicySigners 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0ca05-131">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="0ca05-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0ca05-132">NOTES</span></span>

## <span data-ttu-id="0ca05-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ca05-133">RELATED LINKS</span></span>