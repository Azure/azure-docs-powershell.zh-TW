---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: ee0f1f855f4f24e3672606bfedc000452ce6040d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622432"
---
# <span data-ttu-id="107af-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="107af-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="107af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="107af-102">SYNOPSIS</span></span>
<span data-ttu-id="107af-103">刪除服務。</span><span class="sxs-lookup"><span data-stu-id="107af-103">Deletes the service..</span></span> <span data-ttu-id="107af-104">必須先刪除服務下所建立的所有服務單位，才能刪除該服務。</span><span class="sxs-lookup"><span data-stu-id="107af-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="107af-105">句法</span><span class="sxs-lookup"><span data-stu-id="107af-105">SYNTAX</span></span>

### <span data-ttu-id="107af-106">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="107af-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="107af-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="107af-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107af-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="107af-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107af-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="107af-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107af-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="107af-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107af-111">說明</span><span class="sxs-lookup"><span data-stu-id="107af-111">DESCRIPTION</span></span>
<span data-ttu-id="107af-112">**AzDeploymentManagerService** Cmdlet 會刪除服務拓朴下的服務。</span><span class="sxs-lookup"><span data-stu-id="107af-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="107af-113">依其名稱指定服務、服務拓撲結構，以及資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="107af-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="107af-114">或者，您也可以提供服務物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="107af-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="107af-115">示例</span><span class="sxs-lookup"><span data-stu-id="107af-115">EXAMPLES</span></span>

### <span data-ttu-id="107af-116">範例1</span><span class="sxs-lookup"><span data-stu-id="107af-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="107af-117">這個命令會在 ContosoResourceGroup 中名為 ContosoServiceTopology 的服務拓撲中，刪除名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="107af-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="107af-118">範例2：使用資源識別碼刪除服務。</span><span class="sxs-lookup"><span data-stu-id="107af-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="107af-119">這個命令會在 ContosoResourceGroup 中名為 ContosoServiceTopology 的服務拓撲中，刪除名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="107af-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="107af-120">範例3：使用服務物件刪除服務。</span><span class="sxs-lookup"><span data-stu-id="107af-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="107af-121">這個命令會分別刪除名稱、服務拓朴名稱和 ResourceGroup 與 $serviceObject 的名稱、ServiceTopologyName 及 ResourceGroupName 屬性相符的服務。</span><span class="sxs-lookup"><span data-stu-id="107af-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="107af-122">參數</span><span class="sxs-lookup"><span data-stu-id="107af-122">PARAMETERS</span></span>

### <span data-ttu-id="107af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107af-123">-DefaultProfile</span></span>
<span data-ttu-id="107af-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="107af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107af-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="107af-125">-InputObject</span></span>
<span data-ttu-id="107af-126">服務物件。</span><span class="sxs-lookup"><span data-stu-id="107af-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="107af-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="107af-127">-Name</span></span>
<span data-ttu-id="107af-128">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="107af-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107af-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="107af-129">-PassThru</span></span>
<span data-ttu-id="107af-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="107af-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="107af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107af-131">-ResourceGroupName</span></span>
<span data-ttu-id="107af-132">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="107af-132">The resource group.</span></span>

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

### <span data-ttu-id="107af-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="107af-133">-ResourceId</span></span>
<span data-ttu-id="107af-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="107af-134">The resource identifier.</span></span>

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

### <span data-ttu-id="107af-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="107af-135">-ServiceTopologyName</span></span>
<span data-ttu-id="107af-136">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="107af-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="107af-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="107af-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="107af-138">應該在其中建立服務的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="107af-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107af-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="107af-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="107af-140">要在其中建立服務的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="107af-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107af-141">-確認</span><span class="sxs-lookup"><span data-stu-id="107af-141">-Confirm</span></span>
<span data-ttu-id="107af-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="107af-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107af-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107af-143">-WhatIf</span></span>
<span data-ttu-id="107af-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="107af-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107af-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="107af-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107af-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107af-146">CommonParameters</span></span>
<span data-ttu-id="107af-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="107af-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107af-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="107af-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107af-149">輸入</span><span class="sxs-lookup"><span data-stu-id="107af-149">INPUTS</span></span>

### <span data-ttu-id="107af-150">System.object</span><span class="sxs-lookup"><span data-stu-id="107af-150">System.String</span></span>

### <span data-ttu-id="107af-151">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="107af-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="107af-152">輸出</span><span class="sxs-lookup"><span data-stu-id="107af-152">OUTPUTS</span></span>

### <span data-ttu-id="107af-153">System.object</span><span class="sxs-lookup"><span data-stu-id="107af-153">System.Boolean</span></span>

## <span data-ttu-id="107af-154">筆記</span><span class="sxs-lookup"><span data-stu-id="107af-154">NOTES</span></span>

## <span data-ttu-id="107af-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="107af-155">RELATED LINKS</span></span>
