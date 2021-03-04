---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 64ed7e109877912d7a74937e6bdf6707519aa1e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905838"
---
# <span data-ttu-id="e76d5-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e76d5-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="e76d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e76d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e76d5-103">將部署範本存到檔案。</span><span class="sxs-lookup"><span data-stu-id="e76d5-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="e76d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="e76d5-104">SYNTAX</span></span>

### <span data-ttu-id="e76d5-105">SaveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="e76d5-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e76d5-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e76d5-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e76d5-107">描述</span><span class="sxs-lookup"><span data-stu-id="e76d5-107">DESCRIPTION</span></span>
<span data-ttu-id="e76d5-108">**Save-AzDeploymentTemdlet** 會將部署範本儲存至 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="e76d5-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="e76d5-109">例子</span><span class="sxs-lookup"><span data-stu-id="e76d5-109">EXAMPLES</span></span>

### <span data-ttu-id="e76d5-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e76d5-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="e76d5-111">此命令會從 TestDeployment 中獲得部署範本，並會將它另存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="e76d5-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="e76d5-112">範例 2：取得部署並儲存其範本</span><span class="sxs-lookup"><span data-stu-id="e76d5-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="e76d5-113">此命令會獲得目前訂閱範圍中的部署「RolesDeployment」，並保存其範本。</span><span class="sxs-lookup"><span data-stu-id="e76d5-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="e76d5-114">參數</span><span class="sxs-lookup"><span data-stu-id="e76d5-114">PARAMETERS</span></span>

### <span data-ttu-id="e76d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76d5-115">-DefaultProfile</span></span>
<span data-ttu-id="e76d5-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e76d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e76d5-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="e76d5-117">-DeploymentName</span></span>
<span data-ttu-id="e76d5-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="e76d5-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76d5-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e76d5-119">-DeploymentObject</span></span>
<span data-ttu-id="e76d5-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="e76d5-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e76d5-121">-強制</span><span class="sxs-lookup"><span data-stu-id="e76d5-121">-Force</span></span>
<span data-ttu-id="e76d5-122">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="e76d5-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e76d5-123">-路徑</span><span class="sxs-lookup"><span data-stu-id="e76d5-123">-Path</span></span>
<span data-ttu-id="e76d5-124">範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="e76d5-124">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e76d5-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="e76d5-125">-Pre</span></span>
<span data-ttu-id="e76d5-126">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e76d5-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e76d5-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e76d5-127">-Confirm</span></span>
<span data-ttu-id="e76d5-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e76d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e76d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76d5-129">-WhatIf</span></span>
<span data-ttu-id="e76d5-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e76d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76d5-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e76d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e76d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76d5-132">CommonParameters</span></span>
<span data-ttu-id="e76d5-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e76d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76d5-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e76d5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76d5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e76d5-135">INPUTS</span></span>

### <span data-ttu-id="e76d5-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e76d5-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e76d5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e76d5-137">OUTPUTS</span></span>

### <span data-ttu-id="e76d5-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="e76d5-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="e76d5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e76d5-139">NOTES</span></span>

## <span data-ttu-id="e76d5-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e76d5-140">RELATED LINKS</span></span>
