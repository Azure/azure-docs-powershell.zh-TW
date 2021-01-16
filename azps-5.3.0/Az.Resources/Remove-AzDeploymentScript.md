---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435404"
---
# <span data-ttu-id="31415-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="31415-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="31415-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31415-102">SYNOPSIS</span></span>
<span data-ttu-id="31415-103">移除部署腳本及其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="31415-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="31415-104">句法</span><span class="sxs-lookup"><span data-stu-id="31415-104">SYNTAX</span></span>

### <span data-ttu-id="31415-105">RemoveDeploymentScriptLogByName (預設) </span><span class="sxs-lookup"><span data-stu-id="31415-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31415-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="31415-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31415-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="31415-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31415-108">說明</span><span class="sxs-lookup"><span data-stu-id="31415-108">DESCRIPTION</span></span>
<span data-ttu-id="31415-109">**AzDeploymentScript** Cmdlet 會移除部署腳本及其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="31415-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="31415-110">示例</span><span class="sxs-lookup"><span data-stu-id="31415-110">EXAMPLES</span></span>

### <span data-ttu-id="31415-111">範例1</span><span class="sxs-lookup"><span data-stu-id="31415-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="31415-112">刪除資源群組 DS-TestRG 中名稱為 MyDeploymentScript 的部署腳本。</span><span class="sxs-lookup"><span data-stu-id="31415-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="31415-113">參數</span><span class="sxs-lookup"><span data-stu-id="31415-113">PARAMETERS</span></span>

### <span data-ttu-id="31415-114">-確認</span><span class="sxs-lookup"><span data-stu-id="31415-114">-Confirm</span></span>
<span data-ttu-id="31415-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="31415-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31415-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31415-116">-DefaultProfile</span></span>
<span data-ttu-id="31415-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31415-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31415-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="31415-118">-Id</span></span>
<span data-ttu-id="31415-119">部署腳本的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="31415-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="31415-120">範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="31415-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="31415-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31415-121">-InputObject</span></span>
<span data-ttu-id="31415-122">[部署腳本 PowerShell] 物件。</span><span class="sxs-lookup"><span data-stu-id="31415-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="31415-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="31415-123">-Name</span></span>
<span data-ttu-id="31415-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31415-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="31415-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31415-125">-PassThru</span></span>
<span data-ttu-id="31415-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="31415-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="31415-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31415-127">-ResourceGroupName</span></span>
<span data-ttu-id="31415-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31415-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="31415-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31415-129">-WhatIf</span></span>
<span data-ttu-id="31415-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31415-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31415-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31415-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31415-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31415-132">CommonParameters</span></span>
<span data-ttu-id="31415-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31415-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="31415-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31415-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31415-135">輸入</span><span class="sxs-lookup"><span data-stu-id="31415-135">INPUTS</span></span>

### <span data-ttu-id="31415-136">System.object</span><span class="sxs-lookup"><span data-stu-id="31415-136">System.String</span></span>

### <span data-ttu-id="31415-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="31415-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="31415-138">輸出</span><span class="sxs-lookup"><span data-stu-id="31415-138">OUTPUTS</span></span>

### <span data-ttu-id="31415-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="31415-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="31415-140">筆記</span><span class="sxs-lookup"><span data-stu-id="31415-140">NOTES</span></span>

## <span data-ttu-id="31415-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="31415-141">RELATED LINKS</span></span>