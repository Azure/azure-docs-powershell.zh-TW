---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612596"
---
# <span data-ttu-id="e8426-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="e8426-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="e8426-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8426-102">SYNOPSIS</span></span>
<span data-ttu-id="e8426-103">建立步驟。</span><span class="sxs-lookup"><span data-stu-id="e8426-103">Creates a step.</span></span>

## <span data-ttu-id="e8426-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8426-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8426-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8426-105">DESCRIPTION</span></span>
<span data-ttu-id="e8426-106">**新的-AzDeploymentManagerStep** Cmdlet 會建立可在 [部署] 中參考的部署步驟。</span><span class="sxs-lookup"><span data-stu-id="e8426-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="e8426-107">指定 *Name* 、 *ResourceGroupName* 和 required 屬性。</span><span class="sxs-lookup"><span data-stu-id="e8426-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="e8426-108">您可以在本機修改傳回的物件，然後使用 Set-AzDeploymentManagerStep Cmdlet 將變更套用至步驟。</span><span class="sxs-lookup"><span data-stu-id="e8426-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="e8426-109">示例</span><span class="sxs-lookup"><span data-stu-id="e8426-109">EXAMPLES</span></span>

### <span data-ttu-id="e8426-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e8426-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="e8426-111">在 ContosoResourceGroup 中建立一個名稱為 ContosoService1WaitStep 的步驟，並將其設為資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e8426-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="e8426-112">Duration 屬性提供在執行下一個步驟之前，推出的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e8426-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="e8426-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8426-113">PARAMETERS</span></span>

### <span data-ttu-id="e8426-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8426-114">-DefaultProfile</span></span>
<span data-ttu-id="e8426-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8426-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8426-116">-工期</span><span class="sxs-lookup"><span data-stu-id="e8426-116">-Duration</span></span>
<span data-ttu-id="e8426-117">以 ISO 8601 格式等候的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e8426-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="e8426-118">例如： PT30M、PT1H</span><span class="sxs-lookup"><span data-stu-id="e8426-118">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8426-119">-位置</span><span class="sxs-lookup"><span data-stu-id="e8426-119">-Location</span></span>
<span data-ttu-id="e8426-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e8426-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8426-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8426-121">-Name</span></span>
<span data-ttu-id="e8426-122">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8426-122">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8426-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8426-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8426-124">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="e8426-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8426-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8426-125">-Tag</span></span>
<span data-ttu-id="e8426-126">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e8426-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8426-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e8426-127">-Confirm</span></span>
<span data-ttu-id="e8426-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8426-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8426-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8426-129">-WhatIf</span></span>
<span data-ttu-id="e8426-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8426-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8426-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8426-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8426-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8426-132">CommonParameters</span></span>
<span data-ttu-id="e8426-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8426-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8426-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8426-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8426-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e8426-135">INPUTS</span></span>

### <span data-ttu-id="e8426-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8426-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8426-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e8426-137">OUTPUTS</span></span>

### <span data-ttu-id="e8426-138">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="e8426-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="e8426-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e8426-139">NOTES</span></span>

## <span data-ttu-id="e8426-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8426-140">RELATED LINKS</span></span>
