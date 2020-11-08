---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968983"
---
# <span data-ttu-id="c1887-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="c1887-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="c1887-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1887-102">SYNOPSIS</span></span>
<span data-ttu-id="c1887-103">建立新的可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="c1887-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="c1887-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1887-104">SYNTAX</span></span>

### <span data-ttu-id="c1887-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="c1887-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1887-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="c1887-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1887-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1887-107">DESCRIPTION</span></span>
<span data-ttu-id="c1887-108">New-AzAvailabilityGroupListener Cmdlet 會建立新的可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="c1887-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="c1887-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1887-109">EXAMPLES</span></span>

### <span data-ttu-id="c1887-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c1887-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="c1887-111">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c1887-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="c1887-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="c1887-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="c1887-113">針對 SQL 虛擬電腦群組 SqlVmGroup01 中的可用性群組 AvailabilityGroup01 建立新的可用性群組偵聽程式 AgListener01。</span><span class="sxs-lookup"><span data-stu-id="c1887-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="c1887-114">參數</span><span class="sxs-lookup"><span data-stu-id="c1887-114">PARAMETERS</span></span>

### <span data-ttu-id="c1887-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1887-115">-AsJob</span></span>
<span data-ttu-id="c1887-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1887-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c1887-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c1887-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="c1887-118">可用性組名。</span><span class="sxs-lookup"><span data-stu-id="c1887-118">Availability Group name.</span></span>

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

### <span data-ttu-id="c1887-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1887-119">-DefaultProfile</span></span>
<span data-ttu-id="c1887-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1887-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1887-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c1887-121">-IpAddress</span></span>
<span data-ttu-id="c1887-122">私人 Ip 位址</span><span class="sxs-lookup"><span data-stu-id="c1887-122">Private Ip Address</span></span>

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

### <span data-ttu-id="c1887-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="c1887-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="c1887-124">負載平衡器識別碼</span><span class="sxs-lookup"><span data-stu-id="c1887-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="c1887-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1887-125">-Name</span></span>
<span data-ttu-id="c1887-126">可用性群組偵聽程式名稱。</span><span class="sxs-lookup"><span data-stu-id="c1887-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="c1887-127">-埠</span><span class="sxs-lookup"><span data-stu-id="c1887-127">-Port</span></span>
<span data-ttu-id="c1887-128">AG 偵聽程式的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="c1887-128">Port number of AG Listener.</span></span> <span data-ttu-id="c1887-129">預設值為1433。</span><span class="sxs-lookup"><span data-stu-id="c1887-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="c1887-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="c1887-130">-ProbePort</span></span>
<span data-ttu-id="c1887-131">探測埠</span><span class="sxs-lookup"><span data-stu-id="c1887-131">Probe Port</span></span>

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

### <span data-ttu-id="c1887-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="c1887-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="c1887-133">公用 Ip 位址資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c1887-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="c1887-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1887-134">-ResourceGroupName</span></span>
<span data-ttu-id="c1887-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1887-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="c1887-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c1887-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="c1887-137">Sql VM 資源識別碼清單</span><span class="sxs-lookup"><span data-stu-id="c1887-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="c1887-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="c1887-138">-SqlVMGroupName</span></span>
<span data-ttu-id="c1887-139">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="c1887-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="c1887-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="c1887-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="c1887-141">[SQL 虛擬機器群組] 物件。</span><span class="sxs-lookup"><span data-stu-id="c1887-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="c1887-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c1887-142">-SubnetId</span></span>
<span data-ttu-id="c1887-143">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c1887-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="c1887-144">-確認</span><span class="sxs-lookup"><span data-stu-id="c1887-144">-Confirm</span></span>
<span data-ttu-id="c1887-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1887-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1887-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1887-146">-WhatIf</span></span>
<span data-ttu-id="c1887-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1887-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1887-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1887-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1887-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1887-149">CommonParameters</span></span>
<span data-ttu-id="c1887-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1887-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1887-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c1887-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1887-152">輸入</span><span class="sxs-lookup"><span data-stu-id="c1887-152">INPUTS</span></span>

### <span data-ttu-id="c1887-153">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="c1887-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c1887-154">輸出</span><span class="sxs-lookup"><span data-stu-id="c1887-154">OUTPUTS</span></span>

### <span data-ttu-id="c1887-155">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="c1887-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="c1887-156">筆記</span><span class="sxs-lookup"><span data-stu-id="c1887-156">NOTES</span></span>

## <span data-ttu-id="c1887-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1887-157">RELATED LINKS</span></span>