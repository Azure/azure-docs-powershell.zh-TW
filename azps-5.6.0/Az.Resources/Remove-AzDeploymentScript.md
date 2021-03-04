---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 813291fd0014665958dbee85be36060801b3e569
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908038"
---
# <span data-ttu-id="1e5e8-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1e5e8-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="1e5e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1e5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5e8-103">移除部署腳本及其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="1e5e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="1e5e8-104">SYNTAX</span></span>

### <span data-ttu-id="1e5e8-105">RemoveDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="1e5e8-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e5e8-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e5e8-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e5e8-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e5e8-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e5e8-108">描述</span><span class="sxs-lookup"><span data-stu-id="1e5e8-108">DESCRIPTION</span></span>
<span data-ttu-id="1e5e8-109">**Remove-AzDeploymentScript** Cmdlet 會移除部署腳本及其相關資源。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="1e5e8-110">例子</span><span class="sxs-lookup"><span data-stu-id="1e5e8-110">EXAMPLES</span></span>

### <span data-ttu-id="1e5e8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1e5e8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="1e5e8-112">刪除資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="1e5e8-113">參數</span><span class="sxs-lookup"><span data-stu-id="1e5e8-113">PARAMETERS</span></span>

### <span data-ttu-id="1e5e8-114">-確認</span><span class="sxs-lookup"><span data-stu-id="1e5e8-114">-Confirm</span></span>
<span data-ttu-id="1e5e8-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5e8-116">-DefaultProfile</span></span>
<span data-ttu-id="1e5e8-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e5e8-118">-Id</span><span class="sxs-lookup"><span data-stu-id="1e5e8-118">-Id</span></span>
<span data-ttu-id="1e5e8-119">部署腳本的完全合格的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="1e5e8-120">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="1e5e8-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e5e8-121">-InputObject</span></span>
<span data-ttu-id="1e5e8-122">部署腳本 PowerShell 物件。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e5e8-123">-Name</span></span>
<span data-ttu-id="1e5e8-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e5e8-125">-PassThru</span></span>
<span data-ttu-id="1e5e8-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1e5e8-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1e5e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e5e8-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5e8-129">-WhatIf</span></span>
<span data-ttu-id="1e5e8-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5e8-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5e8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5e8-132">CommonParameters</span></span>
<span data-ttu-id="1e5e8-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1e5e8-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1e5e8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5e8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1e5e8-135">INPUTS</span></span>

### <span data-ttu-id="1e5e8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1e5e8-136">System.String</span></span>

### <span data-ttu-id="1e5e8-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1e5e8-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1e5e8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1e5e8-138">OUTPUTS</span></span>

### <span data-ttu-id="1e5e8-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1e5e8-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1e5e8-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1e5e8-140">NOTES</span></span>

## <span data-ttu-id="1e5e8-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e5e8-141">RELATED LINKS</span></span>