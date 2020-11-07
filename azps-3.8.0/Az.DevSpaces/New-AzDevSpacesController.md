---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965804"
---
# <span data-ttu-id="80b32-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="80b32-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="80b32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80b32-102">SYNOPSIS</span></span>
<span data-ttu-id="80b32-103">建立新的 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="80b32-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="80b32-104">句法</span><span class="sxs-lookup"><span data-stu-id="80b32-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b32-105">說明</span><span class="sxs-lookup"><span data-stu-id="80b32-105">DESCRIPTION</span></span>
<span data-ttu-id="80b32-106">建立新的 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="80b32-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="80b32-107">示例</span><span class="sxs-lookup"><span data-stu-id="80b32-107">EXAMPLES</span></span>

### <span data-ttu-id="80b32-108">範例1</span><span class="sxs-lookup"><span data-stu-id="80b32-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="80b32-109">使用名稱 devSpaceName 在 resourcegroup devSpaceResourceGroup 中建立 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="80b32-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="80b32-110">使用 clusterName 群集作為這個控制器的目標。</span><span class="sxs-lookup"><span data-stu-id="80b32-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="80b32-111">參數</span><span class="sxs-lookup"><span data-stu-id="80b32-111">PARAMETERS</span></span>

### <span data-ttu-id="80b32-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80b32-112">-AsJob</span></span>
<span data-ttu-id="80b32-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80b32-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80b32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b32-114">-DefaultProfile</span></span>
<span data-ttu-id="80b32-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80b32-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80b32-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="80b32-116">-Name</span></span>
<span data-ttu-id="80b32-117">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="80b32-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="80b32-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b32-118">-ResourceGroupName</span></span>
<span data-ttu-id="80b32-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="80b32-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="80b32-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="80b32-120">-Tag</span></span>
<span data-ttu-id="80b32-121">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="80b32-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="80b32-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="80b32-122">-TargetClusterName</span></span>
<span data-ttu-id="80b32-123">目標群集名稱。</span><span class="sxs-lookup"><span data-stu-id="80b32-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="80b32-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b32-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="80b32-125">目標資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80b32-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="80b32-126">-確認</span><span class="sxs-lookup"><span data-stu-id="80b32-126">-Confirm</span></span>
<span data-ttu-id="80b32-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80b32-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b32-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b32-128">-WhatIf</span></span>
<span data-ttu-id="80b32-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80b32-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b32-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80b32-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b32-131">CommonParameters</span></span>
<span data-ttu-id="80b32-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80b32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b32-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80b32-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b32-134">輸入</span><span class="sxs-lookup"><span data-stu-id="80b32-134">INPUTS</span></span>

### <span data-ttu-id="80b32-135">所有</span><span class="sxs-lookup"><span data-stu-id="80b32-135">None</span></span>

## <span data-ttu-id="80b32-136">輸出</span><span class="sxs-lookup"><span data-stu-id="80b32-136">OUTPUTS</span></span>

### <span data-ttu-id="80b32-137">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="80b32-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="80b32-138">筆記</span><span class="sxs-lookup"><span data-stu-id="80b32-138">NOTES</span></span>

## <span data-ttu-id="80b32-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="80b32-139">RELATED LINKS</span></span>
