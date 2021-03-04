---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d3716d18bc883d5407ee4acf3fa43960b63e7cd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909093"
---
# <span data-ttu-id="ef8bc-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ef8bc-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="ef8bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8bc-103">刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-103">Deletes the service topology.</span></span> <span data-ttu-id="ef8bc-104">在服務拓撲下建立的所有服務，在刪除服務拓撲之前，都需要先刪除。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="ef8bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef8bc-105">SYNTAX</span></span>

### <span data-ttu-id="ef8bc-106">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="ef8bc-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8bc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef8bc-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8bc-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="ef8bc-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef8bc-109">描述</span><span class="sxs-lookup"><span data-stu-id="ef8bc-109">DESCRIPTION</span></span>
<span data-ttu-id="ef8bc-110">**Remove-AzDeploymentManagerServiceTop應 Cmdlet** 會刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="ef8bc-111">根據服務拓撲的名稱和資源組名來指定服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="ef8bc-112">或者，您也可以提供 ServiceTopology 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="ef8bc-113">例子</span><span class="sxs-lookup"><span data-stu-id="ef8bc-113">EXAMPLES</span></span>

### <span data-ttu-id="ef8bc-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef8bc-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="ef8bc-115">此命令會刪除 ContosoResourceGroup 中名為 ContosoServiceTopsource 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ef8bc-116">範例 2：使用資源識別碼刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="ef8bc-117">此命令會刪除 ContosoResourceGroup 中名為 ContosoServiceTopsource 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ef8bc-118">範例 3：使用服務拓撲物件刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="ef8bc-119">此命令會刪除服務拓撲，其名稱和資源組會分別符合每個$serviceTopologyObject名稱及 ResourceGroupName 屬性。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="ef8bc-120">參數</span><span class="sxs-lookup"><span data-stu-id="ef8bc-120">PARAMETERS</span></span>

### <span data-ttu-id="ef8bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef8bc-121">-DefaultProfile</span></span>
<span data-ttu-id="ef8bc-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef8bc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef8bc-123">-InputObject</span></span>
<span data-ttu-id="ef8bc-124">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="ef8bc-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef8bc-125">-Name</span></span>
<span data-ttu-id="ef8bc-126">服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef8bc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef8bc-127">-PassThru</span></span>
<span data-ttu-id="ef8bc-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ef8bc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ef8bc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef8bc-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef8bc-130">資源群組。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef8bc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef8bc-131">-ResourceId</span></span>
<span data-ttu-id="ef8bc-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-132">The resource identifier.</span></span>

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

### <span data-ttu-id="ef8bc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ef8bc-133">-Confirm</span></span>
<span data-ttu-id="ef8bc-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef8bc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef8bc-135">-WhatIf</span></span>
<span data-ttu-id="ef8bc-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef8bc-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef8bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8bc-138">CommonParameters</span></span>
<span data-ttu-id="ef8bc-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef8bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef8bc-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef8bc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8bc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ef8bc-141">INPUTS</span></span>

### <span data-ttu-id="ef8bc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ef8bc-142">System.String</span></span>

### <span data-ttu-id="ef8bc-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopserviceserviceResource</span><span class="sxs-lookup"><span data-stu-id="ef8bc-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ef8bc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ef8bc-144">OUTPUTS</span></span>

### <span data-ttu-id="ef8bc-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef8bc-145">System.Boolean</span></span>

## <span data-ttu-id="ef8bc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ef8bc-146">NOTES</span></span>

## <span data-ttu-id="ef8bc-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef8bc-147">RELATED LINKS</span></span>
