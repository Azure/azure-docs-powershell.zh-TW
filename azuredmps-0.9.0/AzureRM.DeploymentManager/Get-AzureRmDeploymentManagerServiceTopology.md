---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443516"
---
# <span data-ttu-id="dabe2-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="dabe2-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="dabe2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dabe2-102">SYNOPSIS</span></span>
<span data-ttu-id="dabe2-103">取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-103">Gets a service topology.</span></span>

## <span data-ttu-id="dabe2-104">句法</span><span class="sxs-lookup"><span data-stu-id="dabe2-104">SYNTAX</span></span>

### <span data-ttu-id="dabe2-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="dabe2-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabe2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dabe2-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dabe2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dabe2-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dabe2-108">說明</span><span class="sxs-lookup"><span data-stu-id="dabe2-108">DESCRIPTION</span></span>
<span data-ttu-id="dabe2-109">**AzureRmDeploymentManagerServiceTopology** Cmdlet 會取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="dabe2-110">您可以在本機修改這個物件，然後使用 Set-AzureRmDeploymentManagerServiceTopology Cmdlet 將變更套用到拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="dabe2-111">依名稱和資源群組名稱指定服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="dabe2-112">或者，您也可以提供 ServiceTopology 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="dabe2-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="dabe2-113">示例</span><span class="sxs-lookup"><span data-stu-id="dabe2-113">EXAMPLES</span></span>

### <span data-ttu-id="dabe2-114">範例1</span><span class="sxs-lookup"><span data-stu-id="dabe2-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="dabe2-115">這個命令會在 ContosoResourceGroup 中取得名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="dabe2-116">範例2：使用資源識別碼取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="dabe2-117">這個命令會在 ContosoResourceGroup 中取得名為 ContosoServiceTopology 的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="dabe2-118">範例3：使用服務拓朴物件取得服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="dabe2-119">這個命令會分別取得名稱和 ResourceGroup 與 $serviceTopologyObject 之 Name 和 ResourceGroupName 屬性相符的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="dabe2-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="dabe2-120">參數</span><span class="sxs-lookup"><span data-stu-id="dabe2-120">PARAMETERS</span></span>

### <span data-ttu-id="dabe2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabe2-121">-DefaultProfile</span></span>
<span data-ttu-id="dabe2-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dabe2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dabe2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="dabe2-123">-Name</span></span>
<span data-ttu-id="dabe2-124">服務拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="dabe2-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="dabe2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabe2-125">-ResourceGroupName</span></span>
<span data-ttu-id="dabe2-126">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="dabe2-126">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabe2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dabe2-127">-ResourceId</span></span>
<span data-ttu-id="dabe2-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dabe2-128">The resource identifier.</span></span>

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

### <span data-ttu-id="dabe2-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="dabe2-129">-ServiceTopology</span></span>
<span data-ttu-id="dabe2-130">[服務拓撲] 資源物件。</span><span class="sxs-lookup"><span data-stu-id="dabe2-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="dabe2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabe2-131">CommonParameters</span></span>
<span data-ttu-id="dabe2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dabe2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabe2-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dabe2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabe2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="dabe2-134">INPUTS</span></span>

### <span data-ttu-id="dabe2-135">所有</span><span class="sxs-lookup"><span data-stu-id="dabe2-135">None</span></span>

## <span data-ttu-id="dabe2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="dabe2-136">OUTPUTS</span></span>

### <span data-ttu-id="dabe2-137">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="dabe2-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="dabe2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="dabe2-138">NOTES</span></span>

## <span data-ttu-id="dabe2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="dabe2-139">RELATED LINKS</span></span>

[<span data-ttu-id="dabe2-140">新-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="dabe2-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="dabe2-141">移除-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="dabe2-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="dabe2-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="dabe2-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)