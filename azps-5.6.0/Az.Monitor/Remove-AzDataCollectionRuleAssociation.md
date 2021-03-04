---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910998"
---
# <span data-ttu-id="98c59-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="98c59-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="98c59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98c59-102">SYNOPSIS</span></span>
<span data-ttu-id="98c59-103">刪除資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="98c59-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="98c59-104">語法</span><span class="sxs-lookup"><span data-stu-id="98c59-104">SYNTAX</span></span>

### <span data-ttu-id="98c59-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="98c59-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="98c59-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98c59-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="98c59-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98c59-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="98c59-108">描述</span><span class="sxs-lookup"><span data-stu-id="98c59-108">DESCRIPTION</span></span>
<span data-ttu-id="98c59-109">**Remove-AzDataCollectionRuleAssociation Cmdlet** 會刪除 DCRA (規則關聯) 。</span><span class="sxs-lookup"><span data-stu-id="98c59-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="98c59-110">若要將 DCR 適用于虛擬機器，請建立虛擬機器的關聯。</span><span class="sxs-lookup"><span data-stu-id="98c59-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="98c59-111">虛擬機器可能與多個 DCRs 相關聯，而 DCR 可能有多個與它相關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="98c59-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="98c59-112">這可讓您定義一組符合特定要求的 DCRs，並只將它們套用至其套用之虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="98c59-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="98c59-113">以下是使用 DCRA [文章的](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 「設定 Azure 監視器代理程式的資料集合」。</span><span class="sxs-lookup"><span data-stu-id="98c59-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="98c59-114">例子</span><span class="sxs-lookup"><span data-stu-id="98c59-114">EXAMPLES</span></span>

### <span data-ttu-id="98c59-115">範例 1：刪除與名稱和目標資源識別碼相關聯的資料收集規則關聯 (關聯的虛擬機器) 參數</span><span class="sxs-lookup"><span data-stu-id="98c59-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="98c59-116">範例 2：使用 Input Object 刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="98c59-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="98c59-117">範例 3：使用關聯資源識別碼屬性刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="98c59-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="98c59-118">參數</span><span class="sxs-lookup"><span data-stu-id="98c59-118">PARAMETERS</span></span>

### <span data-ttu-id="98c59-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c59-119">-DefaultProfile</span></span>
<span data-ttu-id="98c59-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="98c59-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c59-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="98c59-121">-TargetResourceId</span></span>
<span data-ttu-id="98c59-122">相關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98c59-122">The associated resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c59-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="98c59-123">-AssociationName</span></span>
<span data-ttu-id="98c59-124">關聯資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="98c59-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c59-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98c59-125">-InputObject</span></span>
<span data-ttu-id="98c59-126">PSDataCollectionRuleResource 物件</span><span class="sxs-lookup"><span data-stu-id="98c59-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="98c59-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="98c59-127">-AssociationId</span></span>
<span data-ttu-id="98c59-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98c59-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c59-129">-確認</span><span class="sxs-lookup"><span data-stu-id="98c59-129">-Confirm</span></span>
<span data-ttu-id="98c59-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="98c59-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c59-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c59-131">-WhatIf</span></span>
<span data-ttu-id="98c59-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98c59-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c59-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98c59-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c59-134">CommonParameters</span></span>
<span data-ttu-id="98c59-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98c59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c59-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98c59-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c59-137">輸入</span><span class="sxs-lookup"><span data-stu-id="98c59-137">INPUTS</span></span>

### <span data-ttu-id="98c59-138">System.String</span><span class="sxs-lookup"><span data-stu-id="98c59-138">System.String</span></span>
###<span data-ttu-id="98c59-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="98c59-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="98c59-140">輸出</span><span class="sxs-lookup"><span data-stu-id="98c59-140">OUTPUTS</span></span>

### <span data-ttu-id="98c59-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98c59-141">System.Boolean</span></span>

## <span data-ttu-id="98c59-142">筆記</span><span class="sxs-lookup"><span data-stu-id="98c59-142">NOTES</span></span>

## <span data-ttu-id="98c59-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="98c59-143">RELATED LINKS</span></span>

<span data-ttu-id="98c59-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="98c59-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
