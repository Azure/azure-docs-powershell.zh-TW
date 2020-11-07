---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958682"
---
# <span data-ttu-id="7561a-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="7561a-101">Get-AzAttestation</span></span>

## <span data-ttu-id="7561a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7561a-102">SYNOPSIS</span></span>
<span data-ttu-id="7561a-103">取得證明。</span><span class="sxs-lookup"><span data-stu-id="7561a-103">Gets an attestation.</span></span>

## <span data-ttu-id="7561a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7561a-104">SYNTAX</span></span>

### <span data-ttu-id="7561a-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7561a-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7561a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7561a-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7561a-107">說明</span><span class="sxs-lookup"><span data-stu-id="7561a-107">DESCRIPTION</span></span>
<span data-ttu-id="7561a-108">Get-AzAttestation Cmdlet 會取得訂閱中認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7561a-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="7561a-109">示例</span><span class="sxs-lookup"><span data-stu-id="7561a-109">EXAMPLES</span></span>

### <span data-ttu-id="7561a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7561a-110">Example 1</span></span>
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

<span data-ttu-id="7561a-111">在資源群組 *psh-test-rg* 中取得認證提供者 *pshtest* 。</span><span class="sxs-lookup"><span data-stu-id="7561a-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="7561a-112">參數</span><span class="sxs-lookup"><span data-stu-id="7561a-112">PARAMETERS</span></span>

### <span data-ttu-id="7561a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7561a-113">-DefaultProfile</span></span>
<span data-ttu-id="7561a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7561a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7561a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7561a-115">-Name</span></span>
<span data-ttu-id="7561a-116">認證名稱。</span><span class="sxs-lookup"><span data-stu-id="7561a-116">Attestation Name.</span></span>

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

### <span data-ttu-id="7561a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7561a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7561a-118">指定與所查詢之證明相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7561a-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="7561a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7561a-119">-ResourceId</span></span>
<span data-ttu-id="7561a-120">指定與所查詢之證明相關聯的 ResourceID 的名稱</span><span class="sxs-lookup"><span data-stu-id="7561a-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="7561a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7561a-121">CommonParameters</span></span>
<span data-ttu-id="7561a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7561a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7561a-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7561a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7561a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7561a-124">INPUTS</span></span>

### <span data-ttu-id="7561a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7561a-125">System.String</span></span>

## <span data-ttu-id="7561a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7561a-126">OUTPUTS</span></span>

### <span data-ttu-id="7561a-127">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7561a-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="7561a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7561a-128">NOTES</span></span>

## <span data-ttu-id="7561a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7561a-129">RELATED LINKS</span></span>
