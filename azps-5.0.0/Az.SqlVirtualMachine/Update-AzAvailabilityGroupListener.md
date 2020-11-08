---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137965"
---
# <span data-ttu-id="a74f0-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="a74f0-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="a74f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a74f0-102">SYNOPSIS</span></span>
<span data-ttu-id="a74f0-103">更新可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a74f0-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="a74f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a74f0-104">SYNTAX</span></span>

### <span data-ttu-id="a74f0-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="a74f0-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a74f0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a74f0-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a74f0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a74f0-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a74f0-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="a74f0-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a74f0-109">說明</span><span class="sxs-lookup"><span data-stu-id="a74f0-109">DESCRIPTION</span></span>
<span data-ttu-id="a74f0-110">Update-AzAvailabilityGroupListener Cmdlet 會更新可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a74f0-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="a74f0-111">示例</span><span class="sxs-lookup"><span data-stu-id="a74f0-111">EXAMPLES</span></span>

### <span data-ttu-id="a74f0-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a74f0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="a74f0-113">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a74f0-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a74f0-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a74f0-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="a74f0-115">更新可用性群組偵聽程式的清單 SQL 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a74f0-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="a74f0-116">參數</span><span class="sxs-lookup"><span data-stu-id="a74f0-116">PARAMETERS</span></span>

### <span data-ttu-id="a74f0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a74f0-117">-AsJob</span></span>
<span data-ttu-id="a74f0-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a74f0-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a74f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74f0-119">-DefaultProfile</span></span>
<span data-ttu-id="a74f0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a74f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a74f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a74f0-121">-InputObject</span></span>
<span data-ttu-id="a74f0-122">可用性群組偵聽程式物件。</span><span class="sxs-lookup"><span data-stu-id="a74f0-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="a74f0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a74f0-123">-Name</span></span>
<span data-ttu-id="a74f0-124">可用性群組偵聽程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a74f0-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="a74f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="a74f0-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a74f0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="a74f0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a74f0-127">-ResourceId</span></span>
<span data-ttu-id="a74f0-128">可用性群組攔截器資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a74f0-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="a74f0-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a74f0-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="a74f0-130">Sql VM 資源識別碼清單</span><span class="sxs-lookup"><span data-stu-id="a74f0-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="a74f0-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="a74f0-131">-SqlVMGroupName</span></span>
<span data-ttu-id="a74f0-132">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="a74f0-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="a74f0-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="a74f0-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="a74f0-134">[SQL 虛擬機器群組] 物件。</span><span class="sxs-lookup"><span data-stu-id="a74f0-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="a74f0-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a74f0-135">-Confirm</span></span>
<span data-ttu-id="a74f0-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a74f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a74f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74f0-137">-WhatIf</span></span>
<span data-ttu-id="a74f0-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a74f0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a74f0-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a74f0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a74f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74f0-140">CommonParameters</span></span>
<span data-ttu-id="a74f0-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a74f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74f0-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a74f0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74f0-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a74f0-143">INPUTS</span></span>

### <span data-ttu-id="a74f0-144">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="a74f0-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="a74f0-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a74f0-145">System.String</span></span>

### <span data-ttu-id="a74f0-146">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="a74f0-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="a74f0-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a74f0-147">OUTPUTS</span></span>

### <span data-ttu-id="a74f0-148">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="a74f0-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="a74f0-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a74f0-149">NOTES</span></span>

## <span data-ttu-id="a74f0-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a74f0-150">RELATED LINKS</span></span>