---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: a7ff8df963f7d1d58256ab40cf5788e81b49a23c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912250"
---
# <span data-ttu-id="8a567-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="8a567-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="8a567-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a567-102">SYNOPSIS</span></span>
<span data-ttu-id="8a567-103">獲得一或多個 sql 虛擬機器群組。</span><span class="sxs-lookup"><span data-stu-id="8a567-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8a567-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a567-104">SYNTAX</span></span>

### <span data-ttu-id="8a567-105">ResourceGroupOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="8a567-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a567-106">名字</span><span class="sxs-lookup"><span data-stu-id="8a567-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a567-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a567-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a567-108">描述</span><span class="sxs-lookup"><span data-stu-id="8a567-108">DESCRIPTION</span></span>
<span data-ttu-id="8a567-109">Cmdlet Get-AzSqlVMGroup一或多個 sql 虛擬機器群組。</span><span class="sxs-lookup"><span data-stu-id="8a567-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8a567-110">例子</span><span class="sxs-lookup"><span data-stu-id="8a567-110">EXAMPLES</span></span>

### <span data-ttu-id="8a567-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8a567-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="8a567-112">此命令會獲得目前訂閱中所有 Azure SQL 虛擬機器群組的資訊。</span><span class="sxs-lookup"><span data-stu-id="8a567-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="8a567-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="8a567-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8a567-114">此命令會獲得目前訂閱中指派給資源群組 ResourceGroup01 的所有 Azure SQL 虛擬機器群組相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8a567-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8a567-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="8a567-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8a567-116">此命令會獲得指派給資源群組 ResourceGroup01 的 SQL 虛擬機器群組「測試群組」相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8a567-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8a567-117">參數</span><span class="sxs-lookup"><span data-stu-id="8a567-117">PARAMETERS</span></span>

### <span data-ttu-id="8a567-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a567-118">-DefaultProfile</span></span>
<span data-ttu-id="8a567-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a567-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a567-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a567-120">-Name</span></span>
<span data-ttu-id="8a567-121">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="8a567-121">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a567-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a567-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a567-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a567-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="8a567-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a567-124">-ResourceId</span></span>
<span data-ttu-id="8a567-125">SQL 虛擬機器群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a567-125">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a567-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a567-126">CommonParameters</span></span>
<span data-ttu-id="8a567-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a567-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a567-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a567-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a567-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8a567-129">INPUTS</span></span>

### <span data-ttu-id="8a567-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8a567-130">System.String</span></span>

## <span data-ttu-id="8a567-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8a567-131">OUTPUTS</span></span>

### <span data-ttu-id="8a567-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="8a567-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8a567-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8a567-133">NOTES</span></span>

## <span data-ttu-id="8a567-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a567-134">RELATED LINKS</span></span>
