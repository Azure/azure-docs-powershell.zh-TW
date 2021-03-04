---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: 53458d53dd6d8b3f698dc51fc6b1463c9a9134e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905513"
---
# <span data-ttu-id="3181b-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="3181b-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="3181b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3181b-102">SYNOPSIS</span></span>
<span data-ttu-id="3181b-103">開始推出。</span><span class="sxs-lookup"><span data-stu-id="3181b-103">Gets the rollout.</span></span>

## <span data-ttu-id="3181b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3181b-104">SYNTAX</span></span>

### <span data-ttu-id="3181b-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="3181b-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3181b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3181b-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3181b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3181b-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3181b-108">描述</span><span class="sxs-lookup"><span data-stu-id="3181b-108">DESCRIPTION</span></span>
<span data-ttu-id="3181b-109">**Get-AzDeploymentManagerRollout** Cmdlet 會推出，並會返回代表該推出的物件，並包含推出進度的所有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3181b-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="3181b-110">根據部署名稱和資源組名來指定部署。</span><span class="sxs-lookup"><span data-stu-id="3181b-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="3181b-111">或者，您也可以提供部署物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3181b-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="3181b-112">所退回的推出物件包含已部署的服務、服務單位和步驟，以及進行中的服務、服務單位和步驟。</span><span class="sxs-lookup"><span data-stu-id="3181b-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="3181b-113">尚未部署的則不在回應中。</span><span class="sxs-lookup"><span data-stu-id="3181b-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="3181b-114">例子</span><span class="sxs-lookup"><span data-stu-id="3181b-114">EXAMPLES</span></span>

### <span data-ttu-id="3181b-115">範例 1 取得推出</span><span class="sxs-lookup"><span data-stu-id="3181b-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="3181b-116">此命令在 ContosoResourceGroup 中推出名為 ContosoRollout。</span><span class="sxs-lookup"><span data-stu-id="3181b-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="3181b-117">範例 2 取得及顯示推出詳細資料</span><span class="sxs-lookup"><span data-stu-id="3181b-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="3181b-118">此命令在 ContosoResourceGroup 中推出名為 ContosoRollout。</span><span class="sxs-lookup"><span data-stu-id="3181b-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="3181b-119">-Verbose 切換會以階層式顯示所有推出詳細資料;顯示服務、ServiceUnits，以及每個 ServiceUnit 下的步驟，以及每個步驟的情境資訊，以呈現推出時呈現的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="3181b-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="3181b-120">範例 3：使用資源識別碼進行部署</span><span class="sxs-lookup"><span data-stu-id="3181b-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="3181b-121">此命令在 ContosoResourceGroup 中推出名為 ContosoRollout。</span><span class="sxs-lookup"><span data-stu-id="3181b-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3181b-122">範例 4：使用推出物件進行部署。</span><span class="sxs-lookup"><span data-stu-id="3181b-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="3181b-123">此命令會推出其名稱與 ResourceGroup 分別符合其名稱及$rolloutObject屬性。</span><span class="sxs-lookup"><span data-stu-id="3181b-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="3181b-124">參數</span><span class="sxs-lookup"><span data-stu-id="3181b-124">PARAMETERS</span></span>

### <span data-ttu-id="3181b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3181b-125">-DefaultProfile</span></span>
<span data-ttu-id="3181b-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3181b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3181b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3181b-127">-InputObject</span></span>
<span data-ttu-id="3181b-128">推出物件。</span><span class="sxs-lookup"><span data-stu-id="3181b-128">Rollout object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3181b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="3181b-129">-Name</span></span>
<span data-ttu-id="3181b-130">推出名稱。</span><span class="sxs-lookup"><span data-stu-id="3181b-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="3181b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3181b-131">-ResourceGroupName</span></span>
<span data-ttu-id="3181b-132">資源群組。</span><span class="sxs-lookup"><span data-stu-id="3181b-132">The resource group.</span></span>

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

### <span data-ttu-id="3181b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3181b-133">-ResourceId</span></span>
<span data-ttu-id="3181b-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3181b-134">The resource identifier.</span></span>

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

### <span data-ttu-id="3181b-135">-重試Attempt</span><span class="sxs-lookup"><span data-stu-id="3181b-135">-RetryAttempt</span></span>
<span data-ttu-id="3181b-136">重新嘗試推出。</span><span class="sxs-lookup"><span data-stu-id="3181b-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3181b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3181b-137">CommonParameters</span></span>
<span data-ttu-id="3181b-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3181b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3181b-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3181b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3181b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3181b-140">INPUTS</span></span>

### <span data-ttu-id="3181b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3181b-141">System.String</span></span>

### <span data-ttu-id="3181b-142">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3181b-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3181b-143">Microsoft.Azure.Commands.DeploymentManager.models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="3181b-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="3181b-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3181b-144">OUTPUTS</span></span>

### <span data-ttu-id="3181b-145">Microsoft.Azure.Commands.DeploymentManager.models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="3181b-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="3181b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3181b-146">NOTES</span></span>

## <span data-ttu-id="3181b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3181b-147">RELATED LINKS</span></span>
