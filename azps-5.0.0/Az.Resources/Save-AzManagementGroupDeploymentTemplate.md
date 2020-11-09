---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286267"
---
# <span data-ttu-id="2c06b-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="2c06b-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="2c06b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c06b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c06b-103">將部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="2c06b-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="2c06b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c06b-104">SYNTAX</span></span>

### <span data-ttu-id="2c06b-105">SaveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="2c06b-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c06b-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="2c06b-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c06b-107">說明</span><span class="sxs-lookup"><span data-stu-id="2c06b-107">DESCRIPTION</span></span>
<span data-ttu-id="2c06b-108">AzManagementGroupDeploymentTemplate Cmdlet 會將部署範本 **儲存**  到管理群組上部署的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="2c06b-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="2c06b-109">示例</span><span class="sxs-lookup"><span data-stu-id="2c06b-109">EXAMPLES</span></span>

### <span data-ttu-id="2c06b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2c06b-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="2c06b-111">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="2c06b-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="2c06b-112">範例2：取得部署並儲存其範本</span><span class="sxs-lookup"><span data-stu-id="2c06b-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="2c06b-113">這個命令會取得管理群組 "myMG" 的部署 "RolesDeployment"，並儲存其範本。</span><span class="sxs-lookup"><span data-stu-id="2c06b-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="2c06b-114">參數</span><span class="sxs-lookup"><span data-stu-id="2c06b-114">PARAMETERS</span></span>

### <span data-ttu-id="2c06b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c06b-115">-DefaultProfile</span></span>
<span data-ttu-id="2c06b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c06b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c06b-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="2c06b-117">-DeploymentName</span></span>
<span data-ttu-id="2c06b-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="2c06b-118">The deployment name.</span></span>

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

### <span data-ttu-id="2c06b-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="2c06b-119">-DeploymentObject</span></span>
<span data-ttu-id="2c06b-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="2c06b-120">The deployment object.</span></span>

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

### <span data-ttu-id="2c06b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2c06b-121">-Force</span></span>
<span data-ttu-id="2c06b-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2c06b-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c06b-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2c06b-123">-ManagementGroupId</span></span>
<span data-ttu-id="2c06b-124">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c06b-124">The management group id.</span></span>

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

### <span data-ttu-id="2c06b-125">-Path</span><span class="sxs-lookup"><span data-stu-id="2c06b-125">-Path</span></span>
<span data-ttu-id="2c06b-126">範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="2c06b-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="2c06b-127">-預先</span><span class="sxs-lookup"><span data-stu-id="2c06b-127">-Pre</span></span>
<span data-ttu-id="2c06b-128">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="2c06b-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2c06b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="2c06b-129">-Confirm</span></span>
<span data-ttu-id="2c06b-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c06b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c06b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c06b-131">-WhatIf</span></span>
<span data-ttu-id="2c06b-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c06b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c06b-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c06b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c06b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c06b-134">CommonParameters</span></span>
<span data-ttu-id="2c06b-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c06b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c06b-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c06b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c06b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2c06b-137">INPUTS</span></span>

### <span data-ttu-id="2c06b-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2c06b-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2c06b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2c06b-139">OUTPUTS</span></span>

### <span data-ttu-id="2c06b-140">PSTemplatePath 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="2c06b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="2c06b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2c06b-141">NOTES</span></span>

## <span data-ttu-id="2c06b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c06b-142">RELATED LINKS</span></span>
