---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133615"
---
# <span data-ttu-id="8191d-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8191d-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="8191d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8191d-102">SYNOPSIS</span></span>
<span data-ttu-id="8191d-103">將部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="8191d-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="8191d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8191d-104">SYNTAX</span></span>

### <span data-ttu-id="8191d-105">SaveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="8191d-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8191d-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8191d-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8191d-107">說明</span><span class="sxs-lookup"><span data-stu-id="8191d-107">DESCRIPTION</span></span>
<span data-ttu-id="8191d-108">**AzDeploymentTemplate** Cmdlet 會將部署範本儲存至 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="8191d-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="8191d-109">示例</span><span class="sxs-lookup"><span data-stu-id="8191d-109">EXAMPLES</span></span>

### <span data-ttu-id="8191d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8191d-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="8191d-111">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="8191d-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="8191d-112">範例2：取得部署並儲存其範本</span><span class="sxs-lookup"><span data-stu-id="8191d-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="8191d-113">這個命令會在目前的訂閱範圍中取得部署 "RolesDeployment"，並儲存其範本。</span><span class="sxs-lookup"><span data-stu-id="8191d-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="8191d-114">參數</span><span class="sxs-lookup"><span data-stu-id="8191d-114">PARAMETERS</span></span>

### <span data-ttu-id="8191d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8191d-115">-DefaultProfile</span></span>
<span data-ttu-id="8191d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8191d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8191d-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8191d-117">-DeploymentName</span></span>
<span data-ttu-id="8191d-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="8191d-118">The deployment name.</span></span>

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

### <span data-ttu-id="8191d-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8191d-119">-DeploymentObject</span></span>
<span data-ttu-id="8191d-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="8191d-120">The deployment object.</span></span>

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

### <span data-ttu-id="8191d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8191d-121">-Force</span></span>
<span data-ttu-id="8191d-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8191d-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8191d-123">-Path</span><span class="sxs-lookup"><span data-stu-id="8191d-123">-Path</span></span>
<span data-ttu-id="8191d-124">範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="8191d-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="8191d-125">-預先</span><span class="sxs-lookup"><span data-stu-id="8191d-125">-Pre</span></span>
<span data-ttu-id="8191d-126">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="8191d-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8191d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="8191d-127">-Confirm</span></span>
<span data-ttu-id="8191d-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8191d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8191d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8191d-129">-WhatIf</span></span>
<span data-ttu-id="8191d-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8191d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8191d-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8191d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8191d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8191d-132">CommonParameters</span></span>
<span data-ttu-id="8191d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8191d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8191d-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8191d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8191d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8191d-135">INPUTS</span></span>

### <span data-ttu-id="8191d-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8191d-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8191d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8191d-137">OUTPUTS</span></span>

### <span data-ttu-id="8191d-138">PSTemplatePath 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="8191d-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="8191d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8191d-139">NOTES</span></span>

## <span data-ttu-id="8191d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8191d-140">RELATED LINKS</span></span>
