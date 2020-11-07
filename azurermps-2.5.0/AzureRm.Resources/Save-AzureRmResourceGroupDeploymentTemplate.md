---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: 78ad8ee76aeeec4f57e0d2f2a6b2a1f4d9424d97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800302"
---
# <span data-ttu-id="b8c5d-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b8c5d-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="b8c5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c5d-103">將資源群組部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8c5d-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c5d-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c5d-106">AzureRmResourceGroupDeploymentTemplate Cmdlet 會將資源群組部署範本 **儲存**  至 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="b8c5d-107">示例</span><span class="sxs-lookup"><span data-stu-id="b8c5d-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c5d-108">範例1：儲存部署範本</span><span class="sxs-lookup"><span data-stu-id="b8c5d-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="b8c5d-109">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="b8c5d-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8c5d-110">PARAMETERS</span></span>

### <span data-ttu-id="b8c5d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b8c5d-111">-ApiVersion</span></span>
<span data-ttu-id="b8c5d-112">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b8c5d-113">如果沒有指定，則會使用最新的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="b8c5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c5d-114">-DefaultProfile</span></span>
<span data-ttu-id="b8c5d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b8c5d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c5d-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b8c5d-116">-DeploymentName</span></span>
<span data-ttu-id="b8c5d-117">指定部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="b8c5d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c5d-118">-Force</span></span>
<span data-ttu-id="b8c5d-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8c5d-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8c5d-120">-InformationAction</span></span>
<span data-ttu-id="b8c5d-121">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b8c5d-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b8c5d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8c5d-123">持續</span><span class="sxs-lookup"><span data-stu-id="b8c5d-123">Continue</span></span>
- <span data-ttu-id="b8c5d-124">理會</span><span class="sxs-lookup"><span data-stu-id="b8c5d-124">Ignore</span></span>
- <span data-ttu-id="b8c5d-125">看</span><span class="sxs-lookup"><span data-stu-id="b8c5d-125">Inquire</span></span>
- <span data-ttu-id="b8c5d-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8c5d-126">SilentlyContinue</span></span>
- <span data-ttu-id="b8c5d-127">停止</span><span class="sxs-lookup"><span data-stu-id="b8c5d-127">Stop</span></span>
- <span data-ttu-id="b8c5d-128">封存</span><span class="sxs-lookup"><span data-stu-id="b8c5d-128">Suspend</span></span>

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

### <span data-ttu-id="b8c5d-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8c5d-129">-InformationVariable</span></span>
<span data-ttu-id="b8c5d-130">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8c5d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b8c5d-131">-Path</span></span>
<span data-ttu-id="b8c5d-132">指定範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="b8c5d-133">-預先</span><span class="sxs-lookup"><span data-stu-id="b8c5d-133">-Pre</span></span>
<span data-ttu-id="b8c5d-134">表示當您自動判斷要使用哪個 API 版本時，此 Cmdlet 會使用預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="b8c5d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c5d-135">-ResourceGroupName</span></span>
<span data-ttu-id="b8c5d-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b8c5d-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b8c5d-137">-Confirm</span></span>
<span data-ttu-id="b8c5d-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c5d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c5d-139">-WhatIf</span></span>
<span data-ttu-id="b8c5d-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c5d-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c5d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c5d-142">CommonParameters</span></span>
<span data-ttu-id="b8c5d-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c5d-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8c5d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c5d-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c5d-145">INPUTS</span></span>

## <span data-ttu-id="b8c5d-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c5d-146">OUTPUTS</span></span>

## <span data-ttu-id="b8c5d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c5d-147">NOTES</span></span>

## <span data-ttu-id="b8c5d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c5d-148">RELATED LINKS</span></span>
