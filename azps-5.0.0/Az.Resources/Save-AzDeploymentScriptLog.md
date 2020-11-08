---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141266"
---
# <span data-ttu-id="1ab31-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="1ab31-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="1ab31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ab31-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab31-103">將部署腳本執行的記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="1ab31-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="1ab31-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ab31-104">SYNTAX</span></span>

### <span data-ttu-id="1ab31-105">SaveDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="1ab31-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ab31-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab31-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab31-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ab31-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ab31-108">說明</span><span class="sxs-lookup"><span data-stu-id="1ab31-108">DESCRIPTION</span></span>
<span data-ttu-id="1ab31-109">[ **儲存] AzDeploymentScriptLog** 會將部署腳本的執行記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="1ab31-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="1ab31-110">示例</span><span class="sxs-lookup"><span data-stu-id="1ab31-110">EXAMPLES</span></span>

### <span data-ttu-id="1ab31-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1ab31-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="1ab31-112">以指定的名稱和資源群組儲存部署腳本記錄。</span><span class="sxs-lookup"><span data-stu-id="1ab31-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="1ab31-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1ab31-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="1ab31-114">以指定的名稱和資源群組儲存部署腳本記錄的最後3行。</span><span class="sxs-lookup"><span data-stu-id="1ab31-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="1ab31-115">參數</span><span class="sxs-lookup"><span data-stu-id="1ab31-115">PARAMETERS</span></span>

### <span data-ttu-id="1ab31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab31-116">-DefaultProfile</span></span>
<span data-ttu-id="1ab31-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ab31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ab31-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="1ab31-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="1ab31-119">[部署腳本 PowerShell] 物件。</span><span class="sxs-lookup"><span data-stu-id="1ab31-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="1ab31-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab31-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="1ab31-121">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ab31-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="1ab31-122">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="1ab31-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="1ab31-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1ab31-123">-Force</span></span>
<span data-ttu-id="1ab31-124">強制覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="1ab31-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="1ab31-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ab31-125">-Name</span></span>
<span data-ttu-id="1ab31-126">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ab31-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="1ab31-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1ab31-127">-OutputPath</span></span>
<span data-ttu-id="1ab31-128">儲存部署腳本記錄的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="1ab31-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="1ab31-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab31-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ab31-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ab31-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ab31-131">-尾</span><span class="sxs-lookup"><span data-stu-id="1ab31-131">-Tail</span></span>
<span data-ttu-id="1ab31-132">將輸出限制為最後 n 行</span><span class="sxs-lookup"><span data-stu-id="1ab31-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="1ab31-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1ab31-133">-Confirm</span></span>
<span data-ttu-id="1ab31-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ab31-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab31-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab31-135">-WhatIf</span></span>
<span data-ttu-id="1ab31-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ab31-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab31-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ab31-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab31-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab31-138">CommonParameters</span></span>
<span data-ttu-id="1ab31-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ab31-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab31-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1ab31-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab31-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1ab31-141">INPUTS</span></span>

### <span data-ttu-id="1ab31-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1ab31-142">System.String</span></span>

## <span data-ttu-id="1ab31-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1ab31-143">OUTPUTS</span></span>

### <span data-ttu-id="1ab31-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="1ab31-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="1ab31-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1ab31-145">NOTES</span></span>

## <span data-ttu-id="1ab31-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ab31-146">RELATED LINKS</span></span>
