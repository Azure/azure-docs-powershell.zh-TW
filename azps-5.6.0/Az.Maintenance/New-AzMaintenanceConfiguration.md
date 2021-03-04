---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: ac264e048ea428ba68caa683eb6076074c9894b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910478"
---
# <span data-ttu-id="97d42-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="97d42-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="97d42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="97d42-102">SYNOPSIS</span></span>
<span data-ttu-id="97d42-103">建立或更新組組記錄</span><span class="sxs-lookup"><span data-stu-id="97d42-103">Create or Update configuration record</span></span>

## <span data-ttu-id="97d42-104">語法</span><span class="sxs-lookup"><span data-stu-id="97d42-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97d42-105">描述</span><span class="sxs-lookup"><span data-stu-id="97d42-105">DESCRIPTION</span></span>
<span data-ttu-id="97d42-106">建立或更新組組記錄</span><span class="sxs-lookup"><span data-stu-id="97d42-106">Create or Update configuration record</span></span>

## <span data-ttu-id="97d42-107">例子</span><span class="sxs-lookup"><span data-stu-id="97d42-107">EXAMPLES</span></span>

### <span data-ttu-id="97d42-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="97d42-108">Example 1</span></span>
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

<span data-ttu-id="97d42-109">使用範圍主機建立維護組</span><span class="sxs-lookup"><span data-stu-id="97d42-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="97d42-110">參數</span><span class="sxs-lookup"><span data-stu-id="97d42-110">PARAMETERS</span></span>

### <span data-ttu-id="97d42-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97d42-111">-AsJob</span></span>
<span data-ttu-id="97d42-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97d42-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97d42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d42-113">-DefaultProfile</span></span>
<span data-ttu-id="97d42-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="97d42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97d42-115">-工期</span><span class="sxs-lookup"><span data-stu-id="97d42-115">-Duration</span></span>
<span data-ttu-id="97d42-116">持續時間</span><span class="sxs-lookup"><span data-stu-id="97d42-116">The duration</span></span>


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

### <span data-ttu-id="97d42-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="97d42-117">-ExpirationDateTime</span></span>
<span data-ttu-id="97d42-118">以 YYYY-MM-DD hh：mm 格式表示的排程到期日時間</span><span class="sxs-lookup"><span data-stu-id="97d42-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="97d42-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="97d42-119">-ExtensionProperty</span></span>
<span data-ttu-id="97d42-120">每個資源的擴充功能屬性。</span><span class="sxs-lookup"><span data-stu-id="97d42-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="97d42-121">-位置</span><span class="sxs-lookup"><span data-stu-id="97d42-121">-Location</span></span>
<span data-ttu-id="97d42-122">維護組組位置。</span><span class="sxs-lookup"><span data-stu-id="97d42-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="97d42-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="97d42-123">-MaintenanceScope</span></span>
<span data-ttu-id="97d42-124">維護範圍。</span><span class="sxs-lookup"><span data-stu-id="97d42-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="97d42-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="97d42-125">-Name</span></span>
<span data-ttu-id="97d42-126">維護組組名稱。</span><span class="sxs-lookup"><span data-stu-id="97d42-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="97d42-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="97d42-127">-RecurEvery</span></span>
<span data-ttu-id="97d42-128">排程週期</span><span class="sxs-lookup"><span data-stu-id="97d42-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="97d42-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97d42-129">-ResourceGroupName</span></span>
<span data-ttu-id="97d42-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="97d42-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="97d42-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="97d42-131">-StartDateTime</span></span>
<span data-ttu-id="97d42-132">排程的 StartDateTime 格式為 YYYY-MM-DD hh：mm</span><span class="sxs-lookup"><span data-stu-id="97d42-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="97d42-133">-標記</span><span class="sxs-lookup"><span data-stu-id="97d42-133">-Tag</span></span>
<span data-ttu-id="97d42-134">ARM 標記。</span><span class="sxs-lookup"><span data-stu-id="97d42-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="97d42-135">-時區</span><span class="sxs-lookup"><span data-stu-id="97d42-135">-Timezone</span></span>
<span data-ttu-id="97d42-136">時區</span><span class="sxs-lookup"><span data-stu-id="97d42-136">The timezone</span></span>

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

### <span data-ttu-id="97d42-137">-可見度</span><span class="sxs-lookup"><span data-stu-id="97d42-137">-Visibility</span></span>
<span data-ttu-id="97d42-138">範圍可見度</span><span class="sxs-lookup"><span data-stu-id="97d42-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="97d42-139">-確認</span><span class="sxs-lookup"><span data-stu-id="97d42-139">-Confirm</span></span>
<span data-ttu-id="97d42-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="97d42-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97d42-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97d42-141">-WhatIf</span></span>
<span data-ttu-id="97d42-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97d42-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97d42-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97d42-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97d42-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d42-144">CommonParameters</span></span>
<span data-ttu-id="97d42-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="97d42-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d42-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97d42-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d42-147">輸入</span><span class="sxs-lookup"><span data-stu-id="97d42-147">INPUTS</span></span>

### <span data-ttu-id="97d42-148">System.String</span><span class="sxs-lookup"><span data-stu-id="97d42-148">System.String</span></span>

## <span data-ttu-id="97d42-149">輸出</span><span class="sxs-lookup"><span data-stu-id="97d42-149">OUTPUTS</span></span>

### <span data-ttu-id="97d42-150">Microsoft.Azure.Commands.Maintenance.models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="97d42-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="97d42-151">筆記</span><span class="sxs-lookup"><span data-stu-id="97d42-151">NOTES</span></span>

## <span data-ttu-id="97d42-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="97d42-152">RELATED LINKS</span></span>
