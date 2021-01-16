---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288808"
---
# <span data-ttu-id="4e39c-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="4e39c-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="4e39c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e39c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e39c-103">將維護更新套用至資源</span><span class="sxs-lookup"><span data-stu-id="4e39c-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="4e39c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e39c-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e39c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e39c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e39c-106">將維護更新套用至資源</span><span class="sxs-lookup"><span data-stu-id="4e39c-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="4e39c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e39c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e39c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4e39c-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="4e39c-109">將維護更新套用至資源</span><span class="sxs-lookup"><span data-stu-id="4e39c-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="4e39c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e39c-110">PARAMETERS</span></span>

### <span data-ttu-id="4e39c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e39c-111">-AsJob</span></span>
<span data-ttu-id="4e39c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4e39c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e39c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e39c-113">-DefaultProfile</span></span>
<span data-ttu-id="4e39c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e39c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e39c-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4e39c-115">-ProviderName</span></span>
<span data-ttu-id="4e39c-116">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="4e39c-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e39c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e39c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e39c-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e39c-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e39c-119">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="4e39c-119">-ResourceName</span></span>
<span data-ttu-id="4e39c-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4e39c-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e39c-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="4e39c-121">-ResourceParentName</span></span>
<span data-ttu-id="4e39c-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4e39c-122">The parent resource name.</span></span>

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

### <span data-ttu-id="4e39c-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="4e39c-123">-ResourceParentType</span></span>
<span data-ttu-id="4e39c-124">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="4e39c-124">The parent resource type.</span></span>

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

### <span data-ttu-id="4e39c-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4e39c-125">-ResourceType</span></span>
<span data-ttu-id="4e39c-126">資源類型。</span><span class="sxs-lookup"><span data-stu-id="4e39c-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e39c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4e39c-127">-Confirm</span></span>
<span data-ttu-id="4e39c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e39c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e39c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e39c-129">-WhatIf</span></span>
<span data-ttu-id="4e39c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e39c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e39c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e39c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e39c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e39c-132">CommonParameters</span></span>
<span data-ttu-id="4e39c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e39c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e39c-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e39c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e39c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4e39c-135">INPUTS</span></span>

### <span data-ttu-id="4e39c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4e39c-136">System.String</span></span>

## <span data-ttu-id="4e39c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4e39c-137">OUTPUTS</span></span>

### <span data-ttu-id="4e39c-138">PSApplyUpdate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e39c-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="4e39c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4e39c-139">NOTES</span></span>

## <span data-ttu-id="4e39c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e39c-140">RELATED LINKS</span></span>
