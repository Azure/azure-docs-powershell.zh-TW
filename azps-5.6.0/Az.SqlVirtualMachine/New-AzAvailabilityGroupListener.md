---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: f187a2704ed1f23d6cc5ac7dded1c8d9cd8ae954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916467"
---
# <span data-ttu-id="d2a10-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="d2a10-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="d2a10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2a10-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a10-103">建立新的可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="d2a10-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="d2a10-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2a10-104">SYNTAX</span></span>

### <span data-ttu-id="d2a10-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="d2a10-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2a10-106">SqlObject</span><span class="sxs-lookup"><span data-stu-id="d2a10-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a10-107">描述</span><span class="sxs-lookup"><span data-stu-id="d2a10-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a10-108">Cmdlet New-AzAvailabilityGroupListener會建立新的可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="d2a10-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="d2a10-109">例子</span><span class="sxs-lookup"><span data-stu-id="d2a10-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a10-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d2a10-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="d2a10-111">名稱 ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a10-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d2a10-112">AgListener01 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d2a10-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d2a10-113">在 SQL 虛擬機器群組 Sql MachineGroup01 中為可用性群組 AvailabilityGroup01 建立新的可用性群組聆聽者 AgListener01。</span><span class="sxs-lookup"><span data-stu-id="d2a10-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="d2a10-114">參數</span><span class="sxs-lookup"><span data-stu-id="d2a10-114">PARAMETERS</span></span>

### <span data-ttu-id="d2a10-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2a10-115">-AsJob</span></span>
<span data-ttu-id="d2a10-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2a10-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d2a10-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a10-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="d2a10-118">可用性組名。</span><span class="sxs-lookup"><span data-stu-id="d2a10-118">Availability Group name.</span></span>

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

### <span data-ttu-id="d2a10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a10-119">-DefaultProfile</span></span>
<span data-ttu-id="d2a10-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2a10-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a10-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="d2a10-121">-IpAddress</span></span>
<span data-ttu-id="d2a10-122">私人 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="d2a10-122">Private Ip Address</span></span>

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

### <span data-ttu-id="d2a10-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a10-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="d2a10-124">負載平衡器識別碼</span><span class="sxs-lookup"><span data-stu-id="d2a10-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="d2a10-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2a10-125">-Name</span></span>
<span data-ttu-id="d2a10-126">可用性群組聆聽者名稱。</span><span class="sxs-lookup"><span data-stu-id="d2a10-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a10-127">-埠</span><span class="sxs-lookup"><span data-stu-id="d2a10-127">-Port</span></span>
<span data-ttu-id="d2a10-128">AG 聆聽者埠號碼。</span><span class="sxs-lookup"><span data-stu-id="d2a10-128">Port number of AG Listener.</span></span> <span data-ttu-id="d2a10-129">預設值為 1433。</span><span class="sxs-lookup"><span data-stu-id="d2a10-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a10-130">-PortPort</span><span class="sxs-lookup"><span data-stu-id="d2a10-130">-ProbePort</span></span>
<span data-ttu-id="d2a10-131">進位埠</span><span class="sxs-lookup"><span data-stu-id="d2a10-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a10-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a10-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="d2a10-133">公用 Ip 位址資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d2a10-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="d2a10-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a10-134">-ResourceGroupName</span></span>
<span data-ttu-id="d2a10-135">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2a10-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="d2a10-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d2a10-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="d2a10-137">Sql VM 資源識別碼 清單</span><span class="sxs-lookup"><span data-stu-id="d2a10-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2a10-138">-SqlQLGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a10-138">-SqlVMGroupName</span></span>
<span data-ttu-id="d2a10-139">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="d2a10-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d2a10-140">-SqlEVGroupObject</span><span class="sxs-lookup"><span data-stu-id="d2a10-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="d2a10-141">SQL 虛擬機器群組物件。</span><span class="sxs-lookup"><span data-stu-id="d2a10-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="d2a10-142">-子網Id</span><span class="sxs-lookup"><span data-stu-id="d2a10-142">-SubnetId</span></span>
<span data-ttu-id="d2a10-143">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d2a10-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="d2a10-144">-確認</span><span class="sxs-lookup"><span data-stu-id="d2a10-144">-Confirm</span></span>
<span data-ttu-id="d2a10-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d2a10-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a10-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a10-146">-WhatIf</span></span>
<span data-ttu-id="d2a10-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2a10-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a10-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2a10-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a10-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a10-149">CommonParameters</span></span>
<span data-ttu-id="d2a10-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2a10-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a10-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a10-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a10-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d2a10-152">INPUTS</span></span>

### <span data-ttu-id="d2a10-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="d2a10-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d2a10-154">輸出</span><span class="sxs-lookup"><span data-stu-id="d2a10-154">OUTPUTS</span></span>

### <span data-ttu-id="d2a10-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d2a10-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="d2a10-156">筆記</span><span class="sxs-lookup"><span data-stu-id="d2a10-156">NOTES</span></span>

## <span data-ttu-id="d2a10-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2a10-157">RELATED LINKS</span></span>
