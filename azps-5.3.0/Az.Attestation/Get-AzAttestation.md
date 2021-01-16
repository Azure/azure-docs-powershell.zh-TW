---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287491"
---
# <span data-ttu-id="652c1-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="652c1-101">Get-AzAttestation</span></span>

## <span data-ttu-id="652c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="652c1-102">SYNOPSIS</span></span>
<span data-ttu-id="652c1-103">取得證明。</span><span class="sxs-lookup"><span data-stu-id="652c1-103">Gets an attestation.</span></span>

## <span data-ttu-id="652c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="652c1-104">SYNTAX</span></span>

### <span data-ttu-id="652c1-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="652c1-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="652c1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="652c1-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="652c1-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="652c1-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="652c1-108">說明</span><span class="sxs-lookup"><span data-stu-id="652c1-108">DESCRIPTION</span></span>
<span data-ttu-id="652c1-109">Get-AzAttestation Cmdlet 會取得訂閱中認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="652c1-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="652c1-110">示例</span><span class="sxs-lookup"><span data-stu-id="652c1-110">EXAMPLES</span></span>

### <span data-ttu-id="652c1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="652c1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="652c1-112">在資源群組 *psh-test-rg* 中取得認證提供者 *pshtest* 。</span><span class="sxs-lookup"><span data-stu-id="652c1-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="652c1-113">範例2</span><span class="sxs-lookup"><span data-stu-id="652c1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="652c1-114">取得所有可用的證明預設提供者</span><span class="sxs-lookup"><span data-stu-id="652c1-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="652c1-115">範例3</span><span class="sxs-lookup"><span data-stu-id="652c1-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="652c1-116">從 *美國地區 2* 取得證明預設提供者</span><span class="sxs-lookup"><span data-stu-id="652c1-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="652c1-117">參數</span><span class="sxs-lookup"><span data-stu-id="652c1-117">PARAMETERS</span></span>

### <span data-ttu-id="652c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652c1-118">-DefaultProfile</span></span>
<span data-ttu-id="652c1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="652c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="652c1-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="652c1-120">-DefaultProvider</span></span>
<span data-ttu-id="652c1-121">指定這是預設認證提供者的要求。</span><span class="sxs-lookup"><span data-stu-id="652c1-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="652c1-122">-位置</span><span class="sxs-lookup"><span data-stu-id="652c1-122">-Location</span></span>
<span data-ttu-id="652c1-123">指定預設認證提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="652c1-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="652c1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="652c1-124">-Name</span></span>
<span data-ttu-id="652c1-125">認證名稱。</span><span class="sxs-lookup"><span data-stu-id="652c1-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="652c1-127">指定與所查詢之證明相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="652c1-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652c1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="652c1-128">-ResourceId</span></span>
<span data-ttu-id="652c1-129">指定與所查詢之證明相關聯的 ResourceID 的名稱</span><span class="sxs-lookup"><span data-stu-id="652c1-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="652c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652c1-130">CommonParameters</span></span>
<span data-ttu-id="652c1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="652c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652c1-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="652c1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652c1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="652c1-133">INPUTS</span></span>

### <span data-ttu-id="652c1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="652c1-134">System.String</span></span>

## <span data-ttu-id="652c1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="652c1-135">OUTPUTS</span></span>

### <span data-ttu-id="652c1-136">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="652c1-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="652c1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="652c1-137">NOTES</span></span>

## <span data-ttu-id="652c1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="652c1-138">RELATED LINKS</span></span>
