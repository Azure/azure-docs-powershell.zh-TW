---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798070"
---
# <span data-ttu-id="a589f-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="a589f-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="a589f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a589f-102">SYNOPSIS</span></span>
<span data-ttu-id="a589f-103">在 SQL 虛擬電腦群組中取得一或多個可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a589f-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="a589f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a589f-104">SYNTAX</span></span>

### <span data-ttu-id="a589f-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="a589f-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a589f-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="a589f-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a589f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a589f-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a589f-108">說明</span><span class="sxs-lookup"><span data-stu-id="a589f-108">DESCRIPTION</span></span>
<span data-ttu-id="a589f-109">Get-AzAvailabilityGroupListener 從 SQL 虛擬電腦群組取得一或多個可用性群組偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a589f-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="a589f-110">示例</span><span class="sxs-lookup"><span data-stu-id="a589f-110">EXAMPLES</span></span>

### <span data-ttu-id="a589f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a589f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="a589f-112">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a589f-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a589f-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a589f-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="a589f-114">這個命令會在 SQL 虛擬電腦群組 SqlVmGroup01 和資源群組 ResourceGroup01 中取得可用性群組偵聽程式 AgListener01 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a589f-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="a589f-115">範例2</span><span class="sxs-lookup"><span data-stu-id="a589f-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="a589f-116">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a589f-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a589f-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a589f-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="a589f-118">這個命令會取得 SQL 虛擬機器群組 SqlVmGroup01 和資源群組 ResourceGroup01 中所有可用性群組偵聽程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a589f-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="a589f-119">範例3</span><span class="sxs-lookup"><span data-stu-id="a589f-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="a589f-120">Name ResourceGroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a589f-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a589f-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a589f-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="a589f-122">參數</span><span class="sxs-lookup"><span data-stu-id="a589f-122">PARAMETERS</span></span>

### <span data-ttu-id="a589f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a589f-123">-DefaultProfile</span></span>
<span data-ttu-id="a589f-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a589f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a589f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a589f-125">-Name</span></span>
<span data-ttu-id="a589f-126">可用性群組偵聽程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a589f-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="a589f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a589f-127">-ResourceGroupName</span></span>
<span data-ttu-id="a589f-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a589f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a589f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a589f-129">-ResourceId</span></span>
<span data-ttu-id="a589f-130">可用性群組攔截器資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a589f-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="a589f-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="a589f-131">-SqlVMGroupName</span></span>
<span data-ttu-id="a589f-132">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="a589f-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="a589f-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="a589f-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="a589f-134">[SQL 虛擬機器群組] 物件。</span><span class="sxs-lookup"><span data-stu-id="a589f-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="a589f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a589f-135">CommonParameters</span></span>
<span data-ttu-id="a589f-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a589f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a589f-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a589f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a589f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a589f-138">INPUTS</span></span>

### <span data-ttu-id="a589f-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a589f-139">System.String</span></span>

### <span data-ttu-id="a589f-140">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="a589f-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="a589f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a589f-141">OUTPUTS</span></span>

### <span data-ttu-id="a589f-142">SqlVirtualMachine SqlVirtualMachine. AzureAvailabilityGroupListenerModel （）</span><span class="sxs-lookup"><span data-stu-id="a589f-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="a589f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a589f-143">NOTES</span></span>

## <span data-ttu-id="a589f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a589f-144">RELATED LINKS</span></span>
