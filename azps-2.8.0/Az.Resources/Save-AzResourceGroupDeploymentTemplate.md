---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791154"
---
# <span data-ttu-id="2f62d-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="2f62d-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="2f62d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f62d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f62d-103">將資源群組部署範本儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="2f62d-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="2f62d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f62d-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f62d-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f62d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f62d-106">AzResourceGroupDeploymentTemplate Cmdlet 會將資源群組部署範本 **儲存**  至 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="2f62d-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="2f62d-107">示例</span><span class="sxs-lookup"><span data-stu-id="2f62d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f62d-108">範例1：儲存部署範本</span><span class="sxs-lookup"><span data-stu-id="2f62d-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="2f62d-109">這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="2f62d-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="2f62d-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f62d-110">PARAMETERS</span></span>

### <span data-ttu-id="2f62d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2f62d-111">-ApiVersion</span></span>
<span data-ttu-id="2f62d-112">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2f62d-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2f62d-113">如果沒有指定，則會使用最新的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2f62d-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="2f62d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f62d-114">-DefaultProfile</span></span>
<span data-ttu-id="2f62d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2f62d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f62d-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="2f62d-116">-DeploymentName</span></span>
<span data-ttu-id="2f62d-117">指定部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f62d-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="2f62d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2f62d-118">-Force</span></span>
<span data-ttu-id="2f62d-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2f62d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f62d-120">-Path</span><span class="sxs-lookup"><span data-stu-id="2f62d-120">-Path</span></span>
<span data-ttu-id="2f62d-121">指定範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="2f62d-121">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="2f62d-122">-預先</span><span class="sxs-lookup"><span data-stu-id="2f62d-122">-Pre</span></span>
<span data-ttu-id="2f62d-123">表示當您自動判斷要使用哪個 API 版本時，此 Cmdlet 會使用預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2f62d-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="2f62d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f62d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f62d-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f62d-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2f62d-126">-確認</span><span class="sxs-lookup"><span data-stu-id="2f62d-126">-Confirm</span></span>
<span data-ttu-id="2f62d-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f62d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f62d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f62d-128">-WhatIf</span></span>
<span data-ttu-id="2f62d-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f62d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f62d-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f62d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f62d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f62d-131">CommonParameters</span></span>
<span data-ttu-id="2f62d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f62d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f62d-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f62d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f62d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="2f62d-134">INPUTS</span></span>

### <span data-ttu-id="2f62d-135">System.object</span><span class="sxs-lookup"><span data-stu-id="2f62d-135">System.String</span></span>

## <span data-ttu-id="2f62d-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2f62d-136">OUTPUTS</span></span>

### <span data-ttu-id="2f62d-137">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="2f62d-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2f62d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2f62d-138">NOTES</span></span>

## <span data-ttu-id="2f62d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f62d-139">RELATED LINKS</span></span>
