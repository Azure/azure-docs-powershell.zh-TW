---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281595"
---
# <span data-ttu-id="b85d6-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b85d6-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="b85d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b85d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b85d6-103">將部署腳本執行的記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="b85d6-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b85d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b85d6-104">SYNTAX</span></span>

### <span data-ttu-id="b85d6-105">SaveDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b85d6-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b85d6-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="b85d6-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85d6-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="b85d6-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b85d6-108">說明</span><span class="sxs-lookup"><span data-stu-id="b85d6-108">DESCRIPTION</span></span>
<span data-ttu-id="b85d6-109">[ **儲存] AzDeploymentScriptLog** 會將部署腳本的執行記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="b85d6-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="b85d6-110">示例</span><span class="sxs-lookup"><span data-stu-id="b85d6-110">EXAMPLES</span></span>

### <span data-ttu-id="b85d6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b85d6-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="b85d6-112">以指定的名稱和資源群組儲存部署腳本記錄。</span><span class="sxs-lookup"><span data-stu-id="b85d6-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="b85d6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b85d6-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="b85d6-114">以指定的名稱和資源群組儲存部署腳本記錄的最後3行。</span><span class="sxs-lookup"><span data-stu-id="b85d6-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="b85d6-115">參數</span><span class="sxs-lookup"><span data-stu-id="b85d6-115">PARAMETERS</span></span>

### <span data-ttu-id="b85d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85d6-116">-DefaultProfile</span></span>
<span data-ttu-id="b85d6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b85d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85d6-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="b85d6-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="b85d6-119">[部署腳本 PowerShell] 物件。</span><span class="sxs-lookup"><span data-stu-id="b85d6-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="b85d6-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="b85d6-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="b85d6-121">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b85d6-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b85d6-122">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b85d6-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="b85d6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b85d6-123">-Force</span></span>
<span data-ttu-id="b85d6-124">強制覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="b85d6-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="b85d6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b85d6-125">-Name</span></span>
<span data-ttu-id="b85d6-126">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85d6-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="b85d6-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b85d6-127">-OutputPath</span></span>
<span data-ttu-id="b85d6-128">儲存部署腳本記錄的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="b85d6-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="b85d6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85d6-129">-ResourceGroupName</span></span>
<span data-ttu-id="b85d6-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b85d6-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b85d6-131">-尾</span><span class="sxs-lookup"><span data-stu-id="b85d6-131">-Tail</span></span>
<span data-ttu-id="b85d6-132">將輸出限制為最後 n 行</span><span class="sxs-lookup"><span data-stu-id="b85d6-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="b85d6-133">-確認</span><span class="sxs-lookup"><span data-stu-id="b85d6-133">-Confirm</span></span>
<span data-ttu-id="b85d6-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b85d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b85d6-135">-WhatIf</span></span>
<span data-ttu-id="b85d6-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b85d6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85d6-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b85d6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85d6-138">CommonParameters</span></span>
<span data-ttu-id="b85d6-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b85d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85d6-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b85d6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85d6-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b85d6-141">INPUTS</span></span>

### <span data-ttu-id="b85d6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="b85d6-142">System.String</span></span>

## <span data-ttu-id="b85d6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b85d6-143">OUTPUTS</span></span>

### <span data-ttu-id="b85d6-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="b85d6-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="b85d6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b85d6-145">NOTES</span></span>

## <span data-ttu-id="b85d6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b85d6-146">RELATED LINKS</span></span>
