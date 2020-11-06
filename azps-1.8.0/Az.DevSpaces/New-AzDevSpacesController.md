---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 5c4abfa199a8478c247b6c2b95fe0a3651faa4f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622408"
---
# <span data-ttu-id="7be3f-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="7be3f-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="7be3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7be3f-102">SYNOPSIS</span></span>
<span data-ttu-id="7be3f-103">建立新的 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="7be3f-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="7be3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7be3f-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7be3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7be3f-105">DESCRIPTION</span></span>
<span data-ttu-id="7be3f-106">建立新的 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="7be3f-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="7be3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="7be3f-107">EXAMPLES</span></span>

### <span data-ttu-id="7be3f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7be3f-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="7be3f-109">Crreate resourcegroup devSpaceResourceGroup 中的 DevSpaces 控制器，名稱 devSpaceName。</span><span class="sxs-lookup"><span data-stu-id="7be3f-109">Crreate a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="7be3f-110">使用 clusterName 群集作為這個控制器的目標。</span><span class="sxs-lookup"><span data-stu-id="7be3f-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="7be3f-111">參數</span><span class="sxs-lookup"><span data-stu-id="7be3f-111">PARAMETERS</span></span>

### <span data-ttu-id="7be3f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7be3f-112">-AsJob</span></span>
<span data-ttu-id="7be3f-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7be3f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7be3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be3f-114">-DefaultProfile</span></span>
<span data-ttu-id="7be3f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7be3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be3f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7be3f-116">-Name</span></span>
<span data-ttu-id="7be3f-117">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="7be3f-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be3f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be3f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7be3f-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7be3f-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be3f-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="7be3f-120">-Tag</span></span>
<span data-ttu-id="7be3f-121">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7be3f-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="7be3f-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="7be3f-122">-TargetClusterName</span></span>
<span data-ttu-id="7be3f-123">目標群集名稱。</span><span class="sxs-lookup"><span data-stu-id="7be3f-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be3f-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be3f-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="7be3f-125">目標資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7be3f-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be3f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="7be3f-126">-Confirm</span></span>
<span data-ttu-id="7be3f-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7be3f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be3f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be3f-128">-WhatIf</span></span>
<span data-ttu-id="7be3f-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7be3f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be3f-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7be3f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be3f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be3f-131">CommonParameters</span></span>
<span data-ttu-id="7be3f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7be3f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be3f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7be3f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be3f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="7be3f-134">INPUTS</span></span>

### <span data-ttu-id="7be3f-135">所有</span><span class="sxs-lookup"><span data-stu-id="7be3f-135">None</span></span>

## <span data-ttu-id="7be3f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7be3f-136">OUTPUTS</span></span>

### <span data-ttu-id="7be3f-137">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="7be3f-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="7be3f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7be3f-138">NOTES</span></span>

## <span data-ttu-id="7be3f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7be3f-139">RELATED LINKS</span></span>
