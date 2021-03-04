---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: d2131d542d845e065e1aae05a272b045ffa882f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910462"
---
# <span data-ttu-id="bb0dc-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb0dc-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="bb0dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0dc-103">修補程式組組記錄</span><span class="sxs-lookup"><span data-stu-id="bb0dc-103">Patch configuration record</span></span>

## <span data-ttu-id="bb0dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb0dc-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb0dc-105">描述</span><span class="sxs-lookup"><span data-stu-id="bb0dc-105">DESCRIPTION</span></span>
<span data-ttu-id="bb0dc-106">修補程式維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="bb0dc-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="bb0dc-107">例子</span><span class="sxs-lookup"><span data-stu-id="bb0dc-107">EXAMPLES</span></span>

### <span data-ttu-id="bb0dc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="bb0dc-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="bb0dc-109">修補程式維護組組記錄</span><span class="sxs-lookup"><span data-stu-id="bb0dc-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="bb0dc-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb0dc-110">PARAMETERS</span></span>

### <span data-ttu-id="bb0dc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb0dc-111">-AsJob</span></span>
<span data-ttu-id="bb0dc-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bb0dc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb0dc-113">-組式</span><span class="sxs-lookup"><span data-stu-id="bb0dc-113">-Configuration</span></span>
<span data-ttu-id="bb0dc-114">要更新的維護組配置。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0dc-115">-DefaultProfile</span></span>
<span data-ttu-id="bb0dc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb0dc-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb0dc-117">-Name</span></span>
<span data-ttu-id="bb0dc-118">維護組組名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="bb0dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb0dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb0dc-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="bb0dc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="bb0dc-121">-Confirm</span></span>
<span data-ttu-id="bb0dc-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb0dc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb0dc-123">-WhatIf</span></span>
<span data-ttu-id="bb0dc-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb0dc-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb0dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0dc-126">CommonParameters</span></span>
<span data-ttu-id="bb0dc-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb0dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0dc-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb0dc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0dc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bb0dc-129">INPUTS</span></span>

### <span data-ttu-id="bb0dc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bb0dc-130">System.String</span></span>

### <span data-ttu-id="bb0dc-131">Microsoft.Azure.Commands.Maintenance.models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb0dc-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="bb0dc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bb0dc-132">OUTPUTS</span></span>

### <span data-ttu-id="bb0dc-133">Microsoft.Azure.Commands.Maintenance.models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb0dc-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="bb0dc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="bb0dc-134">NOTES</span></span>

## <span data-ttu-id="bb0dc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb0dc-135">RELATED LINKS</span></span>
