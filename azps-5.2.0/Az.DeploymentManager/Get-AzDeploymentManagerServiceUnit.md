---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281180"
---
# <span data-ttu-id="149e0-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="149e0-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="149e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="149e0-102">SYNOPSIS</span></span>
<span data-ttu-id="149e0-103">取得服務單元。</span><span class="sxs-lookup"><span data-stu-id="149e0-103">Gets the service unit.</span></span>

## <span data-ttu-id="149e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="149e0-104">SYNTAX</span></span>

### <span data-ttu-id="149e0-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="149e0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="149e0-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="149e0-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="149e0-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="149e0-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="149e0-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="149e0-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="149e0-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="149e0-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="149e0-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="149e0-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="149e0-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="149e0-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="149e0-112">說明</span><span class="sxs-lookup"><span data-stu-id="149e0-112">DESCRIPTION</span></span>
<span data-ttu-id="149e0-113">**AzDeploymentManagerServiceUnit** Cmdlet 會取得服務中的服務單元。</span><span class="sxs-lookup"><span data-stu-id="149e0-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="149e0-114">依名稱指定服務單位、定義所用的服務、服務拓朴名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="149e0-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="149e0-115">或者，您也可以提供 ServiceUnit 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="149e0-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="149e0-116">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerServiceUnit Cmdlet 將變更套用至服務單元。</span><span class="sxs-lookup"><span data-stu-id="149e0-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="149e0-117">示例</span><span class="sxs-lookup"><span data-stu-id="149e0-117">EXAMPLES</span></span>

### <span data-ttu-id="149e0-118">範例1</span><span class="sxs-lookup"><span data-stu-id="149e0-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="149e0-119">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓朴中，取得服務 ContosoService1 下的服務單元（名為 ContosoService1Storage）。</span><span class="sxs-lookup"><span data-stu-id="149e0-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="149e0-120">範例2：使用資源識別碼取得服務單元。</span><span class="sxs-lookup"><span data-stu-id="149e0-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="149e0-121">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓朴中，取得服務 ContosoService1 下的服務單元（名為 ContosoService1Storage）。</span><span class="sxs-lookup"><span data-stu-id="149e0-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="149e0-122">範例3：使用服務單元物件取得服務單元。</span><span class="sxs-lookup"><span data-stu-id="149e0-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="149e0-123">這個命令會分別取得 name、service name、service 拓朴名稱和 ResourceGroup 與 $serviceUnitObject 的名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務單位。</span><span class="sxs-lookup"><span data-stu-id="149e0-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="149e0-124">參數</span><span class="sxs-lookup"><span data-stu-id="149e0-124">PARAMETERS</span></span>

### <span data-ttu-id="149e0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149e0-125">-DefaultProfile</span></span>
<span data-ttu-id="149e0-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="149e0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="149e0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="149e0-127">-InputObject</span></span>
<span data-ttu-id="149e0-128">[服務單元] 資源物件。</span><span class="sxs-lookup"><span data-stu-id="149e0-128">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="149e0-129">-Name</span></span>
<span data-ttu-id="149e0-130">服務單元的名稱。</span><span class="sxs-lookup"><span data-stu-id="149e0-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="149e0-131">-ResourceGroupName</span></span>
<span data-ttu-id="149e0-132">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="149e0-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="149e0-133">-ResourceId</span></span>
<span data-ttu-id="149e0-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="149e0-134">The resource identifier.</span></span>

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

### <span data-ttu-id="149e0-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="149e0-135">-ServiceName</span></span>
<span data-ttu-id="149e0-136">服務單元所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="149e0-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="149e0-137">-ServiceObject</span></span>
<span data-ttu-id="149e0-138">應該在其中建立服務單元的服務物件。</span><span class="sxs-lookup"><span data-stu-id="149e0-138">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="149e0-139">-ServiceResourceId</span></span>
<span data-ttu-id="149e0-140">在其中建立服務單元的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="149e0-140">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="149e0-141">-ServiceTopologyName</span></span>
<span data-ttu-id="149e0-142">服務單元所屬的服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="149e0-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="149e0-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="149e0-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="149e0-144">應該在其中建立服務單元的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="149e0-144">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="149e0-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="149e0-146">在其中建立服務單元的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="149e0-146">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149e0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149e0-147">CommonParameters</span></span>
<span data-ttu-id="149e0-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="149e0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149e0-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="149e0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149e0-150">輸入</span><span class="sxs-lookup"><span data-stu-id="149e0-150">INPUTS</span></span>

### <span data-ttu-id="149e0-151">System.object</span><span class="sxs-lookup"><span data-stu-id="149e0-151">System.String</span></span>

### <span data-ttu-id="149e0-152">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="149e0-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="149e0-153">輸出</span><span class="sxs-lookup"><span data-stu-id="149e0-153">OUTPUTS</span></span>

### <span data-ttu-id="149e0-154">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="149e0-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="149e0-155">筆記</span><span class="sxs-lookup"><span data-stu-id="149e0-155">NOTES</span></span>

## <span data-ttu-id="149e0-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="149e0-156">RELATED LINKS</span></span>
