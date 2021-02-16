---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132979"
---
# <span data-ttu-id="bb243-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="bb243-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="bb243-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb243-102">SYNOPSIS</span></span>
<span data-ttu-id="bb243-103">更新可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="bb243-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="bb243-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb243-104">SYNTAX</span></span>

### <span data-ttu-id="bb243-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="bb243-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb243-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bb243-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb243-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb243-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb243-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="bb243-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb243-109">說明</span><span class="sxs-lookup"><span data-stu-id="bb243-109">DESCRIPTION</span></span>
<span data-ttu-id="bb243-110">Update-AzAvailabilityGroupListener Cmdlet 會更新可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="bb243-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="bb243-111">示例</span><span class="sxs-lookup"><span data-stu-id="bb243-111">EXAMPLES</span></span>

### <span data-ttu-id="bb243-112">範例1</span><span class="sxs-lookup"><span data-stu-id="bb243-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="bb243-113">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="bb243-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="bb243-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="bb243-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="bb243-115">更新可用性群組偵聽程式的清單 SQL 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bb243-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="bb243-116">參數</span><span class="sxs-lookup"><span data-stu-id="bb243-116">PARAMETERS</span></span>

### <span data-ttu-id="bb243-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb243-117">-AsJob</span></span>
<span data-ttu-id="bb243-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb243-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bb243-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb243-119">-DefaultProfile</span></span>
<span data-ttu-id="bb243-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb243-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb243-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb243-121">-InputObject</span></span>
<span data-ttu-id="bb243-122">可用性群組偵聽程式物件。</span><span class="sxs-lookup"><span data-stu-id="bb243-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="bb243-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb243-123">-Name</span></span>
<span data-ttu-id="bb243-124">可用性群組偵聽程式名稱。</span><span class="sxs-lookup"><span data-stu-id="bb243-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="bb243-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb243-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb243-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb243-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb243-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb243-127">-ResourceId</span></span>
<span data-ttu-id="bb243-128">可用性群組攔截器資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bb243-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="bb243-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="bb243-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="bb243-130">Sql VM 資源識別碼清單</span><span class="sxs-lookup"><span data-stu-id="bb243-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="bb243-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="bb243-131">-SqlVMGroupName</span></span>
<span data-ttu-id="bb243-132">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="bb243-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="bb243-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="bb243-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="bb243-134">[SQL 虛擬機器群組] 物件。</span><span class="sxs-lookup"><span data-stu-id="bb243-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="bb243-135">-確認</span><span class="sxs-lookup"><span data-stu-id="bb243-135">-Confirm</span></span>
<span data-ttu-id="bb243-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb243-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb243-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb243-137">-WhatIf</span></span>
<span data-ttu-id="bb243-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb243-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb243-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb243-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb243-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb243-140">CommonParameters</span></span>
<span data-ttu-id="bb243-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb243-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb243-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bb243-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb243-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bb243-143">INPUTS</span></span>

### <span data-ttu-id="bb243-144">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="bb243-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="bb243-145">System.object</span><span class="sxs-lookup"><span data-stu-id="bb243-145">System.String</span></span>

### <span data-ttu-id="bb243-146">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="bb243-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="bb243-147">輸出</span><span class="sxs-lookup"><span data-stu-id="bb243-147">OUTPUTS</span></span>

### <span data-ttu-id="bb243-148">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="bb243-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="bb243-149">筆記</span><span class="sxs-lookup"><span data-stu-id="bb243-149">NOTES</span></span>

## <span data-ttu-id="bb243-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb243-150">RELATED LINKS</span></span>
