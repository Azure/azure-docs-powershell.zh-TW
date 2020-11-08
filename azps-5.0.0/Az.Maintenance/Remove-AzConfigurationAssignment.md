---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138797"
---
# <span data-ttu-id="4a57e-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="4a57e-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="4a57e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a57e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a57e-103">登出資源的配置。</span><span class="sxs-lookup"><span data-stu-id="4a57e-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="4a57e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a57e-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a57e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a57e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a57e-106">登出資源的配置。</span><span class="sxs-lookup"><span data-stu-id="4a57e-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="4a57e-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a57e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a57e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4a57e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="4a57e-109">登出資源的配置。</span><span class="sxs-lookup"><span data-stu-id="4a57e-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="4a57e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a57e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a57e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a57e-111">-AsJob</span></span>
<span data-ttu-id="4a57e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4a57e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a57e-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="4a57e-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="4a57e-114">配置作業名稱。</span><span class="sxs-lookup"><span data-stu-id="4a57e-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="4a57e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a57e-115">-DefaultProfile</span></span>
<span data-ttu-id="4a57e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a57e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a57e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4a57e-117">-Force</span></span>
<span data-ttu-id="4a57e-118">強制移除而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a57e-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="4a57e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a57e-119">-PassThru</span></span>
<span data-ttu-id="4a57e-120">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="4a57e-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="4a57e-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4a57e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a57e-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4a57e-122">-ProviderName</span></span>
<span data-ttu-id="4a57e-123">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="4a57e-123">The resource provider Name.</span></span>

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

### <span data-ttu-id="4a57e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a57e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a57e-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a57e-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="4a57e-126">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="4a57e-126">-ResourceName</span></span>
<span data-ttu-id="4a57e-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4a57e-127">The resource name.</span></span>

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

### <span data-ttu-id="4a57e-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="4a57e-128">-ResourceParentName</span></span>
<span data-ttu-id="4a57e-129">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4a57e-129">The parent resource name.</span></span>

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

### <span data-ttu-id="4a57e-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="4a57e-130">-ResourceParentType</span></span>
<span data-ttu-id="4a57e-131">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="4a57e-131">The parent resource type.</span></span>

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

### <span data-ttu-id="4a57e-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4a57e-132">-ResourceType</span></span>
<span data-ttu-id="4a57e-133">資源類型。</span><span class="sxs-lookup"><span data-stu-id="4a57e-133">The resource type.</span></span>

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

### <span data-ttu-id="4a57e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="4a57e-134">-Confirm</span></span>
<span data-ttu-id="4a57e-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4a57e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a57e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a57e-136">-WhatIf</span></span>
<span data-ttu-id="4a57e-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a57e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a57e-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a57e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a57e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a57e-139">CommonParameters</span></span>
<span data-ttu-id="4a57e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a57e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a57e-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4a57e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a57e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="4a57e-142">INPUTS</span></span>

### <span data-ttu-id="4a57e-143">System.object</span><span class="sxs-lookup"><span data-stu-id="4a57e-143">System.String</span></span>

## <span data-ttu-id="4a57e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4a57e-144">OUTPUTS</span></span>

### <span data-ttu-id="4a57e-145">System.object</span><span class="sxs-lookup"><span data-stu-id="4a57e-145">System.Boolean</span></span>

## <span data-ttu-id="4a57e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4a57e-146">NOTES</span></span>

## <span data-ttu-id="4a57e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a57e-147">RELATED LINKS</span></span>
