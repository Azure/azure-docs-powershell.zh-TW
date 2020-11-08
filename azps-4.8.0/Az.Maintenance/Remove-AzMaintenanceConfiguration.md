---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127581"
---
# <span data-ttu-id="7456c-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7456c-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="7456c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7456c-102">SYNOPSIS</span></span>
<span data-ttu-id="7456c-103">刪除配置記錄</span><span class="sxs-lookup"><span data-stu-id="7456c-103">Delete Configuration record</span></span>

## <span data-ttu-id="7456c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7456c-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7456c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7456c-105">DESCRIPTION</span></span>
<span data-ttu-id="7456c-106">刪除維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="7456c-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="7456c-107">示例</span><span class="sxs-lookup"><span data-stu-id="7456c-107">EXAMPLES</span></span>

### <span data-ttu-id="7456c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7456c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="7456c-109">刪除維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="7456c-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="7456c-110">參數</span><span class="sxs-lookup"><span data-stu-id="7456c-110">PARAMETERS</span></span>

### <span data-ttu-id="7456c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7456c-111">-AsJob</span></span>
<span data-ttu-id="7456c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7456c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7456c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7456c-113">-DefaultProfile</span></span>
<span data-ttu-id="7456c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7456c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7456c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7456c-115">-Force</span></span>
<span data-ttu-id="7456c-116">強制移除而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="7456c-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="7456c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7456c-117">-Name</span></span>
<span data-ttu-id="7456c-118">維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="7456c-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="7456c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7456c-119">-PassThru</span></span>
<span data-ttu-id="7456c-120">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="7456c-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="7456c-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7456c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7456c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7456c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7456c-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7456c-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="7456c-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7456c-124">-Confirm</span></span>
<span data-ttu-id="7456c-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7456c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7456c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7456c-126">-WhatIf</span></span>
<span data-ttu-id="7456c-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7456c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7456c-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7456c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7456c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7456c-129">CommonParameters</span></span>
<span data-ttu-id="7456c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7456c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7456c-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7456c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7456c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7456c-132">INPUTS</span></span>

### <span data-ttu-id="7456c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7456c-133">System.String</span></span>

## <span data-ttu-id="7456c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7456c-134">OUTPUTS</span></span>

### <span data-ttu-id="7456c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="7456c-135">System.Boolean</span></span>

## <span data-ttu-id="7456c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7456c-136">NOTES</span></span>

## <span data-ttu-id="7456c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7456c-137">RELATED LINKS</span></span>
