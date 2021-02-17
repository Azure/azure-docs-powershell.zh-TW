---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140610"
---
# <span data-ttu-id="5003b-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="5003b-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="5003b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5003b-102">SYNOPSIS</span></span>
<span data-ttu-id="5003b-103">刪除資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="5003b-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="5003b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5003b-104">SYNTAX</span></span>

### <span data-ttu-id="5003b-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="5003b-105">ByName (Default)</span></span>
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

### <span data-ttu-id="5003b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5003b-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="5003b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5003b-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="5003b-108">說明</span><span class="sxs-lookup"><span data-stu-id="5003b-108">DESCRIPTION</span></span>
<span data-ttu-id="5003b-109">**AzDataCollectionRuleAssociation** Cmdlet 會刪除資料收集規則關聯 (DCRA) 。</span><span class="sxs-lookup"><span data-stu-id="5003b-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="5003b-110">若要將 DCR 套用至虛擬機器，您需要建立虛擬機器的關聯。</span><span class="sxs-lookup"><span data-stu-id="5003b-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="5003b-111">虛擬機器可能有多個 DCRs 的關聯，而 DCR 可能會有多個與其關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5003b-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="5003b-112">這可讓您定義一組 DCRs，每個與特定需求相符，並將它們只套用至它們適用的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5003b-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="5003b-113">以下是使用 DCRA 文章的「 [設定 Azure 監視器代理的資料收集](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 」。</span><span class="sxs-lookup"><span data-stu-id="5003b-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="5003b-114">示例</span><span class="sxs-lookup"><span data-stu-id="5003b-114">EXAMPLES</span></span>

### <span data-ttu-id="5003b-115">範例1：刪除資料收集規則關聯，並將名稱和目標資源識別碼 (關聯的虛擬機器) 參數</span><span class="sxs-lookup"><span data-stu-id="5003b-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="5003b-116">範例2：刪除含輸入物件的資料收集規則</span><span class="sxs-lookup"><span data-stu-id="5003b-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="5003b-117">範例3：使用 [關聯資源識別碼] 屬性刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="5003b-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="5003b-118">參數</span><span class="sxs-lookup"><span data-stu-id="5003b-118">PARAMETERS</span></span>

### <span data-ttu-id="5003b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5003b-119">-DefaultProfile</span></span>
<span data-ttu-id="5003b-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5003b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5003b-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5003b-121">-TargetResourceId</span></span>
<span data-ttu-id="5003b-122">關聯的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5003b-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="5003b-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="5003b-123">-AssociationName</span></span>
<span data-ttu-id="5003b-124">關聯資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5003b-124">The name of the association resource.</span></span>

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

### <span data-ttu-id="5003b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5003b-125">-InputObject</span></span>
<span data-ttu-id="5003b-126">PSDataCollectionRuleResource 物件</span><span class="sxs-lookup"><span data-stu-id="5003b-126">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="5003b-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="5003b-127">-AssociationId</span></span>
<span data-ttu-id="5003b-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5003b-128">The resource identifier.</span></span>

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

### <span data-ttu-id="5003b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="5003b-129">-Confirm</span></span>
<span data-ttu-id="5003b-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5003b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5003b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5003b-131">-WhatIf</span></span>
<span data-ttu-id="5003b-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5003b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5003b-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5003b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5003b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5003b-134">CommonParameters</span></span>
<span data-ttu-id="5003b-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5003b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5003b-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5003b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5003b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5003b-137">INPUTS</span></span>

### <span data-ttu-id="5003b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="5003b-138">System.String</span></span>
###<span data-ttu-id="5003b-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="5003b-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="5003b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5003b-140">OUTPUTS</span></span>

### <span data-ttu-id="5003b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5003b-141">System.Boolean</span></span>

## <span data-ttu-id="5003b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5003b-142">NOTES</span></span>

## <span data-ttu-id="5003b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5003b-143">RELATED LINKS</span></span>

<span data-ttu-id="5003b-144">[AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[新-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="5003b-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
