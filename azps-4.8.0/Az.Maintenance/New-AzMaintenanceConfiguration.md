---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127582"
---
# <span data-ttu-id="a65a2-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a65a2-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="a65a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a65a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a65a2-103">建立或更新配置記錄</span><span class="sxs-lookup"><span data-stu-id="a65a2-103">Create or Update configuration record</span></span>

## <span data-ttu-id="a65a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a65a2-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a65a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a65a2-105">DESCRIPTION</span></span>
<span data-ttu-id="a65a2-106">建立或更新配置記錄</span><span class="sxs-lookup"><span data-stu-id="a65a2-106">Create or Update configuration record</span></span>

## <span data-ttu-id="a65a2-107">示例</span><span class="sxs-lookup"><span data-stu-id="a65a2-107">EXAMPLES</span></span>

### <span data-ttu-id="a65a2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a65a2-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="a65a2-109">使用作用域主機建立維護配置</span><span class="sxs-lookup"><span data-stu-id="a65a2-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="a65a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a65a2-110">PARAMETERS</span></span>

### <span data-ttu-id="a65a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a65a2-111">-AsJob</span></span>
<span data-ttu-id="a65a2-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a65a2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a65a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65a2-113">-DefaultProfile</span></span>
<span data-ttu-id="a65a2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a65a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a65a2-115">-工期</span><span class="sxs-lookup"><span data-stu-id="a65a2-115">-Duration</span></span>
<span data-ttu-id="a65a2-116">工期</span><span class="sxs-lookup"><span data-stu-id="a65a2-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65a2-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="a65a2-117">-ExpirationDateTime</span></span>
<span data-ttu-id="a65a2-118">[YYYY-MM hh： MM] 格式的排程 expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="a65a2-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="a65a2-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="a65a2-119">-ExtensionProperty</span></span>
<span data-ttu-id="a65a2-120">每個資源的擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="a65a2-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="a65a2-121">-位置</span><span class="sxs-lookup"><span data-stu-id="a65a2-121">-Location</span></span>
<span data-ttu-id="a65a2-122">維護配置位置。</span><span class="sxs-lookup"><span data-stu-id="a65a2-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="a65a2-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="a65a2-123">-MaintenanceScope</span></span>
<span data-ttu-id="a65a2-124">維護範圍。</span><span class="sxs-lookup"><span data-stu-id="a65a2-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="a65a2-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a65a2-125">-Name</span></span>
<span data-ttu-id="a65a2-126">維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a65a2-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="a65a2-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="a65a2-127">-RecurEvery</span></span>
<span data-ttu-id="a65a2-128">排程週期</span><span class="sxs-lookup"><span data-stu-id="a65a2-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="a65a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="a65a2-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a65a2-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="a65a2-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a65a2-131">-StartDateTime</span></span>
<span data-ttu-id="a65a2-132">[YYYY-MM hh： MM] 格式的排程 StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a65a2-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="a65a2-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="a65a2-133">-Tag</span></span>
<span data-ttu-id="a65a2-134">ARM 標記。</span><span class="sxs-lookup"><span data-stu-id="a65a2-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="a65a2-135">-時區</span><span class="sxs-lookup"><span data-stu-id="a65a2-135">-Timezone</span></span>
<span data-ttu-id="a65a2-136">時區</span><span class="sxs-lookup"><span data-stu-id="a65a2-136">The timezone</span></span>

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

### <span data-ttu-id="a65a2-137">-可見度</span><span class="sxs-lookup"><span data-stu-id="a65a2-137">-Visibility</span></span>
<span data-ttu-id="a65a2-138">範圍的可見度</span><span class="sxs-lookup"><span data-stu-id="a65a2-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="a65a2-139">-確認</span><span class="sxs-lookup"><span data-stu-id="a65a2-139">-Confirm</span></span>
<span data-ttu-id="a65a2-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a65a2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65a2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65a2-141">-WhatIf</span></span>
<span data-ttu-id="a65a2-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a65a2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65a2-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a65a2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65a2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65a2-144">CommonParameters</span></span>
<span data-ttu-id="a65a2-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a65a2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65a2-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a65a2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65a2-147">輸入</span><span class="sxs-lookup"><span data-stu-id="a65a2-147">INPUTS</span></span>

### <span data-ttu-id="a65a2-148">System.object</span><span class="sxs-lookup"><span data-stu-id="a65a2-148">System.String</span></span>

## <span data-ttu-id="a65a2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a65a2-149">OUTPUTS</span></span>

### <span data-ttu-id="a65a2-150">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a65a2-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="a65a2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a65a2-151">NOTES</span></span>

## <span data-ttu-id="a65a2-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a65a2-152">RELATED LINKS</span></span>
