---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129110"
---
# <span data-ttu-id="c2bcb-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="c2bcb-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="c2bcb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2bcb-103">取得資料收集規則關聯 (s) 。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="c2bcb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2bcb-104">SYNTAX</span></span>

### <span data-ttu-id="c2bcb-105">ByAssociatedResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c2bcb-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="c2bcb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c2bcb-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="c2bcb-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="c2bcb-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="c2bcb-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2bcb-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="c2bcb-109">說明</span><span class="sxs-lookup"><span data-stu-id="c2bcb-109">DESCRIPTION</span></span>
<span data-ttu-id="c2bcb-110">**AzDataCollectionRuleAssociation** Cmdlet 會取得一或多個資料收集規則關聯 (DCRA) 。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="c2bcb-111">若要將 DCR 套用至虛擬機器，您需要建立虛擬機器的關聯。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="c2bcb-112">虛擬機器可能有多個 DCRs 的關聯，而 DCR 可能會有多個與其關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="c2bcb-113">這可讓您定義一組 DCRs，每個與特定需求相符，並將它們只套用至它們適用的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="c2bcb-114">以下是使用 DCRA 文章的「 [設定 Azure 監視器代理的資料收集](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 」。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="c2bcb-115">示例</span><span class="sxs-lookup"><span data-stu-id="c2bcb-115">EXAMPLES</span></span>

### <span data-ttu-id="c2bcb-116">範例1：根據目標資源識別碼取得資料收集規則關聯 (關聯的虛擬機器) </span><span class="sxs-lookup"><span data-stu-id="c2bcb-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="c2bcb-117">這個命令會列出指定目標資源識別碼的所有資料收集規則， (虛擬機器) 。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="c2bcb-118">範例2：透過規則 (DCR) 取得資料收集規則關聯</span><span class="sxs-lookup"><span data-stu-id="c2bcb-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="c2bcb-119">這個命令會列出指定資源群組和規則 (DCR) 的資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="c2bcb-120">範例3：透過 input 物件 (PSDataCollectionRuleResource) 取得資料收集規則關聯</span><span class="sxs-lookup"><span data-stu-id="c2bcb-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="c2bcb-121">這個命令會列出指定輸入物件的資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="c2bcb-122">範例4：根據目標資源識別碼取得資料收集規則關聯 (關聯的虛擬機器) 與關聯名稱</span><span class="sxs-lookup"><span data-stu-id="c2bcb-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="c2bcb-123">這個命令會列出一個 (清單，其中只有一個元素) 資料收集規則關聯。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="c2bcb-124">參數</span><span class="sxs-lookup"><span data-stu-id="c2bcb-124">PARAMETERS</span></span>

### <span data-ttu-id="c2bcb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2bcb-125">-DefaultProfile</span></span>
<span data-ttu-id="c2bcb-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c2bcb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2bcb-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c2bcb-127">-TargetResourceId</span></span>
<span data-ttu-id="c2bcb-128">關聯的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2bcb-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="c2bcb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2bcb-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2bcb-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c2bcb-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2bcb-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c2bcb-131">-RuleName</span></span>
<span data-ttu-id="c2bcb-132">資料收集規則名稱</span><span class="sxs-lookup"><span data-stu-id="c2bcb-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2bcb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2bcb-133">-InputObject</span></span>
<span data-ttu-id="c2bcb-134">PSDataCollectionRuleResource 物件</span><span class="sxs-lookup"><span data-stu-id="c2bcb-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="c2bcb-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="c2bcb-135">-AssociationName</span></span>
<span data-ttu-id="c2bcb-136">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-136">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2bcb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2bcb-137">CommonParameters</span></span>
<span data-ttu-id="c2bcb-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2bcb-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2bcb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2bcb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c2bcb-140">INPUTS</span></span>

### <span data-ttu-id="c2bcb-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c2bcb-141">System.String</span></span>
### <span data-ttu-id="c2bcb-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="c2bcb-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="c2bcb-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c2bcb-143">OUTPUTS</span></span>

### <span data-ttu-id="c2bcb-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="c2bcb-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="c2bcb-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c2bcb-145">NOTES</span></span>

## <span data-ttu-id="c2bcb-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2bcb-146">RELATED LINKS</span></span>

<span data-ttu-id="c2bcb-147">[移除-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
[新-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="c2bcb-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
