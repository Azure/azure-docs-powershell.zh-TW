---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 2cebdeab994926d51ff5ff49e6a4a101f3e5c778
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910465"
---
# <span data-ttu-id="a4df9-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4df9-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="a4df9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a4df9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4df9-103">刪除組組記錄</span><span class="sxs-lookup"><span data-stu-id="a4df9-103">Delete Configuration record</span></span>

## <span data-ttu-id="a4df9-104">語法</span><span class="sxs-lookup"><span data-stu-id="a4df9-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4df9-105">描述</span><span class="sxs-lookup"><span data-stu-id="a4df9-105">DESCRIPTION</span></span>
<span data-ttu-id="a4df9-106">刪除維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="a4df9-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="a4df9-107">例子</span><span class="sxs-lookup"><span data-stu-id="a4df9-107">EXAMPLES</span></span>

### <span data-ttu-id="a4df9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a4df9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="a4df9-109">刪除維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="a4df9-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="a4df9-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4df9-110">PARAMETERS</span></span>

### <span data-ttu-id="a4df9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4df9-111">-AsJob</span></span>
<span data-ttu-id="a4df9-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a4df9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4df9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4df9-113">-DefaultProfile</span></span>
<span data-ttu-id="a4df9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4df9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4df9-115">-強制</span><span class="sxs-lookup"><span data-stu-id="a4df9-115">-Force</span></span>
<span data-ttu-id="a4df9-116">強制移除而不確認。</span><span class="sxs-lookup"><span data-stu-id="a4df9-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="a4df9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4df9-117">-Name</span></span>
<span data-ttu-id="a4df9-118">維護組組名稱。</span><span class="sxs-lookup"><span data-stu-id="a4df9-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="a4df9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4df9-119">-PassThru</span></span>
<span data-ttu-id="a4df9-120">會返回移除作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4df9-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="a4df9-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a4df9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4df9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4df9-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4df9-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a4df9-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="a4df9-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a4df9-124">-Confirm</span></span>
<span data-ttu-id="a4df9-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a4df9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4df9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4df9-126">-WhatIf</span></span>
<span data-ttu-id="a4df9-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4df9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4df9-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4df9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4df9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4df9-129">CommonParameters</span></span>
<span data-ttu-id="a4df9-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a4df9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4df9-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4df9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4df9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a4df9-132">INPUTS</span></span>

### <span data-ttu-id="a4df9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a4df9-133">System.String</span></span>

## <span data-ttu-id="a4df9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a4df9-134">OUTPUTS</span></span>

### <span data-ttu-id="a4df9-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4df9-135">System.Boolean</span></span>

## <span data-ttu-id="a4df9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a4df9-136">NOTES</span></span>

## <span data-ttu-id="a4df9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4df9-137">RELATED LINKS</span></span>
