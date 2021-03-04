---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 08cde5aed74b194ede03f695eaf071d18467cb1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904454"
---
# <span data-ttu-id="2ce18-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="2ce18-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="2ce18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ce18-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce18-103">建立步驟。</span><span class="sxs-lookup"><span data-stu-id="2ce18-103">Creates a step.</span></span>

## <span data-ttu-id="2ce18-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ce18-104">SYNTAX</span></span>

### <span data-ttu-id="2ce18-105">請 (預設) </span><span class="sxs-lookup"><span data-stu-id="2ce18-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ce18-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="2ce18-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ce18-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="2ce18-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ce18-108">描述</span><span class="sxs-lookup"><span data-stu-id="2ce18-108">DESCRIPTION</span></span>
<span data-ttu-id="2ce18-109">**New-AzDeploymentManagerStep** Cmdlet 會建立可在推出時參照的部署步驟。</span><span class="sxs-lookup"><span data-stu-id="2ce18-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="2ce18-110">指定 *名稱\*\*、ResourceGroupName* 和必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="2ce18-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="2ce18-111">您可以在本地修改所返回的物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerStep步驟。</span><span class="sxs-lookup"><span data-stu-id="2ce18-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="2ce18-112">例子</span><span class="sxs-lookup"><span data-stu-id="2ce18-112">EXAMPLES</span></span>

### <span data-ttu-id="2ce18-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2ce18-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="2ce18-114">在 ContosoResourceGroup 中建立一個步驟，名稱為 ContosoService1WaitStep，而 US 中為資源的位置。</span><span class="sxs-lookup"><span data-stu-id="2ce18-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="2ce18-115">Duration 屬性提供推出前要等待的持續時間，然後執行下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="2ce18-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="2ce18-116">參數</span><span class="sxs-lookup"><span data-stu-id="2ce18-116">PARAMETERS</span></span>

### <span data-ttu-id="2ce18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce18-117">-DefaultProfile</span></span>
<span data-ttu-id="2ce18-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ce18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce18-119">-工期</span><span class="sxs-lookup"><span data-stu-id="2ce18-119">-Duration</span></span>
<span data-ttu-id="2ce18-120">以 ISO 8601 格式等待的工期。</span><span class="sxs-lookup"><span data-stu-id="2ce18-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="2ce18-121">例如：PT30M、PT1H</span><span class="sxs-lookup"><span data-stu-id="2ce18-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="2ce18-122">-HealthCheckProperties</span></span>
<span data-ttu-id="2ce18-123">健康狀態檢查屬性。</span><span class="sxs-lookup"><span data-stu-id="2ce18-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="2ce18-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="2ce18-125">定義健康狀態檢查屬性的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="2ce18-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-126">-位置</span><span class="sxs-lookup"><span data-stu-id="2ce18-126">-Location</span></span>
<span data-ttu-id="2ce18-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="2ce18-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ce18-128">-Name</span></span>
<span data-ttu-id="2ce18-129">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ce18-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce18-130">-ResourceGroupName</span></span>
<span data-ttu-id="2ce18-131">資源群組。</span><span class="sxs-lookup"><span data-stu-id="2ce18-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-132">-標記</span><span class="sxs-lookup"><span data-stu-id="2ce18-132">-Tag</span></span>
<span data-ttu-id="2ce18-133">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2ce18-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce18-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2ce18-134">-Confirm</span></span>
<span data-ttu-id="2ce18-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ce18-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ce18-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce18-136">-WhatIf</span></span>
<span data-ttu-id="2ce18-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ce18-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce18-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ce18-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ce18-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce18-139">CommonParameters</span></span>
<span data-ttu-id="2ce18-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ce18-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce18-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ce18-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce18-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2ce18-142">INPUTS</span></span>

### <span data-ttu-id="2ce18-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ce18-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ce18-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2ce18-144">OUTPUTS</span></span>

### <span data-ttu-id="2ce18-145">Microsoft.Azure.Commands.DeploymentManager.models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="2ce18-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="2ce18-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2ce18-146">NOTES</span></span>

## <span data-ttu-id="2ce18-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ce18-147">RELATED LINKS</span></span>
