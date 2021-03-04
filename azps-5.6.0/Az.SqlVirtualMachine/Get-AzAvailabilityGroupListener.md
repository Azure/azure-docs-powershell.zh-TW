---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: be20b280dccccae6f6afcc1a18514ad3dfb89ba2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916468"
---
# <span data-ttu-id="b902b-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="b902b-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="b902b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b902b-102">SYNOPSIS</span></span>
<span data-ttu-id="b902b-103">在 SQL 虛擬機器群組中取得一或多個可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="b902b-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="b902b-104">語法</span><span class="sxs-lookup"><span data-stu-id="b902b-104">SYNTAX</span></span>

### <span data-ttu-id="b902b-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="b902b-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b902b-106">SqlObject</span><span class="sxs-lookup"><span data-stu-id="b902b-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b902b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b902b-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b902b-108">描述</span><span class="sxs-lookup"><span data-stu-id="b902b-108">DESCRIPTION</span></span>
<span data-ttu-id="b902b-109">此Get-AzAvailabilityGroupListener會從 SQL 虛擬機器群組中，獲得一或多個可用性群組聆聽者。</span><span class="sxs-lookup"><span data-stu-id="b902b-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="b902b-110">例子</span><span class="sxs-lookup"><span data-stu-id="b902b-110">EXAMPLES</span></span>

### <span data-ttu-id="b902b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b902b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="b902b-112">名稱 ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="b902b-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="b902b-113">AgListener01 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="b902b-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="b902b-114">此命令會獲得 SQL 虛擬機器群組 Sql Virtual MachineGroup01 和資源群組 ResourceGroup01 中可用性群組聆聽者 AgListener01 的資訊。</span><span class="sxs-lookup"><span data-stu-id="b902b-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="b902b-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="b902b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="b902b-116">名稱 ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="b902b-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="b902b-117">AgListener01 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="b902b-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="b902b-118">此命令會獲得 SQL 虛擬機器群組 SqlEvGroup01 和資源群組 ResourceGroup01 中所有可用性群組聆聽者的資訊。</span><span class="sxs-lookup"><span data-stu-id="b902b-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="b902b-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="b902b-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="b902b-120">名稱 ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="b902b-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="b902b-121">AgListener01 ResourceGroup01 SqlEvGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="b902b-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="b902b-122">參數</span><span class="sxs-lookup"><span data-stu-id="b902b-122">PARAMETERS</span></span>

### <span data-ttu-id="b902b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b902b-123">-DefaultProfile</span></span>
<span data-ttu-id="b902b-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b902b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b902b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b902b-125">-Name</span></span>
<span data-ttu-id="b902b-126">可用性群組聆聽者名稱。</span><span class="sxs-lookup"><span data-stu-id="b902b-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b902b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b902b-127">-ResourceGroupName</span></span>
<span data-ttu-id="b902b-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b902b-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b902b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b902b-129">-ResourceId</span></span>
<span data-ttu-id="b902b-130">可用性群組聆聽者資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b902b-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="b902b-131">-SqlQLGroupName</span><span class="sxs-lookup"><span data-stu-id="b902b-131">-SqlVMGroupName</span></span>
<span data-ttu-id="b902b-132">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="b902b-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="b902b-133">-SqlEVGroupObject</span><span class="sxs-lookup"><span data-stu-id="b902b-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="b902b-134">SQL 虛擬機器群組物件。</span><span class="sxs-lookup"><span data-stu-id="b902b-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="b902b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b902b-135">CommonParameters</span></span>
<span data-ttu-id="b902b-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b902b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b902b-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b902b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b902b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b902b-138">INPUTS</span></span>

### <span data-ttu-id="b902b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b902b-139">System.String</span></span>

### <span data-ttu-id="b902b-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="b902b-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b902b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b902b-141">OUTPUTS</span></span>

### <span data-ttu-id="b902b-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="b902b-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="b902b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b902b-143">NOTES</span></span>

## <span data-ttu-id="b902b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b902b-144">RELATED LINKS</span></span>
