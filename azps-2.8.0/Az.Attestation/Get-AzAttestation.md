---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613826"
---
# <span data-ttu-id="88932-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="88932-101">Get-AzAttestation</span></span>

## <span data-ttu-id="88932-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88932-102">SYNOPSIS</span></span>
<span data-ttu-id="88932-103">取得證明。</span><span class="sxs-lookup"><span data-stu-id="88932-103">Gets an attestation.</span></span>

## <span data-ttu-id="88932-104">句法</span><span class="sxs-lookup"><span data-stu-id="88932-104">SYNTAX</span></span>

### <span data-ttu-id="88932-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="88932-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88932-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="88932-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88932-107">說明</span><span class="sxs-lookup"><span data-stu-id="88932-107">DESCRIPTION</span></span>
<span data-ttu-id="88932-108">Get-AzAttestation Cmdlet 會取得訂閱中認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88932-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="88932-109">示例</span><span class="sxs-lookup"><span data-stu-id="88932-109">EXAMPLES</span></span>

### <span data-ttu-id="88932-110">範例1</span><span class="sxs-lookup"><span data-stu-id="88932-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="88932-111">在資源群組 "rg1" 中取得證明「範例」。</span><span class="sxs-lookup"><span data-stu-id="88932-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="88932-112">參數</span><span class="sxs-lookup"><span data-stu-id="88932-112">PARAMETERS</span></span>

### <span data-ttu-id="88932-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88932-113">-DefaultProfile</span></span>
<span data-ttu-id="88932-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88932-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88932-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="88932-115">-Name</span></span>
<span data-ttu-id="88932-116">認證名稱。</span><span class="sxs-lookup"><span data-stu-id="88932-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88932-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88932-117">-ResourceGroupName</span></span>
<span data-ttu-id="88932-118">指定與所查詢之證明相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88932-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88932-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88932-119">-ResourceId</span></span>
<span data-ttu-id="88932-120">指定與所查詢之證明相關聯的 ResourceID 的名稱</span><span class="sxs-lookup"><span data-stu-id="88932-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88932-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88932-121">CommonParameters</span></span>
<span data-ttu-id="88932-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88932-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88932-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88932-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88932-124">輸入</span><span class="sxs-lookup"><span data-stu-id="88932-124">INPUTS</span></span>

### <span data-ttu-id="88932-125">System.object</span><span class="sxs-lookup"><span data-stu-id="88932-125">System.String</span></span>

## <span data-ttu-id="88932-126">輸出</span><span class="sxs-lookup"><span data-stu-id="88932-126">OUTPUTS</span></span>

### <span data-ttu-id="88932-127">PSAttestation 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="88932-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="88932-128">筆記</span><span class="sxs-lookup"><span data-stu-id="88932-128">NOTES</span></span>

## <span data-ttu-id="88932-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="88932-129">RELATED LINKS</span></span>
