---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622451"
---
# <span data-ttu-id="38c8e-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="38c8e-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="38c8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="38c8e-103">取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-103">Gets the service topology.</span></span>

## <span data-ttu-id="38c8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="38c8e-104">SYNTAX</span></span>

### <span data-ttu-id="38c8e-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="38c8e-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38c8e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c8e-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38c8e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="38c8e-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38c8e-108">說明</span><span class="sxs-lookup"><span data-stu-id="38c8e-108">DESCRIPTION</span></span>
<span data-ttu-id="38c8e-109">**AzDeploymentManagerServiceTopology** Cmdlet 會取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="38c8e-110">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerServiceTopology Cmdlet 將變更套用到拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="38c8e-111">依名稱和資源群組名稱指定服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="38c8e-112">或者，您也可以提供 ServiceTopology 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="38c8e-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="38c8e-113">示例</span><span class="sxs-lookup"><span data-stu-id="38c8e-113">EXAMPLES</span></span>

### <span data-ttu-id="38c8e-114">範例1</span><span class="sxs-lookup"><span data-stu-id="38c8e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="38c8e-115">這個命令會在 ContosoResourceGroup 中取得名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="38c8e-116">範例2：使用資源識別碼取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="38c8e-117">這個命令會在 ContosoResourceGroup 中取得名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="38c8e-118">範例3：使用服務拓朴物件取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="38c8e-119">這個命令會分別取得名稱和 ResourceGroup 與 $serviceTopologyObject 之 Name 和 ResourceGroupName 屬性相符的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="38c8e-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="38c8e-120">參數</span><span class="sxs-lookup"><span data-stu-id="38c8e-120">PARAMETERS</span></span>

### <span data-ttu-id="38c8e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c8e-121">-DefaultProfile</span></span>
<span data-ttu-id="38c8e-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38c8e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c8e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38c8e-123">-InputObject</span></span>
<span data-ttu-id="38c8e-124">[服務拓撲] 資源物件。</span><span class="sxs-lookup"><span data-stu-id="38c8e-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="38c8e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="38c8e-125">-Name</span></span>
<span data-ttu-id="38c8e-126">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="38c8e-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="38c8e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c8e-127">-ResourceGroupName</span></span>
<span data-ttu-id="38c8e-128">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="38c8e-128">The resource group.</span></span>

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

### <span data-ttu-id="38c8e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c8e-129">-ResourceId</span></span>
<span data-ttu-id="38c8e-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="38c8e-130">The resource identifier.</span></span>

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

### <span data-ttu-id="38c8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c8e-131">CommonParameters</span></span>
<span data-ttu-id="38c8e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38c8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c8e-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38c8e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c8e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="38c8e-134">INPUTS</span></span>

### <span data-ttu-id="38c8e-135">System.object</span><span class="sxs-lookup"><span data-stu-id="38c8e-135">System.String</span></span>

### <span data-ttu-id="38c8e-136">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="38c8e-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="38c8e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="38c8e-137">OUTPUTS</span></span>

### <span data-ttu-id="38c8e-138">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="38c8e-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="38c8e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="38c8e-139">NOTES</span></span>

## <span data-ttu-id="38c8e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="38c8e-140">RELATED LINKS</span></span>
