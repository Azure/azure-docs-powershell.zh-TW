---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c02a88cdb550e1ec9cb343b286d3211045873820
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909105"
---
# <span data-ttu-id="88104-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="88104-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="88104-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88104-102">SYNOPSIS</span></span>
<span data-ttu-id="88104-103">獲得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-103">Gets the service topology.</span></span>

## <span data-ttu-id="88104-104">語法</span><span class="sxs-lookup"><span data-stu-id="88104-104">SYNTAX</span></span>

### <span data-ttu-id="88104-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="88104-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88104-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="88104-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88104-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="88104-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88104-108">描述</span><span class="sxs-lookup"><span data-stu-id="88104-108">DESCRIPTION</span></span>
<span data-ttu-id="88104-109">**Get-AzDeploymentManagerServiceTop以 Cmdlet** 取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="88104-110">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerServiceTopology拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="88104-111">根據服務拓撲的名稱和資源組名來指定服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="88104-112">或者，您也可以提供 ServiceTopology 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="88104-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="88104-113">例子</span><span class="sxs-lookup"><span data-stu-id="88104-113">EXAMPLES</span></span>

### <span data-ttu-id="88104-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="88104-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="88104-115">此命令會獲得 ContosoResourceGroup 中名為 ContosoServiceTopsource 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="88104-116">範例 2：使用資源識別碼取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="88104-117">此命令會獲得 ContosoResourceGroup 中名為 ContosoServiceTopsource 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="88104-118">範例 3：使用服務拓撲物件取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="88104-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="88104-119">此命令會獲得服務拓撲，其名稱和資源組會分別符合 $serviceTopologyObject 的名稱和 ResourceGroupName 屬性。</span><span class="sxs-lookup"><span data-stu-id="88104-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="88104-120">參數</span><span class="sxs-lookup"><span data-stu-id="88104-120">PARAMETERS</span></span>

### <span data-ttu-id="88104-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88104-121">-DefaultProfile</span></span>
<span data-ttu-id="88104-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88104-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88104-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88104-123">-InputObject</span></span>
<span data-ttu-id="88104-124">服務拓撲資源物件。</span><span class="sxs-lookup"><span data-stu-id="88104-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="88104-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="88104-125">-Name</span></span>
<span data-ttu-id="88104-126">服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="88104-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88104-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88104-127">-ResourceGroupName</span></span>
<span data-ttu-id="88104-128">資源群組。</span><span class="sxs-lookup"><span data-stu-id="88104-128">The resource group.</span></span>

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

### <span data-ttu-id="88104-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88104-129">-ResourceId</span></span>
<span data-ttu-id="88104-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="88104-130">The resource identifier.</span></span>

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

### <span data-ttu-id="88104-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88104-131">CommonParameters</span></span>
<span data-ttu-id="88104-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88104-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88104-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88104-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88104-134">輸入</span><span class="sxs-lookup"><span data-stu-id="88104-134">INPUTS</span></span>

### <span data-ttu-id="88104-135">System.String</span><span class="sxs-lookup"><span data-stu-id="88104-135">System.String</span></span>

### <span data-ttu-id="88104-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopserviceserviceResource</span><span class="sxs-lookup"><span data-stu-id="88104-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="88104-137">輸出</span><span class="sxs-lookup"><span data-stu-id="88104-137">OUTPUTS</span></span>

### <span data-ttu-id="88104-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopserviceserviceResource</span><span class="sxs-lookup"><span data-stu-id="88104-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="88104-139">筆記</span><span class="sxs-lookup"><span data-stu-id="88104-139">NOTES</span></span>

## <span data-ttu-id="88104-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="88104-140">RELATED LINKS</span></span>
