---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: 56891d1dae20f89289b9c2f72bf87bfeed7bd347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908434"
---
# <span data-ttu-id="e8e98-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="e8e98-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="e8e98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8e98-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e98-103">刪除可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="e8e98-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="e8e98-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8e98-104">SYNTAX</span></span>

### <span data-ttu-id="e8e98-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="e8e98-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e98-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e98-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e98-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e98-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e98-108">SqlObject</span><span class="sxs-lookup"><span data-stu-id="e8e98-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8e98-109">描述</span><span class="sxs-lookup"><span data-stu-id="e8e98-109">DESCRIPTION</span></span>
<span data-ttu-id="e8e98-110">此Remove-AzAvailabilityGroupListener Cmdlet 會刪除可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="e8e98-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="e8e98-111">例子</span><span class="sxs-lookup"><span data-stu-id="e8e98-111">EXAMPLES</span></span>

### <span data-ttu-id="e8e98-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="e8e98-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="e8e98-113">名稱 ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e98-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="e8e98-114">AgListener01 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="e8e98-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="e8e98-115">刪除可用性群組 Availability Group AvailabilityGroup01 中的可用性群組聆聽者 AgListener01。</span><span class="sxs-lookup"><span data-stu-id="e8e98-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="e8e98-116">參數</span><span class="sxs-lookup"><span data-stu-id="e8e98-116">PARAMETERS</span></span>

### <span data-ttu-id="e8e98-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8e98-117">-AsJob</span></span>
<span data-ttu-id="e8e98-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8e98-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e8e98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e98-119">-DefaultProfile</span></span>
<span data-ttu-id="e8e98-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8e98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e98-121">-InputObject</span></span>
<span data-ttu-id="e8e98-122">可用性群組聆聽者物件。</span><span class="sxs-lookup"><span data-stu-id="e8e98-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e98-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8e98-123">-Name</span></span>
<span data-ttu-id="e8e98-124">可用性群組聆聽者名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e98-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8e98-125">-PassThru</span></span>
<span data-ttu-id="e8e98-126">指定是否要在 Cmdlet 執行結束時輸出已刪除的資源。</span><span class="sxs-lookup"><span data-stu-id="e8e98-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="e8e98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e98-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8e98-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e98-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e98-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e98-129">-ResourceId</span></span>
<span data-ttu-id="e8e98-130">可用性群組聆聽者資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8e98-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e98-131">-SqlQLGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e98-131">-SqlVMGroupName</span></span>
<span data-ttu-id="e8e98-132">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="e8e98-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e98-133">-SqlEVGroupObject</span><span class="sxs-lookup"><span data-stu-id="e8e98-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="e8e98-134">SQL 虛擬機器群組物件。</span><span class="sxs-lookup"><span data-stu-id="e8e98-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e98-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e8e98-135">-Confirm</span></span>
<span data-ttu-id="e8e98-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e8e98-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e98-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e98-137">-WhatIf</span></span>
<span data-ttu-id="e8e98-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8e98-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8e98-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8e98-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e98-140">CommonParameters</span></span>
<span data-ttu-id="e8e98-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8e98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e98-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8e98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e98-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e8e98-143">INPUTS</span></span>

### <span data-ttu-id="e8e98-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="e8e98-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="e8e98-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e8e98-145">System.String</span></span>

### <span data-ttu-id="e8e98-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="e8e98-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e8e98-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e8e98-147">OUTPUTS</span></span>

### <span data-ttu-id="e8e98-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="e8e98-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="e8e98-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e8e98-149">NOTES</span></span>

## <span data-ttu-id="e8e98-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8e98-150">RELATED LINKS</span></span>
