---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957729"
---
# <span data-ttu-id="99cb0-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="99cb0-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="99cb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="99cb0-103">將部署腳本執行的記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="99cb0-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="99cb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="99cb0-104">SYNTAX</span></span>

### <span data-ttu-id="99cb0-105">SaveDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="99cb0-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99cb0-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="99cb0-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99cb0-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="99cb0-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99cb0-108">說明</span><span class="sxs-lookup"><span data-stu-id="99cb0-108">DESCRIPTION</span></span>
<span data-ttu-id="99cb0-109">[ **儲存] AzDeploymentScriptLog** 會將部署腳本的執行記錄儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="99cb0-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="99cb0-110">示例</span><span class="sxs-lookup"><span data-stu-id="99cb0-110">EXAMPLES</span></span>

### <span data-ttu-id="99cb0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="99cb0-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="99cb0-112">以指定的名稱和資源群組儲存部署腳本記錄。</span><span class="sxs-lookup"><span data-stu-id="99cb0-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="99cb0-113">參數</span><span class="sxs-lookup"><span data-stu-id="99cb0-113">PARAMETERS</span></span>

### <span data-ttu-id="99cb0-114">-確認</span><span class="sxs-lookup"><span data-stu-id="99cb0-114">-Confirm</span></span>
<span data-ttu-id="99cb0-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99cb0-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cb0-116">-DefaultProfile</span></span>
<span data-ttu-id="99cb0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99cb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="99cb0-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="99cb0-119">[部署腳本 PowerShell] 物件。</span><span class="sxs-lookup"><span data-stu-id="99cb0-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="99cb0-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="99cb0-121">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="99cb0-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="99cb0-122">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="99cb0-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="99cb0-123">-Force</span></span>
<span data-ttu-id="99cb0-124">強制覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb0-124">Forces the overwrite of the existing file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="99cb0-125">-Name</span></span>
<span data-ttu-id="99cb0-126">部署腳本的名稱。</span><span class="sxs-lookup"><span data-stu-id="99cb0-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="99cb0-127">-OutputPath</span></span>
<span data-ttu-id="99cb0-128">儲存部署腳本記錄的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="99cb0-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99cb0-129">-ResourceGroupName</span></span>
<span data-ttu-id="99cb0-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99cb0-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99cb0-131">-WhatIf</span></span>
<span data-ttu-id="99cb0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99cb0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99cb0-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99cb0-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cb0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cb0-134">CommonParameters</span></span>
<span data-ttu-id="99cb0-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99cb0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99cb0-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99cb0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cb0-137">輸入</span><span class="sxs-lookup"><span data-stu-id="99cb0-137">INPUTS</span></span>

### <span data-ttu-id="99cb0-138">System.object</span><span class="sxs-lookup"><span data-stu-id="99cb0-138">System.String</span></span>

## <span data-ttu-id="99cb0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="99cb0-139">OUTPUTS</span></span>

### <span data-ttu-id="99cb0-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="99cb0-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="99cb0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="99cb0-141">NOTES</span></span>

## <span data-ttu-id="99cb0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="99cb0-142">RELATED LINKS</span></span>
