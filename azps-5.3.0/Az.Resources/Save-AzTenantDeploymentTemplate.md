---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449196"
---
# <span data-ttu-id="f1dda-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f1dda-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="f1dda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1dda-102">SYNOPSIS</span></span>
<span data-ttu-id="f1dda-103">將部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="f1dda-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="f1dda-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1dda-104">SYNTAX</span></span>

### <span data-ttu-id="f1dda-105">SaveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1dda-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dda-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f1dda-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1dda-107">說明</span><span class="sxs-lookup"><span data-stu-id="f1dda-107">DESCRIPTION</span></span>
<span data-ttu-id="f1dda-108">AzTenantDeploymentTemplate Cmdlet 會將部署範本 **儲存**  至 JSON 檔案，以便在租使用者範圍中部署。</span><span class="sxs-lookup"><span data-stu-id="f1dda-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="f1dda-109">示例</span><span class="sxs-lookup"><span data-stu-id="f1dda-109">EXAMPLES</span></span>

### <span data-ttu-id="f1dda-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f1dda-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="f1dda-111">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="f1dda-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="f1dda-112">範例2：取得部署並儲存其範本</span><span class="sxs-lookup"><span data-stu-id="f1dda-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="f1dda-113">這個命令會在目前的租使用者範圍中取得部署 "RolesDeployment"，並儲存其範本。</span><span class="sxs-lookup"><span data-stu-id="f1dda-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="f1dda-114">參數</span><span class="sxs-lookup"><span data-stu-id="f1dda-114">PARAMETERS</span></span>

### <span data-ttu-id="f1dda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1dda-115">-DefaultProfile</span></span>
<span data-ttu-id="f1dda-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1dda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1dda-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="f1dda-117">-DeploymentName</span></span>
<span data-ttu-id="f1dda-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="f1dda-118">The deployment name.</span></span>

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

### <span data-ttu-id="f1dda-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f1dda-119">-DeploymentObject</span></span>
<span data-ttu-id="f1dda-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="f1dda-120">The deployment object.</span></span>

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

### <span data-ttu-id="f1dda-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f1dda-121">-Force</span></span>
<span data-ttu-id="f1dda-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="f1dda-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1dda-123">-Path</span><span class="sxs-lookup"><span data-stu-id="f1dda-123">-Path</span></span>
<span data-ttu-id="f1dda-124">範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="f1dda-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="f1dda-125">-預先</span><span class="sxs-lookup"><span data-stu-id="f1dda-125">-Pre</span></span>
<span data-ttu-id="f1dda-126">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="f1dda-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f1dda-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f1dda-127">-Confirm</span></span>
<span data-ttu-id="f1dda-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1dda-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1dda-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1dda-129">-WhatIf</span></span>
<span data-ttu-id="f1dda-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1dda-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1dda-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1dda-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1dda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1dda-132">CommonParameters</span></span>
<span data-ttu-id="f1dda-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1dda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1dda-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1dda-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1dda-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f1dda-135">INPUTS</span></span>

### <span data-ttu-id="f1dda-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f1dda-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f1dda-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f1dda-137">OUTPUTS</span></span>

### <span data-ttu-id="f1dda-138">PSTemplatePath 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="f1dda-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="f1dda-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f1dda-139">NOTES</span></span>

## <span data-ttu-id="f1dda-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1dda-140">RELATED LINKS</span></span>
