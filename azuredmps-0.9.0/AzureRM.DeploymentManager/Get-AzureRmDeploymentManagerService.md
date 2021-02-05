---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572100"
---
# <span data-ttu-id="24263-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="24263-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="24263-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24263-102">SYNOPSIS</span></span>
<span data-ttu-id="24263-103">取得服務拓朴中的服務。</span><span class="sxs-lookup"><span data-stu-id="24263-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="24263-104">句法</span><span class="sxs-lookup"><span data-stu-id="24263-104">SYNTAX</span></span>

### <span data-ttu-id="24263-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="24263-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24263-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="24263-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24263-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="24263-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24263-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="24263-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24263-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="24263-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24263-110">說明</span><span class="sxs-lookup"><span data-stu-id="24263-110">DESCRIPTION</span></span>
<span data-ttu-id="24263-111">**AzureRmDeploymentManagerService** Cmdlet 會在服務拓撲下取得服務，並傳回代表該服務的物件。</span><span class="sxs-lookup"><span data-stu-id="24263-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="24263-112">依其名稱指定服務、服務拓撲結構，以及資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="24263-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="24263-113">或者，您也可以提供服務物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="24263-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="24263-114">您可以在本機修改這個物件，然後使用 Set-AzureRmDeploymentManagerService Cmdlet 將變更套用至服務。</span><span class="sxs-lookup"><span data-stu-id="24263-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="24263-115">示例</span><span class="sxs-lookup"><span data-stu-id="24263-115">EXAMPLES</span></span>

### <span data-ttu-id="24263-116">範例1</span><span class="sxs-lookup"><span data-stu-id="24263-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="24263-117">這個命令會在 ContosoResourceGroup 中，在名為 ContosoServiceTopology 的服務拓撲中取得名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="24263-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="24263-118">範例2：使用資源識別碼取得服務。</span><span class="sxs-lookup"><span data-stu-id="24263-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="24263-119">這個命令會在 ContosoResourceGroup 中，在名為 ContosoServiceTopology 的服務拓撲中取得名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="24263-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="24263-120">範例3：使用服務物件取得服務。</span><span class="sxs-lookup"><span data-stu-id="24263-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="24263-121">這個命令會分別取得名稱、服務拓朴名稱和 ResourceGroup 與 $serviceObject 的 Name、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務。</span><span class="sxs-lookup"><span data-stu-id="24263-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="24263-122">參數</span><span class="sxs-lookup"><span data-stu-id="24263-122">PARAMETERS</span></span>

### <span data-ttu-id="24263-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24263-123">-DefaultProfile</span></span>
<span data-ttu-id="24263-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24263-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24263-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="24263-125">-Name</span></span>
<span data-ttu-id="24263-126">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="24263-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24263-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24263-127">-ResourceGroupName</span></span>
<span data-ttu-id="24263-128">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="24263-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24263-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24263-129">-ResourceId</span></span>
<span data-ttu-id="24263-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24263-130">The resource identifier.</span></span>

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

### <span data-ttu-id="24263-131">-服務</span><span class="sxs-lookup"><span data-stu-id="24263-131">-Service</span></span>
<span data-ttu-id="24263-132">服務物件。</span><span class="sxs-lookup"><span data-stu-id="24263-132">Service object.</span></span>

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

### <span data-ttu-id="24263-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="24263-133">-ServiceTopology</span></span>
<span data-ttu-id="24263-134">應該在其中建立服務的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="24263-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="24263-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="24263-135">-ServiceTopologyName</span></span>
<span data-ttu-id="24263-136">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="24263-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="24263-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="24263-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="24263-138">要在其中建立服務的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24263-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="24263-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24263-139">CommonParameters</span></span>
<span data-ttu-id="24263-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24263-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24263-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24263-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24263-142">輸入</span><span class="sxs-lookup"><span data-stu-id="24263-142">INPUTS</span></span>

### <span data-ttu-id="24263-143">所有</span><span class="sxs-lookup"><span data-stu-id="24263-143">None</span></span>

## <span data-ttu-id="24263-144">輸出</span><span class="sxs-lookup"><span data-stu-id="24263-144">OUTPUTS</span></span>

### <span data-ttu-id="24263-145">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="24263-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="24263-146">筆記</span><span class="sxs-lookup"><span data-stu-id="24263-146">NOTES</span></span>

## <span data-ttu-id="24263-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="24263-147">RELATED LINKS</span></span>

[<span data-ttu-id="24263-148">新-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="24263-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="24263-149">移除-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="24263-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="24263-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="24263-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
