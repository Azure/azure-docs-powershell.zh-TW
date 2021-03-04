---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: c5d01afa5cd583ac0d356913dc3633cfddba6204
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917929"
---
# <span data-ttu-id="f1834-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f1834-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="f1834-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1834-102">SYNOPSIS</span></span>
<span data-ttu-id="f1834-103">將部署範本存到檔案。</span><span class="sxs-lookup"><span data-stu-id="f1834-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="f1834-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1834-104">SYNTAX</span></span>

### <span data-ttu-id="f1834-105">SaveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1834-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1834-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f1834-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1834-107">描述</span><span class="sxs-lookup"><span data-stu-id="f1834-107">DESCRIPTION</span></span>
<span data-ttu-id="f1834-108">**Save-AzManagementGroupDeploymentTemdlet** 會將部署範本儲存至 JSON 檔案，以用於管理群組的部署。</span><span class="sxs-lookup"><span data-stu-id="f1834-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="f1834-109">例子</span><span class="sxs-lookup"><span data-stu-id="f1834-109">EXAMPLES</span></span>

### <span data-ttu-id="f1834-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f1834-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="f1834-111">此命令會從 TestDeployment 中獲得部署範本，並會將它另存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="f1834-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="f1834-112">範例 2：取得部署並儲存其範本</span><span class="sxs-lookup"><span data-stu-id="f1834-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="f1834-113">此命令會獲得管理群組 「myMG」的部署「RolesDeployment」，並保存其範本。</span><span class="sxs-lookup"><span data-stu-id="f1834-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="f1834-114">參數</span><span class="sxs-lookup"><span data-stu-id="f1834-114">PARAMETERS</span></span>

### <span data-ttu-id="f1834-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1834-115">-DefaultProfile</span></span>
<span data-ttu-id="f1834-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1834-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1834-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f1834-117">-DeploymentName</span></span>
<span data-ttu-id="f1834-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="f1834-118">The deployment name.</span></span>

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

### <span data-ttu-id="f1834-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f1834-119">-DeploymentObject</span></span>
<span data-ttu-id="f1834-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="f1834-120">The deployment object.</span></span>

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

### <span data-ttu-id="f1834-121">-強制</span><span class="sxs-lookup"><span data-stu-id="f1834-121">-Force</span></span>
<span data-ttu-id="f1834-122">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="f1834-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1834-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f1834-123">-ManagementGroupId</span></span>
<span data-ttu-id="f1834-124">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1834-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1834-125">-路徑</span><span class="sxs-lookup"><span data-stu-id="f1834-125">-Path</span></span>
<span data-ttu-id="f1834-126">範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="f1834-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="f1834-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f1834-127">-Pre</span></span>
<span data-ttu-id="f1834-128">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f1834-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f1834-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f1834-129">-Confirm</span></span>
<span data-ttu-id="f1834-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1834-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1834-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1834-131">-WhatIf</span></span>
<span data-ttu-id="f1834-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1834-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1834-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1834-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1834-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1834-134">CommonParameters</span></span>
<span data-ttu-id="f1834-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1834-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1834-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1834-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1834-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f1834-137">INPUTS</span></span>

### <span data-ttu-id="f1834-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f1834-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f1834-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f1834-139">OUTPUTS</span></span>

### <span data-ttu-id="f1834-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="f1834-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="f1834-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f1834-141">NOTES</span></span>

## <span data-ttu-id="f1834-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1834-142">RELATED LINKS</span></span>
