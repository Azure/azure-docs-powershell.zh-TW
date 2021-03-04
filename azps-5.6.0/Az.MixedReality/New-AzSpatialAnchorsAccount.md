---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906553"
---
# <span data-ttu-id="d8252-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d8252-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d8252-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8252-102">SYNOPSIS</span></span>
<span data-ttu-id="d8252-103">建立空間錨點帳戶</span><span class="sxs-lookup"><span data-stu-id="d8252-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="d8252-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8252-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8252-105">描述</span><span class="sxs-lookup"><span data-stu-id="d8252-105">DESCRIPTION</span></span>
<span data-ttu-id="d8252-106">在特定訂閱、資源群組和地區中建立新空間錨點帳戶。</span><span class="sxs-lookup"><span data-stu-id="d8252-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="d8252-107">例子</span><span class="sxs-lookup"><span data-stu-id="d8252-107">EXAMPLES</span></span>

### <span data-ttu-id="d8252-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d8252-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="d8252-109">在目前的訂閱、資源群組 "rg1" 和美國中，建立新空間錨點帳戶的「範例」。</span><span class="sxs-lookup"><span data-stu-id="d8252-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="d8252-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8252-110">PARAMETERS</span></span>

### <span data-ttu-id="d8252-111">-確認</span><span class="sxs-lookup"><span data-stu-id="d8252-111">-Confirm</span></span>
<span data-ttu-id="d8252-112">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d8252-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8252-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8252-113">-DefaultProfile</span></span>
<span data-ttu-id="d8252-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8252-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8252-115">-位置</span><span class="sxs-lookup"><span data-stu-id="d8252-115">-Location</span></span>
<span data-ttu-id="d8252-116">空間錨點帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="d8252-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8252-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8252-117">-Name</span></span>
<span data-ttu-id="d8252-118">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d8252-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8252-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8252-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8252-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d8252-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8252-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8252-121">-WhatIf</span></span>
<span data-ttu-id="d8252-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8252-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8252-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8252-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8252-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8252-124">CommonParameters</span></span>
<span data-ttu-id="d8252-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8252-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d8252-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d8252-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8252-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d8252-127">INPUTS</span></span>

### <span data-ttu-id="d8252-128">沒有</span><span class="sxs-lookup"><span data-stu-id="d8252-128">None</span></span>

## <span data-ttu-id="d8252-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d8252-129">OUTPUTS</span></span>

### <span data-ttu-id="d8252-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d8252-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d8252-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d8252-131">NOTES</span></span>

## <span data-ttu-id="d8252-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8252-132">RELATED LINKS</span></span>
