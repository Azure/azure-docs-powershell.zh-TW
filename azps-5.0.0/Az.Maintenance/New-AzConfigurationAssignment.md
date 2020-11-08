---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138798"
---
# <span data-ttu-id="b5116-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b5116-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="b5116-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5116-102">SYNOPSIS</span></span>
<span data-ttu-id="b5116-103">註冊資源的設定。</span><span class="sxs-lookup"><span data-stu-id="b5116-103">Register configuration for resource.</span></span>

## <span data-ttu-id="b5116-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5116-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5116-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5116-105">DESCRIPTION</span></span>
<span data-ttu-id="b5116-106">註冊資源的維護設定。</span><span class="sxs-lookup"><span data-stu-id="b5116-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="b5116-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5116-107">EXAMPLES</span></span>

### <span data-ttu-id="b5116-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b5116-108">Example 1</span></span>
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

<span data-ttu-id="b5116-109">註冊專用主機的維護設定。</span><span class="sxs-lookup"><span data-stu-id="b5116-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="b5116-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5116-110">PARAMETERS</span></span>

### <span data-ttu-id="b5116-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5116-111">-AsJob</span></span>
<span data-ttu-id="b5116-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5116-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5116-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b5116-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="b5116-114">配置作業名稱應該與 MaintenanceConfigurationName 相符。</span><span class="sxs-lookup"><span data-stu-id="b5116-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="b5116-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5116-115">-DefaultProfile</span></span>
<span data-ttu-id="b5116-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5116-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5116-117">-位置</span><span class="sxs-lookup"><span data-stu-id="b5116-117">-Location</span></span>
<span data-ttu-id="b5116-118">資源不含空間的位置。</span><span class="sxs-lookup"><span data-stu-id="b5116-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="b5116-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b5116-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="b5116-120">完全合格的 MaintenanceConfiguration。</span><span class="sxs-lookup"><span data-stu-id="b5116-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="b5116-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="b5116-121">-ProviderName</span></span>
<span data-ttu-id="b5116-122">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="b5116-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="b5116-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5116-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5116-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5116-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="b5116-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5116-125">-ResourceId</span></span>
<span data-ttu-id="b5116-126">配置作業名稱應該與 MaintenanceConfigurationName 相符。</span><span class="sxs-lookup"><span data-stu-id="b5116-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="b5116-127">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="b5116-127">-ResourceName</span></span>
<span data-ttu-id="b5116-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b5116-128">The resource name.</span></span>

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

### <span data-ttu-id="b5116-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="b5116-129">-ResourceParentName</span></span>
<span data-ttu-id="b5116-130">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b5116-130">The parent resource name.</span></span>

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

### <span data-ttu-id="b5116-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="b5116-131">-ResourceParentType</span></span>
<span data-ttu-id="b5116-132">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="b5116-132">The parent resource type.</span></span>

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

### <span data-ttu-id="b5116-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b5116-133">-ResourceType</span></span>
<span data-ttu-id="b5116-134">資源類型。</span><span class="sxs-lookup"><span data-stu-id="b5116-134">The resource type.</span></span>

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

### <span data-ttu-id="b5116-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b5116-135">-Confirm</span></span>
<span data-ttu-id="b5116-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5116-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5116-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5116-137">-WhatIf</span></span>
<span data-ttu-id="b5116-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5116-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5116-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5116-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5116-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5116-140">CommonParameters</span></span>
<span data-ttu-id="b5116-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5116-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5116-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5116-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5116-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b5116-143">INPUTS</span></span>

### <span data-ttu-id="b5116-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b5116-144">System.String</span></span>

## <span data-ttu-id="b5116-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b5116-145">OUTPUTS</span></span>

### <span data-ttu-id="b5116-146">PSConfigurationAssignment 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5116-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="b5116-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b5116-147">NOTES</span></span>

## <span data-ttu-id="b5116-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5116-148">RELATED LINKS</span></span>