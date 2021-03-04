---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 097248e06acd081582ecc34a863658b2b073ef60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915506"
---
# <span data-ttu-id="12001-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="12001-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="12001-102">簡介</span><span class="sxs-lookup"><span data-stu-id="12001-102">SYNOPSIS</span></span>
<span data-ttu-id="12001-103">建立新 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="12001-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="12001-104">語法</span><span class="sxs-lookup"><span data-stu-id="12001-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12001-105">描述</span><span class="sxs-lookup"><span data-stu-id="12001-105">DESCRIPTION</span></span>
<span data-ttu-id="12001-106">建立新 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="12001-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="12001-107">例子</span><span class="sxs-lookup"><span data-stu-id="12001-107">EXAMPLES</span></span>

### <span data-ttu-id="12001-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="12001-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="12001-109">使用名稱 devSpaceName 在 resourcegroup devSpaceResourceGroup 中建立 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="12001-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="12001-110">使用 clusterName cluster 做為此控制器的目標。</span><span class="sxs-lookup"><span data-stu-id="12001-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="12001-111">參數</span><span class="sxs-lookup"><span data-stu-id="12001-111">PARAMETERS</span></span>

### <span data-ttu-id="12001-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12001-112">-AsJob</span></span>
<span data-ttu-id="12001-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="12001-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12001-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12001-114">-DefaultProfile</span></span>
<span data-ttu-id="12001-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="12001-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12001-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="12001-116">-Name</span></span>
<span data-ttu-id="12001-117">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="12001-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="12001-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12001-118">-ResourceGroupName</span></span>
<span data-ttu-id="12001-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="12001-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="12001-120">-標記</span><span class="sxs-lookup"><span data-stu-id="12001-120">-Tag</span></span>
<span data-ttu-id="12001-121">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="12001-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="12001-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="12001-122">-TargetClusterName</span></span>
<span data-ttu-id="12001-123">目標群組名。</span><span class="sxs-lookup"><span data-stu-id="12001-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="12001-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12001-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="12001-125">目標資源組名。</span><span class="sxs-lookup"><span data-stu-id="12001-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="12001-126">-確認</span><span class="sxs-lookup"><span data-stu-id="12001-126">-Confirm</span></span>
<span data-ttu-id="12001-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="12001-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12001-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12001-128">-WhatIf</span></span>
<span data-ttu-id="12001-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12001-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12001-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12001-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12001-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12001-131">CommonParameters</span></span>
<span data-ttu-id="12001-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="12001-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12001-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="12001-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12001-134">輸入</span><span class="sxs-lookup"><span data-stu-id="12001-134">INPUTS</span></span>

### <span data-ttu-id="12001-135">沒有</span><span class="sxs-lookup"><span data-stu-id="12001-135">None</span></span>

## <span data-ttu-id="12001-136">輸出</span><span class="sxs-lookup"><span data-stu-id="12001-136">OUTPUTS</span></span>

### <span data-ttu-id="12001-137">Microsoft.Azure.Commands.DevSpaces.models.PSController</span><span class="sxs-lookup"><span data-stu-id="12001-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="12001-138">筆記</span><span class="sxs-lookup"><span data-stu-id="12001-138">NOTES</span></span>

## <span data-ttu-id="12001-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="12001-139">RELATED LINKS</span></span>
