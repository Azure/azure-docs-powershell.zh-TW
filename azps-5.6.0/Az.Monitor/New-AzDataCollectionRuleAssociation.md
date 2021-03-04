---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1086f67bcec4adeef74fe7bf591e61d9d08a90e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910069"
---
# <span data-ttu-id="ba92f-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="ba92f-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="ba92f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba92f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba92f-103">建立資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="ba92f-103">Create data collection rule association.</span></span>

## <span data-ttu-id="ba92f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba92f-104">SYNTAX</span></span>

### <span data-ttu-id="ba92f-105">ByDataCollectionRuleId (預設) </span><span class="sxs-lookup"><span data-stu-id="ba92f-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="ba92f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba92f-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="ba92f-107">描述</span><span class="sxs-lookup"><span data-stu-id="ba92f-107">DESCRIPTION</span></span>
<span data-ttu-id="ba92f-108">**New-AzDataCollectionRuleAssociation** Cmdlet 會建立資料集合規則關聯 (DCRA) 。</span><span class="sxs-lookup"><span data-stu-id="ba92f-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="ba92f-109">若要將 DCR 適用于虛擬機器，請建立虛擬機器的關聯。</span><span class="sxs-lookup"><span data-stu-id="ba92f-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="ba92f-110">虛擬機器可能與多個 DCRs 相關聯，而 DCR 可能有多個與它相關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ba92f-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="ba92f-111">這可讓您定義一組符合特定要求的 DCRs，並只將它們套用至其套用之虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ba92f-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="ba92f-112">以下是使用 DCRA [文章的](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 「設定 Azure 監視器代理程式的資料集合」。</span><span class="sxs-lookup"><span data-stu-id="ba92f-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="ba92f-113">例子</span><span class="sxs-lookup"><span data-stu-id="ba92f-113">EXAMPLES</span></span>

### <span data-ttu-id="ba92f-114">範例 1：建立資料收集規則關聯</span><span class="sxs-lookup"><span data-stu-id="ba92f-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="ba92f-115">此命令會為給定規則和目標資源識別碼建立資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="ba92f-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="ba92f-116">範例 2：從 DCR 物件建立資料收集規則關聯</span><span class="sxs-lookup"><span data-stu-id="ba92f-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="ba92f-117">此命令會為給定規則和目標資源識別碼建立資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="ba92f-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="ba92f-118">參數</span><span class="sxs-lookup"><span data-stu-id="ba92f-118">PARAMETERS</span></span>

### <span data-ttu-id="ba92f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba92f-119">-DefaultProfile</span></span>
<span data-ttu-id="ba92f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ba92f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba92f-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ba92f-121">-TargetResourceId</span></span>
<span data-ttu-id="ba92f-122">要關聯的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ba92f-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba92f-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="ba92f-123">-AssociationName</span></span>
<span data-ttu-id="ba92f-124">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ba92f-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba92f-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ba92f-125">-RuleId</span></span>
<span data-ttu-id="ba92f-126">資料收集規則識別碼</span><span class="sxs-lookup"><span data-stu-id="ba92f-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba92f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba92f-127">-InputObject</span></span>
<span data-ttu-id="ba92f-128">PSDataCollectionRuleResource 物件</span><span class="sxs-lookup"><span data-stu-id="ba92f-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="ba92f-129">-描述</span><span class="sxs-lookup"><span data-stu-id="ba92f-129">-Description</span></span>
<span data-ttu-id="ba92f-130">資源描述</span><span class="sxs-lookup"><span data-stu-id="ba92f-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba92f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ba92f-131">-Confirm</span></span>
<span data-ttu-id="ba92f-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba92f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba92f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba92f-133">-WhatIf</span></span>
<span data-ttu-id="ba92f-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba92f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba92f-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba92f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba92f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba92f-136">CommonParameters</span></span>
<span data-ttu-id="ba92f-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba92f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba92f-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba92f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba92f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ba92f-139">INPUTS</span></span>

### <span data-ttu-id="ba92f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ba92f-140">System.String</span></span>

## <span data-ttu-id="ba92f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ba92f-141">OUTPUTS</span></span>

### <span data-ttu-id="ba92f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="ba92f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="ba92f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ba92f-143">NOTES</span></span>

## <span data-ttu-id="ba92f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba92f-144">RELATED LINKS</span></span>

<span data-ttu-id="ba92f-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md) 
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="ba92f-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md)
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
