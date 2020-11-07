---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: aa34157f556de3fe0acc5d8197caaa1a14dc364d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957692"
---
# <span data-ttu-id="b6a71-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b6a71-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="b6a71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6a71-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a71-103">將部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="b6a71-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="b6a71-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6a71-104">SYNTAX</span></span>

### <span data-ttu-id="b6a71-105">SaveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="b6a71-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6a71-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="b6a71-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a71-107">說明</span><span class="sxs-lookup"><span data-stu-id="b6a71-107">DESCRIPTION</span></span>
<span data-ttu-id="b6a71-108">**AzDeploymentTemplate** Cmdlet 會將部署範本儲存至 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b6a71-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="b6a71-109">示例</span><span class="sxs-lookup"><span data-stu-id="b6a71-109">EXAMPLES</span></span>

### <span data-ttu-id="b6a71-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b6a71-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="b6a71-111">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b6a71-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="b6a71-112">範例2：取得部署並儲存其範本</span><span class="sxs-lookup"><span data-stu-id="b6a71-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="b6a71-113">這個命令會在目前的訂閱範圍中取得部署 "RolesDeployment"，並儲存其範本。</span><span class="sxs-lookup"><span data-stu-id="b6a71-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="b6a71-114">參數</span><span class="sxs-lookup"><span data-stu-id="b6a71-114">PARAMETERS</span></span>

### <span data-ttu-id="b6a71-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6a71-115">-ApiVersion</span></span>
<span data-ttu-id="b6a71-116">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b6a71-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b6a71-117">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="b6a71-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b6a71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a71-118">-DefaultProfile</span></span>
<span data-ttu-id="b6a71-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6a71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a71-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b6a71-120">-DeploymentName</span></span>
<span data-ttu-id="b6a71-121">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="b6a71-121">The deployment name.</span></span>

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

### <span data-ttu-id="b6a71-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="b6a71-122">-DeploymentObject</span></span>
<span data-ttu-id="b6a71-123">部署物件。</span><span class="sxs-lookup"><span data-stu-id="b6a71-123">The deployment object.</span></span>

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

### <span data-ttu-id="b6a71-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b6a71-124">-Force</span></span>
<span data-ttu-id="b6a71-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="b6a71-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6a71-126">-Path</span><span class="sxs-lookup"><span data-stu-id="b6a71-126">-Path</span></span>
<span data-ttu-id="b6a71-127">範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="b6a71-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="b6a71-128">-預先</span><span class="sxs-lookup"><span data-stu-id="b6a71-128">-Pre</span></span>
<span data-ttu-id="b6a71-129">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="b6a71-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b6a71-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b6a71-130">-Confirm</span></span>
<span data-ttu-id="b6a71-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6a71-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a71-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a71-132">-WhatIf</span></span>
<span data-ttu-id="b6a71-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6a71-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a71-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6a71-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a71-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a71-135">CommonParameters</span></span>
<span data-ttu-id="b6a71-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6a71-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a71-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6a71-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a71-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b6a71-138">INPUTS</span></span>

### <span data-ttu-id="b6a71-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b6a71-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b6a71-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b6a71-140">OUTPUTS</span></span>

### <span data-ttu-id="b6a71-141">PSTemplatePath 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="b6a71-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="b6a71-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b6a71-142">NOTES</span></span>

## <span data-ttu-id="b6a71-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6a71-143">RELATED LINKS</span></span>
