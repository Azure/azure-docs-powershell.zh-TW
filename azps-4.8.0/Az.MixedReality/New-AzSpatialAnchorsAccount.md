---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129437"
---
# <span data-ttu-id="98652-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="98652-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="98652-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98652-102">SYNOPSIS</span></span>
<span data-ttu-id="98652-103">建立空間錨點帳戶</span><span class="sxs-lookup"><span data-stu-id="98652-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="98652-104">句法</span><span class="sxs-lookup"><span data-stu-id="98652-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98652-105">說明</span><span class="sxs-lookup"><span data-stu-id="98652-105">DESCRIPTION</span></span>
<span data-ttu-id="98652-106">在特定的訂閱、資源群組和區域中建立新的空間錨點帳戶。</span><span class="sxs-lookup"><span data-stu-id="98652-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="98652-107">示例</span><span class="sxs-lookup"><span data-stu-id="98652-107">EXAMPLES</span></span>

### <span data-ttu-id="98652-108">範例1</span><span class="sxs-lookup"><span data-stu-id="98652-108">Example 1</span></span>
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

<span data-ttu-id="98652-109">在目前訂閱、資源群組 "rg1" 和美國中部建立新的空間錨點帳戶「範例」。</span><span class="sxs-lookup"><span data-stu-id="98652-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="98652-110">參數</span><span class="sxs-lookup"><span data-stu-id="98652-110">PARAMETERS</span></span>

### <span data-ttu-id="98652-111">-確認</span><span class="sxs-lookup"><span data-stu-id="98652-111">-Confirm</span></span>
<span data-ttu-id="98652-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98652-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98652-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98652-113">-DefaultProfile</span></span>
<span data-ttu-id="98652-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98652-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98652-115">-位置</span><span class="sxs-lookup"><span data-stu-id="98652-115">-Location</span></span>
<span data-ttu-id="98652-116">空間錨點帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="98652-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="98652-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="98652-117">-Name</span></span>
<span data-ttu-id="98652-118">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="98652-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="98652-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98652-119">-ResourceGroupName</span></span>
<span data-ttu-id="98652-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="98652-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="98652-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98652-121">-WhatIf</span></span>
<span data-ttu-id="98652-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98652-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98652-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98652-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98652-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98652-124">CommonParameters</span></span>
<span data-ttu-id="98652-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98652-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98652-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98652-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98652-127">輸入</span><span class="sxs-lookup"><span data-stu-id="98652-127">INPUTS</span></span>

### <span data-ttu-id="98652-128">所有</span><span class="sxs-lookup"><span data-stu-id="98652-128">None</span></span>

## <span data-ttu-id="98652-129">輸出</span><span class="sxs-lookup"><span data-stu-id="98652-129">OUTPUTS</span></span>

### <span data-ttu-id="98652-130">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="98652-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="98652-131">筆記</span><span class="sxs-lookup"><span data-stu-id="98652-131">NOTES</span></span>

## <span data-ttu-id="98652-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="98652-132">RELATED LINKS</span></span>
