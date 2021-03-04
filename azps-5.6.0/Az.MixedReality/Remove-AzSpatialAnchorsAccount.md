---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909014"
---
# <span data-ttu-id="f3eb0-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f3eb0-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f3eb0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3eb0-103">刪除空間錨點帳戶</span><span class="sxs-lookup"><span data-stu-id="f3eb0-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="f3eb0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3eb0-104">SYNTAX</span></span>

### <span data-ttu-id="f3eb0-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f3eb0-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3eb0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3eb0-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3eb0-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3eb0-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3eb0-108">描述</span><span class="sxs-lookup"><span data-stu-id="f3eb0-108">DESCRIPTION</span></span>
<span data-ttu-id="f3eb0-109">刪除特定訂閱和資源群組中指定的空間錨點帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="f3eb0-110">例子</span><span class="sxs-lookup"><span data-stu-id="f3eb0-110">EXAMPLES</span></span>

### <span data-ttu-id="f3eb0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f3eb0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="f3eb0-112">從目前的訂閱和資源群組 "rg1" 刪除空間錨點帳戶的「範例」。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="f3eb0-113">參數</span><span class="sxs-lookup"><span data-stu-id="f3eb0-113">PARAMETERS</span></span>

### <span data-ttu-id="f3eb0-114">-確認</span><span class="sxs-lookup"><span data-stu-id="f3eb0-114">-Confirm</span></span>
<span data-ttu-id="f3eb0-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3eb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3eb0-116">-DefaultProfile</span></span>
<span data-ttu-id="f3eb0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3eb0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3eb0-118">-InputObject</span></span>
<span data-ttu-id="f3eb0-119">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3eb0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3eb0-120">-Name</span></span>
<span data-ttu-id="f3eb0-121">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3eb0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3eb0-122">-PassThru</span></span>
<span data-ttu-id="f3eb0-123">如果指定，則 Return 物件。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3eb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3eb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3eb0-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3eb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3eb0-126">-ResourceId</span></span>
<span data-ttu-id="f3eb0-127">空間錨點帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3eb0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3eb0-128">-WhatIf</span></span>
<span data-ttu-id="f3eb0-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3eb0-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3eb0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3eb0-131">CommonParameters</span></span>
<span data-ttu-id="f3eb0-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f3eb0-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f3eb0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3eb0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f3eb0-134">INPUTS</span></span>

### <span data-ttu-id="f3eb0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f3eb0-135">System.String</span></span>

### <span data-ttu-id="f3eb0-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f3eb0-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="f3eb0-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3eb0-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f3eb0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f3eb0-138">OUTPUTS</span></span>

### <span data-ttu-id="f3eb0-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3eb0-139">System.Boolean</span></span>

## <span data-ttu-id="f3eb0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f3eb0-140">NOTES</span></span>

## <span data-ttu-id="f3eb0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3eb0-141">RELATED LINKS</span></span>
