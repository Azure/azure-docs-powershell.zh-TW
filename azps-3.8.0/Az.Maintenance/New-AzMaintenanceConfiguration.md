---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965666"
---
# <span data-ttu-id="09121-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="09121-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="09121-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09121-102">SYNOPSIS</span></span>
<span data-ttu-id="09121-103">建立或更新配置記錄</span><span class="sxs-lookup"><span data-stu-id="09121-103">Create or Update configuration record</span></span>

## <span data-ttu-id="09121-104">句法</span><span class="sxs-lookup"><span data-stu-id="09121-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09121-105">說明</span><span class="sxs-lookup"><span data-stu-id="09121-105">DESCRIPTION</span></span>
<span data-ttu-id="09121-106">建立或更新配置記錄</span><span class="sxs-lookup"><span data-stu-id="09121-106">Create or Update configuration record</span></span>

## <span data-ttu-id="09121-107">示例</span><span class="sxs-lookup"><span data-stu-id="09121-107">EXAMPLES</span></span>

### <span data-ttu-id="09121-108">範例1</span><span class="sxs-lookup"><span data-stu-id="09121-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="09121-109">使用作用域主機建立維護配置</span><span class="sxs-lookup"><span data-stu-id="09121-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="09121-110">參數</span><span class="sxs-lookup"><span data-stu-id="09121-110">PARAMETERS</span></span>

### <span data-ttu-id="09121-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09121-111">-AsJob</span></span>
<span data-ttu-id="09121-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="09121-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09121-113">-DefaultProfile</span></span>
<span data-ttu-id="09121-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09121-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09121-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="09121-115">-ExtensionProperty</span></span>
<span data-ttu-id="09121-116">每個資源的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="09121-116">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="09121-117">-位置</span><span class="sxs-lookup"><span data-stu-id="09121-117">-Location</span></span>
<span data-ttu-id="09121-118">維護配置位置。</span><span class="sxs-lookup"><span data-stu-id="09121-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="09121-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="09121-119">-MaintenanceScope</span></span>
<span data-ttu-id="09121-120">維護範圍。</span><span class="sxs-lookup"><span data-stu-id="09121-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="09121-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="09121-121">-Name</span></span>
<span data-ttu-id="09121-122">維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="09121-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="09121-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09121-123">-ResourceGroupName</span></span>
<span data-ttu-id="09121-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09121-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="09121-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="09121-125">-Tag</span></span>
<span data-ttu-id="09121-126">ARM 標記。</span><span class="sxs-lookup"><span data-stu-id="09121-126">The ARM Tags.</span></span>

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

### <span data-ttu-id="09121-127">-確認</span><span class="sxs-lookup"><span data-stu-id="09121-127">-Confirm</span></span>
<span data-ttu-id="09121-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="09121-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09121-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09121-129">-WhatIf</span></span>
<span data-ttu-id="09121-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09121-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09121-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09121-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09121-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09121-132">CommonParameters</span></span>
<span data-ttu-id="09121-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09121-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09121-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09121-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09121-135">輸入</span><span class="sxs-lookup"><span data-stu-id="09121-135">INPUTS</span></span>

### <span data-ttu-id="09121-136">System.object</span><span class="sxs-lookup"><span data-stu-id="09121-136">System.String</span></span>

## <span data-ttu-id="09121-137">輸出</span><span class="sxs-lookup"><span data-stu-id="09121-137">OUTPUTS</span></span>

### <span data-ttu-id="09121-138">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="09121-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="09121-139">筆記</span><span class="sxs-lookup"><span data-stu-id="09121-139">NOTES</span></span>

## <span data-ttu-id="09121-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="09121-140">RELATED LINKS</span></span>
