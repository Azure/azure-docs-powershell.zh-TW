---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 12a2e8b27697436a38753c054f178878b9ed3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909106"
---
# <span data-ttu-id="892b7-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="892b7-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="892b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="892b7-102">SYNOPSIS</span></span>
<span data-ttu-id="892b7-103">獲得服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-103">Gets the service.</span></span>

## <span data-ttu-id="892b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="892b7-104">SYNTAX</span></span>

### <span data-ttu-id="892b7-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="892b7-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892b7-106">ByServiceTopserviceObject</span><span class="sxs-lookup"><span data-stu-id="892b7-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="892b7-107">ByServiceTopsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="892b7-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892b7-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="892b7-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="892b7-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="892b7-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="892b7-110">描述</span><span class="sxs-lookup"><span data-stu-id="892b7-110">DESCRIPTION</span></span>
<span data-ttu-id="892b7-111">**Get-AzDeploymentManagerService** Cmdlet 會依據服務拓撲取得服務，並會返回代表該服務的物件。</span><span class="sxs-lookup"><span data-stu-id="892b7-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="892b7-112">根據服務的名稱、服務拓撲和資源組名來指定服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="892b7-113">或者，您也可以提供 Service 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="892b7-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="892b7-114">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerService服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="892b7-115">例子</span><span class="sxs-lookup"><span data-stu-id="892b7-115">EXAMPLES</span></span>

### <span data-ttu-id="892b7-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="892b7-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="892b7-117">此命令會以 ContosoResourceGroup 中名為 ContosoServiceTop內的服務拓撲，獲得名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="892b7-118">範例 2：使用資源識別碼取得服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="892b7-119">此命令會以 ContosoResourceGroup 中名為 ContosoServiceTop內的服務拓撲，獲得名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="892b7-120">範例 3：使用服務物件取得服務。</span><span class="sxs-lookup"><span data-stu-id="892b7-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="892b7-121">此命令會獲得服務，其名稱、服務拓撲名稱及 ResourceGroup 會分別符合該名稱、ServiceTopologyName 和 ResourceGroupName 屬性$serviceObject名稱。</span><span class="sxs-lookup"><span data-stu-id="892b7-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="892b7-122">參數</span><span class="sxs-lookup"><span data-stu-id="892b7-122">PARAMETERS</span></span>

### <span data-ttu-id="892b7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892b7-123">-DefaultProfile</span></span>
<span data-ttu-id="892b7-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="892b7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="892b7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="892b7-125">-InputObject</span></span>
<span data-ttu-id="892b7-126">服務物件。</span><span class="sxs-lookup"><span data-stu-id="892b7-126">Service object.</span></span>

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

### <span data-ttu-id="892b7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="892b7-127">-Name</span></span>
<span data-ttu-id="892b7-128">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="892b7-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892b7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892b7-129">-ResourceGroupName</span></span>
<span data-ttu-id="892b7-130">資源群組。</span><span class="sxs-lookup"><span data-stu-id="892b7-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892b7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="892b7-131">-ResourceId</span></span>
<span data-ttu-id="892b7-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="892b7-132">The resource identifier.</span></span>

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

### <span data-ttu-id="892b7-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="892b7-133">-ServiceTopologyName</span></span>
<span data-ttu-id="892b7-134">服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="892b7-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="892b7-135">-ServiceTopectObject</span><span class="sxs-lookup"><span data-stu-id="892b7-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="892b7-136">服務應建立的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="892b7-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892b7-137">-ServiceTopsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="892b7-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="892b7-138">服務應建立的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="892b7-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892b7-139">CommonParameters</span></span>
<span data-ttu-id="892b7-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="892b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892b7-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="892b7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892b7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="892b7-142">INPUTS</span></span>

### <span data-ttu-id="892b7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="892b7-143">System.String</span></span>

### <span data-ttu-id="892b7-144">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="892b7-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="892b7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="892b7-145">OUTPUTS</span></span>

### <span data-ttu-id="892b7-146">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="892b7-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="892b7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="892b7-147">NOTES</span></span>

## <span data-ttu-id="892b7-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="892b7-148">RELATED LINKS</span></span>
