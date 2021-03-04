---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 73e51981dc57c4bc81f530f32b597c619b0bab78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910314"
---
# <span data-ttu-id="fc649-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="fc649-101">Get-AzAttestation</span></span>

## <span data-ttu-id="fc649-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc649-102">SYNOPSIS</span></span>
<span data-ttu-id="fc649-103">獲得證明。</span><span class="sxs-lookup"><span data-stu-id="fc649-103">Gets an attestation.</span></span>

## <span data-ttu-id="fc649-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc649-104">SYNTAX</span></span>

### <span data-ttu-id="fc649-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc649-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc649-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc649-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc649-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc649-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc649-108">描述</span><span class="sxs-lookup"><span data-stu-id="fc649-108">DESCRIPTION</span></span>
<span data-ttu-id="fc649-109">Cmdlet Get-AzAttestation訂閱內容相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fc649-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="fc649-110">例子</span><span class="sxs-lookup"><span data-stu-id="fc649-110">EXAMPLES</span></span>

### <span data-ttu-id="fc649-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="fc649-111">Example 1</span></span>
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

<span data-ttu-id="fc649-112">在 Resource Group *psh-test-rg* 中取得證明提供者 *pshtest。*</span><span class="sxs-lookup"><span data-stu-id="fc649-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="fc649-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="fc649-113">Example 2</span></span>
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

<span data-ttu-id="fc649-114">取得所有可用的證明預設提供者</span><span class="sxs-lookup"><span data-stu-id="fc649-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="fc649-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="fc649-115">Example 3</span></span>
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

<span data-ttu-id="fc649-116">取得美國東部位置 *2* 的認證預設提供者</span><span class="sxs-lookup"><span data-stu-id="fc649-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="fc649-117">參數</span><span class="sxs-lookup"><span data-stu-id="fc649-117">PARAMETERS</span></span>

### <span data-ttu-id="fc649-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc649-118">-DefaultProfile</span></span>
<span data-ttu-id="fc649-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc649-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc649-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="fc649-120">-DefaultProvider</span></span>
<span data-ttu-id="fc649-121">指定這是要求給預設證明提供者。</span><span class="sxs-lookup"><span data-stu-id="fc649-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="fc649-122">-位置</span><span class="sxs-lookup"><span data-stu-id="fc649-122">-Location</span></span>
<span data-ttu-id="fc649-123">指定預設證明提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="fc649-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="fc649-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc649-124">-Name</span></span>
<span data-ttu-id="fc649-125">表示名稱。</span><span class="sxs-lookup"><span data-stu-id="fc649-125">Attestation Name.</span></span>

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

### <span data-ttu-id="fc649-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc649-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc649-127">指定與查詢結果相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fc649-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="fc649-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc649-128">-ResourceId</span></span>
<span data-ttu-id="fc649-129">指定與查詢結果相關聯的 ResourceID 名稱</span><span class="sxs-lookup"><span data-stu-id="fc649-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="fc649-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc649-130">CommonParameters</span></span>
<span data-ttu-id="fc649-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc649-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc649-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc649-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc649-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fc649-133">INPUTS</span></span>

### <span data-ttu-id="fc649-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fc649-134">System.String</span></span>

## <span data-ttu-id="fc649-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fc649-135">OUTPUTS</span></span>

### <span data-ttu-id="fc649-136">Microsoft.Azure.Commands.點出ation.models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="fc649-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="fc649-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fc649-137">NOTES</span></span>

## <span data-ttu-id="fc649-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc649-138">RELATED LINKS</span></span>
