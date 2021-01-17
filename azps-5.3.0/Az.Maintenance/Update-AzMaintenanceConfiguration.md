---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439227"
---
# <span data-ttu-id="a7f30-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7f30-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="a7f30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7f30-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f30-103">修補程式配置記錄</span><span class="sxs-lookup"><span data-stu-id="a7f30-103">Patch configuration record</span></span>

## <span data-ttu-id="a7f30-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7f30-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f30-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7f30-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f30-106">修補程式維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="a7f30-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="a7f30-107">示例</span><span class="sxs-lookup"><span data-stu-id="a7f30-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f30-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a7f30-108">Example 1</span></span>
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

<span data-ttu-id="a7f30-109">修補程式維護配置記錄</span><span class="sxs-lookup"><span data-stu-id="a7f30-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="a7f30-110">參數</span><span class="sxs-lookup"><span data-stu-id="a7f30-110">PARAMETERS</span></span>

### <span data-ttu-id="a7f30-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f30-111">-AsJob</span></span>
<span data-ttu-id="a7f30-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a7f30-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7f30-113">-配置</span><span class="sxs-lookup"><span data-stu-id="a7f30-113">-Configuration</span></span>
<span data-ttu-id="a7f30-114">要更新的維護設定。</span><span class="sxs-lookup"><span data-stu-id="a7f30-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="a7f30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f30-115">-DefaultProfile</span></span>
<span data-ttu-id="a7f30-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7f30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f30-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7f30-117">-Name</span></span>
<span data-ttu-id="a7f30-118">維護配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a7f30-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="a7f30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f30-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7f30-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7f30-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="a7f30-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a7f30-121">-Confirm</span></span>
<span data-ttu-id="a7f30-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7f30-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f30-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f30-123">-WhatIf</span></span>
<span data-ttu-id="a7f30-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7f30-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f30-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7f30-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f30-126">CommonParameters</span></span>
<span data-ttu-id="a7f30-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7f30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f30-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a7f30-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f30-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a7f30-129">INPUTS</span></span>

### <span data-ttu-id="a7f30-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a7f30-130">System.String</span></span>

### <span data-ttu-id="a7f30-131">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7f30-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="a7f30-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a7f30-132">OUTPUTS</span></span>

### <span data-ttu-id="a7f30-133">PSMaintenanceConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a7f30-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="a7f30-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a7f30-134">NOTES</span></span>

## <span data-ttu-id="a7f30-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7f30-135">RELATED LINKS</span></span>
