---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138743"
---
# <span data-ttu-id="18c4b-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="18c4b-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="18c4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="18c4b-103">刪除空間錨點帳戶</span><span class="sxs-lookup"><span data-stu-id="18c4b-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="18c4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="18c4b-104">SYNTAX</span></span>

### <span data-ttu-id="18c4b-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="18c4b-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c4b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18c4b-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18c4b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="18c4b-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18c4b-108">說明</span><span class="sxs-lookup"><span data-stu-id="18c4b-108">DESCRIPTION</span></span>
<span data-ttu-id="18c4b-109">從特定的訂閱和資源群組刪除指定的空間錨定帳戶。</span><span class="sxs-lookup"><span data-stu-id="18c4b-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="18c4b-110">示例</span><span class="sxs-lookup"><span data-stu-id="18c4b-110">EXAMPLES</span></span>

### <span data-ttu-id="18c4b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="18c4b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="18c4b-112">從目前的訂閱和資源群組 "rg1" 刪除空間錨定帳戶 "範例"。</span><span class="sxs-lookup"><span data-stu-id="18c4b-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="18c4b-113">參數</span><span class="sxs-lookup"><span data-stu-id="18c4b-113">PARAMETERS</span></span>

### <span data-ttu-id="18c4b-114">-確認</span><span class="sxs-lookup"><span data-stu-id="18c4b-114">-Confirm</span></span>
<span data-ttu-id="18c4b-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18c4b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18c4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c4b-116">-DefaultProfile</span></span>
<span data-ttu-id="18c4b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18c4b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c4b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18c4b-118">-InputObject</span></span>
<span data-ttu-id="18c4b-119">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="18c4b-119">The custom domain object.</span></span>

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

### <span data-ttu-id="18c4b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="18c4b-120">-Name</span></span>
<span data-ttu-id="18c4b-121">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="18c4b-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="18c4b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18c4b-122">-PassThru</span></span>
<span data-ttu-id="18c4b-123">傳回物件（如果已指定）。</span><span class="sxs-lookup"><span data-stu-id="18c4b-123">Return object if specified.</span></span>

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

### <span data-ttu-id="18c4b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c4b-124">-ResourceGroupName</span></span>
<span data-ttu-id="18c4b-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="18c4b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="18c4b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18c4b-126">-ResourceId</span></span>
<span data-ttu-id="18c4b-127">空間錨定帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="18c4b-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="18c4b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c4b-128">-WhatIf</span></span>
<span data-ttu-id="18c4b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18c4b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c4b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18c4b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18c4b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c4b-131">CommonParameters</span></span>
<span data-ttu-id="18c4b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18c4b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18c4b-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18c4b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c4b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="18c4b-134">INPUTS</span></span>

### <span data-ttu-id="18c4b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="18c4b-135">System.String</span></span>

### <span data-ttu-id="18c4b-136">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="18c4b-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="18c4b-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="18c4b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18c4b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="18c4b-138">OUTPUTS</span></span>

### <span data-ttu-id="18c4b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="18c4b-139">System.Boolean</span></span>

## <span data-ttu-id="18c4b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="18c4b-140">NOTES</span></span>

## <span data-ttu-id="18c4b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="18c4b-141">RELATED LINKS</span></span>