---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284795"
---
# <span data-ttu-id="40b95-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="40b95-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="40b95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40b95-102">SYNOPSIS</span></span>
<span data-ttu-id="40b95-103">刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-103">Deletes the service topology.</span></span> <span data-ttu-id="40b95-104">在刪除服務拓撲之前，必須先刪除在服務拓撲結構中建立的所有服務。</span><span class="sxs-lookup"><span data-stu-id="40b95-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="40b95-105">句法</span><span class="sxs-lookup"><span data-stu-id="40b95-105">SYNTAX</span></span>

### <span data-ttu-id="40b95-106">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="40b95-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b95-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="40b95-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b95-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="40b95-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b95-109">說明</span><span class="sxs-lookup"><span data-stu-id="40b95-109">DESCRIPTION</span></span>
<span data-ttu-id="40b95-110">**AzDeploymentManagerServiceTopology** Cmdlet 會刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="40b95-111">依名稱和資源群組名稱指定服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="40b95-112">或者，您也可以提供 ServiceTopology 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="40b95-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="40b95-113">示例</span><span class="sxs-lookup"><span data-stu-id="40b95-113">EXAMPLES</span></span>

### <span data-ttu-id="40b95-114">範例1</span><span class="sxs-lookup"><span data-stu-id="40b95-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="40b95-115">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="40b95-116">範例2：使用資源識別碼刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="40b95-117">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="40b95-118">範例3：使用服務拓朴物件刪除服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="40b95-119">這個命令會分別刪除名稱和 ResourceGroup 與 $serviceTopologyObject 的 Name 和 ResourceGroupName 屬性相符的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="40b95-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="40b95-120">參數</span><span class="sxs-lookup"><span data-stu-id="40b95-120">PARAMETERS</span></span>

### <span data-ttu-id="40b95-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b95-121">-DefaultProfile</span></span>
<span data-ttu-id="40b95-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40b95-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b95-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40b95-123">-InputObject</span></span>
<span data-ttu-id="40b95-124">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="40b95-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="40b95-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="40b95-125">-Name</span></span>
<span data-ttu-id="40b95-126">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="40b95-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="40b95-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40b95-127">-PassThru</span></span>
<span data-ttu-id="40b95-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="40b95-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="40b95-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b95-129">-ResourceGroupName</span></span>
<span data-ttu-id="40b95-130">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="40b95-130">The resource group.</span></span>

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

### <span data-ttu-id="40b95-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40b95-131">-ResourceId</span></span>
<span data-ttu-id="40b95-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="40b95-132">The resource identifier.</span></span>

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

### <span data-ttu-id="40b95-133">-確認</span><span class="sxs-lookup"><span data-stu-id="40b95-133">-Confirm</span></span>
<span data-ttu-id="40b95-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40b95-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b95-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b95-135">-WhatIf</span></span>
<span data-ttu-id="40b95-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40b95-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b95-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40b95-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b95-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b95-138">CommonParameters</span></span>
<span data-ttu-id="40b95-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40b95-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b95-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="40b95-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b95-141">輸入</span><span class="sxs-lookup"><span data-stu-id="40b95-141">INPUTS</span></span>

### <span data-ttu-id="40b95-142">System.object</span><span class="sxs-lookup"><span data-stu-id="40b95-142">System.String</span></span>

### <span data-ttu-id="40b95-143">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="40b95-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="40b95-144">輸出</span><span class="sxs-lookup"><span data-stu-id="40b95-144">OUTPUTS</span></span>

### <span data-ttu-id="40b95-145">System.object</span><span class="sxs-lookup"><span data-stu-id="40b95-145">System.Boolean</span></span>

## <span data-ttu-id="40b95-146">筆記</span><span class="sxs-lookup"><span data-stu-id="40b95-146">NOTES</span></span>

## <span data-ttu-id="40b95-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="40b95-147">RELATED LINKS</span></span>
