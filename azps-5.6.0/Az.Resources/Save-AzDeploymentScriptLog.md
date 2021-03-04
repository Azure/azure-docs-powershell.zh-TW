---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 876414b754a259d253dc56e5d92c570aa8f48318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913110"
---
# <span data-ttu-id="b92c5-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b92c5-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="b92c5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b92c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b92c5-103">將部署腳本執行記錄存到磁片。</span><span class="sxs-lookup"><span data-stu-id="b92c5-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b92c5-104">語法</span><span class="sxs-lookup"><span data-stu-id="b92c5-104">SYNTAX</span></span>

### <span data-ttu-id="b92c5-105">SaveDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b92c5-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b92c5-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="b92c5-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b92c5-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="b92c5-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b92c5-108">描述</span><span class="sxs-lookup"><span data-stu-id="b92c5-108">DESCRIPTION</span></span>
<span data-ttu-id="b92c5-109">**Save-AzDeploymentScriptLog** 會將部署腳本執行的記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="b92c5-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b92c5-110">例子</span><span class="sxs-lookup"><span data-stu-id="b92c5-110">EXAMPLES</span></span>

### <span data-ttu-id="b92c5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b92c5-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="b92c5-112">使用指定的名稱和資源群組來記錄部署腳本。</span><span class="sxs-lookup"><span data-stu-id="b92c5-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="b92c5-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b92c5-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="b92c5-114">將部署腳本的最後 3 行記錄與指定的名稱和資源群組一併保存。</span><span class="sxs-lookup"><span data-stu-id="b92c5-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="b92c5-115">參數</span><span class="sxs-lookup"><span data-stu-id="b92c5-115">PARAMETERS</span></span>

### <span data-ttu-id="b92c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92c5-116">-DefaultProfile</span></span>
<span data-ttu-id="b92c5-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b92c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b92c5-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="b92c5-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="b92c5-119">部署腳本 PowerShell 物件。</span><span class="sxs-lookup"><span data-stu-id="b92c5-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="b92c5-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="b92c5-121">部署腳本的完全合格的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b92c5-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b92c5-122">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b92c5-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-123">-強制</span><span class="sxs-lookup"><span data-stu-id="b92c5-123">-Force</span></span>
<span data-ttu-id="b92c5-124">強制覆寫現有檔案。</span><span class="sxs-lookup"><span data-stu-id="b92c5-124">Forces the overwrite of the existing file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b92c5-125">-Name</span></span>
<span data-ttu-id="b92c5-126">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92c5-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b92c5-127">-OutputPath</span></span>
<span data-ttu-id="b92c5-128">儲存部署腳本記錄之目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="b92c5-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b92c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="b92c5-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92c5-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="b92c5-131">-Tail</span></span>
<span data-ttu-id="b92c5-132">將輸出限制為最後 n 行</span><span class="sxs-lookup"><span data-stu-id="b92c5-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b92c5-133">-確認</span><span class="sxs-lookup"><span data-stu-id="b92c5-133">-Confirm</span></span>
<span data-ttu-id="b92c5-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b92c5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b92c5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b92c5-135">-WhatIf</span></span>
<span data-ttu-id="b92c5-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b92c5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b92c5-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b92c5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b92c5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92c5-138">CommonParameters</span></span>
<span data-ttu-id="b92c5-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b92c5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92c5-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b92c5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92c5-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b92c5-141">INPUTS</span></span>

### <span data-ttu-id="b92c5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b92c5-142">System.String</span></span>

## <span data-ttu-id="b92c5-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b92c5-143">OUTPUTS</span></span>

### <span data-ttu-id="b92c5-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="b92c5-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="b92c5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b92c5-145">NOTES</span></span>

## <span data-ttu-id="b92c5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b92c5-146">RELATED LINKS</span></span>
