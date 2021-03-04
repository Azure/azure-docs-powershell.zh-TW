---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 993c1968d144a5a1a56a0bd3dff46a9920a90264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917150"
---
# <span data-ttu-id="f1ed7-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f1ed7-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="f1ed7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ed7-103">註冊資源的組配置。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-103">Register configuration for resource.</span></span>

## <span data-ttu-id="f1ed7-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1ed7-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1ed7-105">描述</span><span class="sxs-lookup"><span data-stu-id="f1ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ed7-106">註冊資源的維護組配置。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="f1ed7-107">例子</span><span class="sxs-lookup"><span data-stu-id="f1ed7-107">EXAMPLES</span></span>

### <span data-ttu-id="f1ed7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f1ed7-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="f1ed7-109">註冊專用主機的維護組配置。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="f1ed7-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1ed7-110">PARAMETERS</span></span>

### <span data-ttu-id="f1ed7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1ed7-111">-AsJob</span></span>
<span data-ttu-id="f1ed7-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1ed7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1ed7-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f1ed7-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="f1ed7-114">組組指派名稱應符合 MaintenanceConfigurationName。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ed7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ed7-115">-DefaultProfile</span></span>
<span data-ttu-id="f1ed7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ed7-117">-位置</span><span class="sxs-lookup"><span data-stu-id="f1ed7-117">-Location</span></span>
<span data-ttu-id="f1ed7-118">資源不含空格的位置。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-118">The location without spaces for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ed7-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f1ed7-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="f1ed7-120">完全合格的維護設定檔。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-120">The fully qualified MaintenanceConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ed7-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f1ed7-121">-ProviderName</span></span>
<span data-ttu-id="f1ed7-122">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="f1ed7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ed7-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1ed7-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="f1ed7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1ed7-125">-ResourceId</span></span>
<span data-ttu-id="f1ed7-126">組組指派名稱應符合 MaintenanceConfigurationName。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f1ed7-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f1ed7-127">-ResourceName</span></span>
<span data-ttu-id="f1ed7-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-128">The resource name.</span></span>

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

### <span data-ttu-id="f1ed7-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f1ed7-129">-ResourceParentName</span></span>
<span data-ttu-id="f1ed7-130">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-130">The parent resource name.</span></span>

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

### <span data-ttu-id="f1ed7-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f1ed7-131">-ResourceParentType</span></span>
<span data-ttu-id="f1ed7-132">父資源類型。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-132">The parent resource type.</span></span>

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

### <span data-ttu-id="f1ed7-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f1ed7-133">-ResourceType</span></span>
<span data-ttu-id="f1ed7-134">資源類型。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-134">The resource type.</span></span>

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

### <span data-ttu-id="f1ed7-135">-確認</span><span class="sxs-lookup"><span data-stu-id="f1ed7-135">-Confirm</span></span>
<span data-ttu-id="f1ed7-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ed7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ed7-137">-WhatIf</span></span>
<span data-ttu-id="f1ed7-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ed7-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ed7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ed7-140">CommonParameters</span></span>
<span data-ttu-id="f1ed7-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1ed7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ed7-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1ed7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ed7-143">輸入</span><span class="sxs-lookup"><span data-stu-id="f1ed7-143">INPUTS</span></span>

### <span data-ttu-id="f1ed7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f1ed7-144">System.String</span></span>

## <span data-ttu-id="f1ed7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f1ed7-145">OUTPUTS</span></span>

### <span data-ttu-id="f1ed7-146">Microsoft.Azure.Commands.Maintenance.models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f1ed7-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="f1ed7-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f1ed7-147">NOTES</span></span>

## <span data-ttu-id="f1ed7-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1ed7-148">RELATED LINKS</span></span>
