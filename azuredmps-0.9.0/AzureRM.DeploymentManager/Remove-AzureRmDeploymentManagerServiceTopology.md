---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442580"
---
# <span data-ttu-id="e32d3-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e32d3-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="e32d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e32d3-102">SYNOPSIS</span></span>
<span data-ttu-id="e32d3-103">刪除服務拓撲及其所有資源。</span><span class="sxs-lookup"><span data-stu-id="e32d3-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="e32d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e32d3-104">SYNTAX</span></span>

### <span data-ttu-id="e32d3-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="e32d3-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32d3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e32d3-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32d3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e32d3-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32d3-108">說明</span><span class="sxs-lookup"><span data-stu-id="e32d3-108">DESCRIPTION</span></span>
<span data-ttu-id="e32d3-109">**AzureRmDeploymentManagerServiceTopology** Cmdlet 會刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="e32d3-110">依名稱和資源群組名稱指定服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="e32d3-111">或者，您也可以提供 ServiceTopology 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e32d3-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="e32d3-112">示例</span><span class="sxs-lookup"><span data-stu-id="e32d3-112">EXAMPLES</span></span>

### <span data-ttu-id="e32d3-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e32d3-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="e32d3-114">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e32d3-115">範例2：使用資源識別碼刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="e32d3-116">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e32d3-117">範例3：使用服務拓朴物件刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="e32d3-118">這個命令會分別刪除名稱和 ResourceGroup 與 $serviceTopologyObject 的 Name 和 ResourceGroupName 屬性相符的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="e32d3-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="e32d3-119">參數</span><span class="sxs-lookup"><span data-stu-id="e32d3-119">PARAMETERS</span></span>

### <span data-ttu-id="e32d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32d3-120">-DefaultProfile</span></span>
<span data-ttu-id="e32d3-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e32d3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e32d3-122">-Force</span></span>
<span data-ttu-id="e32d3-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e32d3-123">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e32d3-124">-Name</span></span>
<span data-ttu-id="e32d3-125">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="e32d3-125">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e32d3-126">-PassThru</span></span>
<span data-ttu-id="e32d3-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="e32d3-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="e32d3-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="e32d3-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e32d3-130">-ResourceId</span></span>
<span data-ttu-id="e32d3-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e32d3-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e32d3-132">-ServiceTopology</span></span>
<span data-ttu-id="e32d3-133">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="e32d3-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e32d3-134">-Confirm</span></span>
<span data-ttu-id="e32d3-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e32d3-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32d3-136">-WhatIf</span></span>
<span data-ttu-id="e32d3-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e32d3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e32d3-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e32d3-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32d3-139">CommonParameters</span></span>
<span data-ttu-id="e32d3-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e32d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32d3-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e32d3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32d3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e32d3-142">INPUTS</span></span>

### <span data-ttu-id="e32d3-143">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="e32d3-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="e32d3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e32d3-144">OUTPUTS</span></span>

### <span data-ttu-id="e32d3-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e32d3-145">System.Boolean</span></span>

## <span data-ttu-id="e32d3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e32d3-146">NOTES</span></span>

## <span data-ttu-id="e32d3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e32d3-147">RELATED LINKS</span></span>

[<span data-ttu-id="e32d3-148">新-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e32d3-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="e32d3-149">AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e32d3-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="e32d3-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e32d3-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)