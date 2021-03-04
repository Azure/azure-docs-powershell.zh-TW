---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: c94f1e842697a64dd95f7d5ccb90e389484a61e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905734"
---
# <span data-ttu-id="87b96-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="87b96-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="87b96-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87b96-102">SYNOPSIS</span></span>
<span data-ttu-id="87b96-103">更新可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="87b96-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="87b96-104">語法</span><span class="sxs-lookup"><span data-stu-id="87b96-104">SYNTAX</span></span>

### <span data-ttu-id="87b96-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="87b96-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87b96-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="87b96-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87b96-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b96-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b96-108">SqlObject</span><span class="sxs-lookup"><span data-stu-id="87b96-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b96-109">描述</span><span class="sxs-lookup"><span data-stu-id="87b96-109">DESCRIPTION</span></span>
<span data-ttu-id="87b96-110">此Update-AzAvailabilityGroupListener Cmdlet 會更新可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="87b96-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="87b96-111">例子</span><span class="sxs-lookup"><span data-stu-id="87b96-111">EXAMPLES</span></span>

### <span data-ttu-id="87b96-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="87b96-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="87b96-113">名稱 ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="87b96-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="87b96-114">AgListener01 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="87b96-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="87b96-115">更新可用性群組聆聽者的清單 SQL 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="87b96-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="87b96-116">參數</span><span class="sxs-lookup"><span data-stu-id="87b96-116">PARAMETERS</span></span>

### <span data-ttu-id="87b96-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87b96-117">-AsJob</span></span>
<span data-ttu-id="87b96-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87b96-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="87b96-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b96-119">-DefaultProfile</span></span>
<span data-ttu-id="87b96-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="87b96-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b96-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87b96-121">-InputObject</span></span>
<span data-ttu-id="87b96-122">可用性群組聆聽者物件。</span><span class="sxs-lookup"><span data-stu-id="87b96-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="87b96-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="87b96-123">-Name</span></span>
<span data-ttu-id="87b96-124">可用性群組聆聽者名稱。</span><span class="sxs-lookup"><span data-stu-id="87b96-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="87b96-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b96-125">-ResourceGroupName</span></span>
<span data-ttu-id="87b96-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87b96-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="87b96-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b96-127">-ResourceId</span></span>
<span data-ttu-id="87b96-128">可用性群組聆聽者資源識別碼</span><span class="sxs-lookup"><span data-stu-id="87b96-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b96-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="87b96-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="87b96-130">Sql VM 資源識別碼 清單</span><span class="sxs-lookup"><span data-stu-id="87b96-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b96-131">-SqlQLGroupName</span><span class="sxs-lookup"><span data-stu-id="87b96-131">-SqlVMGroupName</span></span>
<span data-ttu-id="87b96-132">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="87b96-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="87b96-133">-SqlEVGroupObject</span><span class="sxs-lookup"><span data-stu-id="87b96-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="87b96-134">SQL 虛擬機器群組物件。</span><span class="sxs-lookup"><span data-stu-id="87b96-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="87b96-135">-確認</span><span class="sxs-lookup"><span data-stu-id="87b96-135">-Confirm</span></span>
<span data-ttu-id="87b96-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="87b96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b96-137">-WhatIf</span></span>
<span data-ttu-id="87b96-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87b96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b96-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87b96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b96-140">CommonParameters</span></span>
<span data-ttu-id="87b96-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87b96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b96-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87b96-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b96-143">輸入</span><span class="sxs-lookup"><span data-stu-id="87b96-143">INPUTS</span></span>

### <span data-ttu-id="87b96-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="87b96-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="87b96-145">System.String</span><span class="sxs-lookup"><span data-stu-id="87b96-145">System.String</span></span>

### <span data-ttu-id="87b96-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="87b96-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="87b96-147">輸出</span><span class="sxs-lookup"><span data-stu-id="87b96-147">OUTPUTS</span></span>

### <span data-ttu-id="87b96-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="87b96-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="87b96-149">筆記</span><span class="sxs-lookup"><span data-stu-id="87b96-149">NOTES</span></span>

## <span data-ttu-id="87b96-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="87b96-150">RELATED LINKS</span></span>
