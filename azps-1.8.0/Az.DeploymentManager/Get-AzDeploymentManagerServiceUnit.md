---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 607e094a03d43704057af80266a6f9f2b669d3b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622452"
---
# <span data-ttu-id="c7d25-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="c7d25-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="c7d25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7d25-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d25-103">取得服務單元。</span><span class="sxs-lookup"><span data-stu-id="c7d25-103">Gets the service unit.</span></span>

## <span data-ttu-id="c7d25-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7d25-104">SYNTAX</span></span>

### <span data-ttu-id="c7d25-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="c7d25-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d25-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="c7d25-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d25-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d25-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> [-ServiceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d25-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c7d25-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7d25-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c7d25-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d25-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d25-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7d25-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7d25-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ServiceUnitObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d25-112">說明</span><span class="sxs-lookup"><span data-stu-id="c7d25-112">DESCRIPTION</span></span>
<span data-ttu-id="c7d25-113">**AzDeploymentManagerServiceUnit** Cmdlet 會取得服務中的服務單元。</span><span class="sxs-lookup"><span data-stu-id="c7d25-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="c7d25-114">依名稱指定服務單位、定義所用的服務、服務拓朴名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7d25-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="c7d25-115">或者，您也可以提供 ServiceUnit 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="c7d25-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="c7d25-116">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerServiceUnit Cmdlet 將變更套用至服務單元。</span><span class="sxs-lookup"><span data-stu-id="c7d25-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="c7d25-117">示例</span><span class="sxs-lookup"><span data-stu-id="c7d25-117">EXAMPLES</span></span>

### <span data-ttu-id="c7d25-118">範例1</span><span class="sxs-lookup"><span data-stu-id="c7d25-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="c7d25-119">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓朴中，取得服務 ContosoService1 下的服務單元（名為 ContosoService1Storage）。</span><span class="sxs-lookup"><span data-stu-id="c7d25-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c7d25-120">範例2：使用資源識別碼取得服務單元。</span><span class="sxs-lookup"><span data-stu-id="c7d25-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="c7d25-121">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓朴中，取得服務 ContosoService1 下的服務單元（名為 ContosoService1Storage）。</span><span class="sxs-lookup"><span data-stu-id="c7d25-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c7d25-122">範例3：使用服務單元物件取得服務單元。</span><span class="sxs-lookup"><span data-stu-id="c7d25-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="c7d25-123">這個命令會分別取得 name、service name、service 拓朴名稱和 ResourceGroup 與 $serviceUnitObject 的名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務單位。</span><span class="sxs-lookup"><span data-stu-id="c7d25-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="c7d25-124">參數</span><span class="sxs-lookup"><span data-stu-id="c7d25-124">PARAMETERS</span></span>

### <span data-ttu-id="c7d25-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d25-125">-DefaultProfile</span></span>
<span data-ttu-id="c7d25-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7d25-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7d25-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7d25-127">-Name</span></span>
<span data-ttu-id="c7d25-128">服務單元的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7d25-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d25-129">-ResourceGroupName</span></span>
<span data-ttu-id="c7d25-130">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="c7d25-130">The resource group.</span></span>

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

### <span data-ttu-id="c7d25-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d25-131">-ResourceId</span></span>
<span data-ttu-id="c7d25-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7d25-132">The resource identifier.</span></span>

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

### <span data-ttu-id="c7d25-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7d25-133">-ServiceName</span></span>
<span data-ttu-id="c7d25-134">服務單元所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c7d25-134">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="c7d25-135">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="c7d25-135">-ServiceObject</span></span>
<span data-ttu-id="c7d25-136">應該在其中建立服務單元的服務物件。</span><span class="sxs-lookup"><span data-stu-id="c7d25-136">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c7d25-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d25-137">-ServiceResourceId</span></span>
<span data-ttu-id="c7d25-138">在其中建立服務單元的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7d25-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c7d25-139">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="c7d25-139">-ServiceTopologyName</span></span>
<span data-ttu-id="c7d25-140">服務單元所屬的服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7d25-140">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="c7d25-141">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c7d25-141">-ServiceTopologyObject</span></span>
<span data-ttu-id="c7d25-142">應該在其中建立服務單元的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="c7d25-142">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c7d25-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d25-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="c7d25-144">在其中建立服務單元的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7d25-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="c7d25-145">-ServiceUnitObject</span><span class="sxs-lookup"><span data-stu-id="c7d25-145">-ServiceUnitObject</span></span>
<span data-ttu-id="c7d25-146">[服務單元] 資源物件。</span><span class="sxs-lookup"><span data-stu-id="c7d25-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="c7d25-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d25-147">CommonParameters</span></span>
<span data-ttu-id="c7d25-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7d25-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d25-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7d25-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d25-150">輸入</span><span class="sxs-lookup"><span data-stu-id="c7d25-150">INPUTS</span></span>

### <span data-ttu-id="c7d25-151">System.object</span><span class="sxs-lookup"><span data-stu-id="c7d25-151">System.String</span></span>

### <span data-ttu-id="c7d25-152">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="c7d25-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c7d25-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c7d25-153">OUTPUTS</span></span>

### <span data-ttu-id="c7d25-154">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="c7d25-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c7d25-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c7d25-155">NOTES</span></span>

## <span data-ttu-id="c7d25-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7d25-156">RELATED LINKS</span></span>
