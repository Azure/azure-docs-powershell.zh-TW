---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127590"
---
# <span data-ttu-id="51b81-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="51b81-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="51b81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51b81-102">SYNOPSIS</span></span>
<span data-ttu-id="51b81-103">註冊資源的設定。</span><span class="sxs-lookup"><span data-stu-id="51b81-103">Register configuration for resource.</span></span>

## <span data-ttu-id="51b81-104">句法</span><span class="sxs-lookup"><span data-stu-id="51b81-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51b81-105">說明</span><span class="sxs-lookup"><span data-stu-id="51b81-105">DESCRIPTION</span></span>
<span data-ttu-id="51b81-106">註冊資源的維護設定。</span><span class="sxs-lookup"><span data-stu-id="51b81-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="51b81-107">示例</span><span class="sxs-lookup"><span data-stu-id="51b81-107">EXAMPLES</span></span>

### <span data-ttu-id="51b81-108">範例1</span><span class="sxs-lookup"><span data-stu-id="51b81-108">Example 1</span></span>
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

<span data-ttu-id="51b81-109">註冊專用主機的維護設定。</span><span class="sxs-lookup"><span data-stu-id="51b81-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="51b81-110">參數</span><span class="sxs-lookup"><span data-stu-id="51b81-110">PARAMETERS</span></span>

### <span data-ttu-id="51b81-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51b81-111">-AsJob</span></span>
<span data-ttu-id="51b81-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="51b81-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51b81-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="51b81-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="51b81-114">配置作業名稱應該與 MaintenanceConfigurationName 相符。</span><span class="sxs-lookup"><span data-stu-id="51b81-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="51b81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b81-115">-DefaultProfile</span></span>
<span data-ttu-id="51b81-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51b81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b81-117">-位置</span><span class="sxs-lookup"><span data-stu-id="51b81-117">-Location</span></span>
<span data-ttu-id="51b81-118">資源不含空間的位置。</span><span class="sxs-lookup"><span data-stu-id="51b81-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="51b81-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="51b81-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="51b81-120">完全合格的 MaintenanceConfiguration。</span><span class="sxs-lookup"><span data-stu-id="51b81-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="51b81-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="51b81-121">-ProviderName</span></span>
<span data-ttu-id="51b81-122">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="51b81-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="51b81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b81-123">-ResourceGroupName</span></span>
<span data-ttu-id="51b81-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="51b81-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="51b81-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b81-125">-ResourceId</span></span>
<span data-ttu-id="51b81-126">配置作業名稱應該與 MaintenanceConfigurationName 相符。</span><span class="sxs-lookup"><span data-stu-id="51b81-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="51b81-127">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="51b81-127">-ResourceName</span></span>
<span data-ttu-id="51b81-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="51b81-128">The resource name.</span></span>

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

### <span data-ttu-id="51b81-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="51b81-129">-ResourceParentName</span></span>
<span data-ttu-id="51b81-130">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="51b81-130">The parent resource name.</span></span>

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

### <span data-ttu-id="51b81-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="51b81-131">-ResourceParentType</span></span>
<span data-ttu-id="51b81-132">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="51b81-132">The parent resource type.</span></span>

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

### <span data-ttu-id="51b81-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="51b81-133">-ResourceType</span></span>
<span data-ttu-id="51b81-134">資源類型。</span><span class="sxs-lookup"><span data-stu-id="51b81-134">The resource type.</span></span>

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

### <span data-ttu-id="51b81-135">-確認</span><span class="sxs-lookup"><span data-stu-id="51b81-135">-Confirm</span></span>
<span data-ttu-id="51b81-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="51b81-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b81-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b81-137">-WhatIf</span></span>
<span data-ttu-id="51b81-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51b81-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b81-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51b81-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b81-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b81-140">CommonParameters</span></span>
<span data-ttu-id="51b81-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51b81-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b81-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="51b81-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b81-143">輸入</span><span class="sxs-lookup"><span data-stu-id="51b81-143">INPUTS</span></span>

### <span data-ttu-id="51b81-144">System.object</span><span class="sxs-lookup"><span data-stu-id="51b81-144">System.String</span></span>

## <span data-ttu-id="51b81-145">輸出</span><span class="sxs-lookup"><span data-stu-id="51b81-145">OUTPUTS</span></span>

### <span data-ttu-id="51b81-146">PSConfigurationAssignment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="51b81-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="51b81-147">筆記</span><span class="sxs-lookup"><span data-stu-id="51b81-147">NOTES</span></span>

## <span data-ttu-id="51b81-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="51b81-148">RELATED LINKS</span></span>