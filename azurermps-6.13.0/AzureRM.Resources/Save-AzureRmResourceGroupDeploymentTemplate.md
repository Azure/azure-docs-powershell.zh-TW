---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 3f73a7d4192f6e77b66698cd84f65b40bc5505fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625753"
---
# <span data-ttu-id="b16d9-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b16d9-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="b16d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b16d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b16d9-103">將資源群組部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="b16d9-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b16d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b16d9-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b16d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="b16d9-105">DESCRIPTION</span></span>
<span data-ttu-id="b16d9-106">AzureRmResourceGroupDeploymentTemplate Cmdlet 會將資源群組部署範本 **儲存**  至 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b16d9-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="b16d9-107">示例</span><span class="sxs-lookup"><span data-stu-id="b16d9-107">EXAMPLES</span></span>

### <span data-ttu-id="b16d9-108">範例1：儲存部署範本</span><span class="sxs-lookup"><span data-stu-id="b16d9-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="b16d9-109">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b16d9-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="b16d9-110">參數</span><span class="sxs-lookup"><span data-stu-id="b16d9-110">PARAMETERS</span></span>

### <span data-ttu-id="b16d9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b16d9-111">-ApiVersion</span></span>
<span data-ttu-id="b16d9-112">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b16d9-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b16d9-113">如果沒有指定，則會使用最新的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b16d9-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="b16d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16d9-114">-DefaultProfile</span></span>
<span data-ttu-id="b16d9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b16d9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b16d9-116">-DeploymentName</span></span>
<span data-ttu-id="b16d9-117">指定部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="b16d9-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b16d9-118">-Force</span></span>
<span data-ttu-id="b16d9-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b16d9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b16d9-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b16d9-120">-InformationAction</span></span>
<span data-ttu-id="b16d9-121">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b16d9-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b16d9-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b16d9-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b16d9-123">持續</span><span class="sxs-lookup"><span data-stu-id="b16d9-123">Continue</span></span>
- <span data-ttu-id="b16d9-124">理會</span><span class="sxs-lookup"><span data-stu-id="b16d9-124">Ignore</span></span>
- <span data-ttu-id="b16d9-125">看</span><span class="sxs-lookup"><span data-stu-id="b16d9-125">Inquire</span></span>
- <span data-ttu-id="b16d9-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b16d9-126">SilentlyContinue</span></span>
- <span data-ttu-id="b16d9-127">停止</span><span class="sxs-lookup"><span data-stu-id="b16d9-127">Stop</span></span>
- <span data-ttu-id="b16d9-128">封存</span><span class="sxs-lookup"><span data-stu-id="b16d9-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b16d9-129">-InformationVariable</span></span>
<span data-ttu-id="b16d9-130">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b16d9-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b16d9-131">-Path</span></span>
<span data-ttu-id="b16d9-132">指定範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="b16d9-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-133">-預先</span><span class="sxs-lookup"><span data-stu-id="b16d9-133">-Pre</span></span>
<span data-ttu-id="b16d9-134">表示當您自動判斷要使用哪個 API 版本時，此 Cmdlet 會使用預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b16d9-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="b16d9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16d9-135">-ResourceGroupName</span></span>
<span data-ttu-id="b16d9-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b16d9-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b16d9-137">-Confirm</span></span>
<span data-ttu-id="b16d9-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b16d9-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16d9-139">-WhatIf</span></span>
<span data-ttu-id="b16d9-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b16d9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16d9-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b16d9-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16d9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16d9-142">CommonParameters</span></span>
<span data-ttu-id="b16d9-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b16d9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16d9-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b16d9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16d9-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b16d9-145">INPUTS</span></span>

## <span data-ttu-id="b16d9-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b16d9-146">OUTPUTS</span></span>

## <span data-ttu-id="b16d9-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b16d9-147">NOTES</span></span>

## <span data-ttu-id="b16d9-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b16d9-148">RELATED LINKS</span></span>
