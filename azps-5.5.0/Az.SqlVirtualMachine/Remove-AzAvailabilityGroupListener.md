---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130638"
---
# <span data-ttu-id="3ed4b-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="3ed4b-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="3ed4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ed4b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed4b-103">刪除可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="3ed4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ed4b-104">SYNTAX</span></span>

### <span data-ttu-id="3ed4b-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="3ed4b-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ed4b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ed4b-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed4b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed4b-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed4b-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="3ed4b-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed4b-109">說明</span><span class="sxs-lookup"><span data-stu-id="3ed4b-109">DESCRIPTION</span></span>
<span data-ttu-id="3ed4b-110">Remove-AzAvailabilityGroupListener Cmdlet 會刪除可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="3ed4b-111">示例</span><span class="sxs-lookup"><span data-stu-id="3ed4b-111">EXAMPLES</span></span>

### <span data-ttu-id="3ed4b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3ed4b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="3ed4b-113">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed4b-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="3ed4b-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="3ed4b-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="3ed4b-115">刪除可用性群組 AvailabilityGroup01 中的可用性群組偵聽程式 AgListener01。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="3ed4b-116">參數</span><span class="sxs-lookup"><span data-stu-id="3ed4b-116">PARAMETERS</span></span>

### <span data-ttu-id="3ed4b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ed4b-117">-AsJob</span></span>
<span data-ttu-id="3ed4b-118">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3ed4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed4b-119">-DefaultProfile</span></span>
<span data-ttu-id="3ed4b-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ed4b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ed4b-121">-InputObject</span></span>
<span data-ttu-id="3ed4b-122">可用性群組偵聽程式物件。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="3ed4b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ed4b-123">-Name</span></span>
<span data-ttu-id="3ed4b-124">可用性群組偵聽程式名稱。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="3ed4b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ed4b-125">-PassThru</span></span>
<span data-ttu-id="3ed4b-126">指定是否要在 Cmdlet 執行結束時輸出已刪除的資源。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="3ed4b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed4b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ed4b-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ed4b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ed4b-129">-ResourceId</span></span>
<span data-ttu-id="3ed4b-130">可用性群組攔截器資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3ed4b-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="3ed4b-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed4b-131">-SqlVMGroupName</span></span>
<span data-ttu-id="3ed4b-132">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="3ed4b-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="3ed4b-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="3ed4b-134">[SQL 虛擬機器群組] 物件。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="3ed4b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="3ed4b-135">-Confirm</span></span>
<span data-ttu-id="3ed4b-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed4b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed4b-137">-WhatIf</span></span>
<span data-ttu-id="3ed4b-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed4b-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed4b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed4b-140">CommonParameters</span></span>
<span data-ttu-id="3ed4b-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed4b-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ed4b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed4b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3ed4b-143">INPUTS</span></span>

### <span data-ttu-id="3ed4b-144">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="3ed4b-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="3ed4b-145">System.object</span><span class="sxs-lookup"><span data-stu-id="3ed4b-145">System.String</span></span>

### <span data-ttu-id="3ed4b-146">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="3ed4b-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="3ed4b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="3ed4b-147">OUTPUTS</span></span>

### <span data-ttu-id="3ed4b-148">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="3ed4b-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="3ed4b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="3ed4b-149">NOTES</span></span>

## <span data-ttu-id="3ed4b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ed4b-150">RELATED LINKS</span></span>
