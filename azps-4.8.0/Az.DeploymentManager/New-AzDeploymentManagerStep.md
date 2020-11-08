---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969248"
---
# <span data-ttu-id="90c8e-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="90c8e-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="90c8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="90c8e-103">建立步驟。</span><span class="sxs-lookup"><span data-stu-id="90c8e-103">Creates a step.</span></span>

## <span data-ttu-id="90c8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="90c8e-104">SYNTAX</span></span>

### <span data-ttu-id="90c8e-105">等待 (預設) </span><span class="sxs-lookup"><span data-stu-id="90c8e-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c8e-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="90c8e-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c8e-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="90c8e-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c8e-108">說明</span><span class="sxs-lookup"><span data-stu-id="90c8e-108">DESCRIPTION</span></span>
<span data-ttu-id="90c8e-109">**新的-AzDeploymentManagerStep** Cmdlet 會建立可在 [部署] 中參考的部署步驟。</span><span class="sxs-lookup"><span data-stu-id="90c8e-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="90c8e-110">指定 *Name* 、 *ResourceGroupName* 和 required 屬性。</span><span class="sxs-lookup"><span data-stu-id="90c8e-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="90c8e-111">您可以在本機修改傳回的物件，然後使用 Set-AzDeploymentManagerStep Cmdlet 將變更套用至步驟。</span><span class="sxs-lookup"><span data-stu-id="90c8e-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="90c8e-112">示例</span><span class="sxs-lookup"><span data-stu-id="90c8e-112">EXAMPLES</span></span>

### <span data-ttu-id="90c8e-113">範例1</span><span class="sxs-lookup"><span data-stu-id="90c8e-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="90c8e-114">在 ContosoResourceGroup 中建立一個名稱為 ContosoService1WaitStep 的步驟，並將其設為資源的位置。</span><span class="sxs-lookup"><span data-stu-id="90c8e-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="90c8e-115">Duration 屬性提供在執行下一個步驟之前，推出的持續時間。</span><span class="sxs-lookup"><span data-stu-id="90c8e-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="90c8e-116">參數</span><span class="sxs-lookup"><span data-stu-id="90c8e-116">PARAMETERS</span></span>

### <span data-ttu-id="90c8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c8e-117">-DefaultProfile</span></span>
<span data-ttu-id="90c8e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90c8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c8e-119">-工期</span><span class="sxs-lookup"><span data-stu-id="90c8e-119">-Duration</span></span>
<span data-ttu-id="90c8e-120">以 ISO 8601 格式等候的持續時間。</span><span class="sxs-lookup"><span data-stu-id="90c8e-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="90c8e-121">例如： PT30M、PT1H</span><span class="sxs-lookup"><span data-stu-id="90c8e-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="90c8e-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="90c8e-122">-HealthCheckProperties</span></span>
<span data-ttu-id="90c8e-123">[狀況檢查] 屬性。</span><span class="sxs-lookup"><span data-stu-id="90c8e-123">The health check properties.</span></span>

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

### <span data-ttu-id="90c8e-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="90c8e-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="90c8e-125">定義健康情況檢查屬性之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="90c8e-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="90c8e-126">-位置</span><span class="sxs-lookup"><span data-stu-id="90c8e-126">-Location</span></span>
<span data-ttu-id="90c8e-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="90c8e-127">The location of the resource.</span></span>

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

### <span data-ttu-id="90c8e-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="90c8e-128">-Name</span></span>
<span data-ttu-id="90c8e-129">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="90c8e-129">The name of the step.</span></span>

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

### <span data-ttu-id="90c8e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c8e-130">-ResourceGroupName</span></span>
<span data-ttu-id="90c8e-131">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="90c8e-131">The resource group.</span></span>

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

### <span data-ttu-id="90c8e-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="90c8e-132">-Tag</span></span>
<span data-ttu-id="90c8e-133">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="90c8e-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="90c8e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="90c8e-134">-Confirm</span></span>
<span data-ttu-id="90c8e-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90c8e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c8e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c8e-136">-WhatIf</span></span>
<span data-ttu-id="90c8e-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90c8e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c8e-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90c8e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c8e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c8e-139">CommonParameters</span></span>
<span data-ttu-id="90c8e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90c8e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c8e-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90c8e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c8e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="90c8e-142">INPUTS</span></span>

### <span data-ttu-id="90c8e-143">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90c8e-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90c8e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="90c8e-144">OUTPUTS</span></span>

### <span data-ttu-id="90c8e-145">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="90c8e-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="90c8e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="90c8e-146">NOTES</span></span>

## <span data-ttu-id="90c8e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="90c8e-147">RELATED LINKS</span></span>
