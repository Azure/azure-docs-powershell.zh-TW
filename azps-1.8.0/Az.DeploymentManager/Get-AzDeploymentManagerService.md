---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622453"
---
# <span data-ttu-id="88777-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="88777-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="88777-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88777-102">SYNOPSIS</span></span>
<span data-ttu-id="88777-103">取得服務。</span><span class="sxs-lookup"><span data-stu-id="88777-103">Gets the service.</span></span>

## <span data-ttu-id="88777-104">句法</span><span class="sxs-lookup"><span data-stu-id="88777-104">SYNTAX</span></span>

### <span data-ttu-id="88777-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="88777-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88777-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="88777-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88777-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="88777-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88777-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="88777-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88777-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="88777-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88777-110">說明</span><span class="sxs-lookup"><span data-stu-id="88777-110">DESCRIPTION</span></span>
<span data-ttu-id="88777-111">**AzDeploymentManagerService** Cmdlet 會在服務拓撲下取得服務，並傳回代表該服務的物件。</span><span class="sxs-lookup"><span data-stu-id="88777-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="88777-112">依其名稱指定服務、服務拓撲結構，以及資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="88777-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="88777-113">或者，您也可以提供服務物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="88777-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="88777-114">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerService Cmdlet 將變更套用至服務。</span><span class="sxs-lookup"><span data-stu-id="88777-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="88777-115">示例</span><span class="sxs-lookup"><span data-stu-id="88777-115">EXAMPLES</span></span>

### <span data-ttu-id="88777-116">範例1</span><span class="sxs-lookup"><span data-stu-id="88777-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="88777-117">這個命令會在 ContosoResourceGroup 中，在名為 ContosoServiceTopology 的服務拓撲中取得名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="88777-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="88777-118">範例2：使用資源識別碼取得服務。</span><span class="sxs-lookup"><span data-stu-id="88777-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="88777-119">這個命令會在 ContosoResourceGroup 中，在名為 ContosoServiceTopology 的服務拓撲中取得名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="88777-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="88777-120">範例3：使用服務物件取得服務。</span><span class="sxs-lookup"><span data-stu-id="88777-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="88777-121">這個命令會分別取得名稱、服務拓朴名稱和 ResourceGroup 與 $serviceObject 的 Name、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務。</span><span class="sxs-lookup"><span data-stu-id="88777-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="88777-122">參數</span><span class="sxs-lookup"><span data-stu-id="88777-122">PARAMETERS</span></span>

### <span data-ttu-id="88777-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88777-123">-DefaultProfile</span></span>
<span data-ttu-id="88777-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88777-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88777-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88777-125">-InputObject</span></span>
<span data-ttu-id="88777-126">服務物件。</span><span class="sxs-lookup"><span data-stu-id="88777-126">Service object.</span></span>

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

### <span data-ttu-id="88777-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="88777-127">-Name</span></span>
<span data-ttu-id="88777-128">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="88777-128">The name of the service.</span></span>

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

### <span data-ttu-id="88777-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88777-129">-ResourceGroupName</span></span>
<span data-ttu-id="88777-130">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="88777-130">The resource group.</span></span>

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

### <span data-ttu-id="88777-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88777-131">-ResourceId</span></span>
<span data-ttu-id="88777-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88777-132">The resource identifier.</span></span>

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

### <span data-ttu-id="88777-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="88777-133">-ServiceTopologyName</span></span>
<span data-ttu-id="88777-134">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="88777-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="88777-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="88777-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="88777-136">應該在其中建立服務的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="88777-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="88777-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="88777-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="88777-138">要在其中建立服務的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88777-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="88777-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88777-139">CommonParameters</span></span>
<span data-ttu-id="88777-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88777-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88777-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88777-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88777-142">輸入</span><span class="sxs-lookup"><span data-stu-id="88777-142">INPUTS</span></span>

### <span data-ttu-id="88777-143">System.object</span><span class="sxs-lookup"><span data-stu-id="88777-143">System.String</span></span>

### <span data-ttu-id="88777-144">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="88777-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="88777-145">輸出</span><span class="sxs-lookup"><span data-stu-id="88777-145">OUTPUTS</span></span>

### <span data-ttu-id="88777-146">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="88777-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="88777-147">筆記</span><span class="sxs-lookup"><span data-stu-id="88777-147">NOTES</span></span>

## <span data-ttu-id="88777-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="88777-148">RELATED LINKS</span></span>
