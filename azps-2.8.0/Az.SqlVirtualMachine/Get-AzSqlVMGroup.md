---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: 1d6c7ef54248258fc6a641dc6c917866163bd52a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792851"
---
# <span data-ttu-id="f874b-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="f874b-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="f874b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f874b-102">SYNOPSIS</span></span>
<span data-ttu-id="f874b-103">取得一或多個 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="f874b-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="f874b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f874b-104">SYNTAX</span></span>

### <span data-ttu-id="f874b-105">ResourceGroupOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="f874b-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f874b-106">列名</span><span class="sxs-lookup"><span data-stu-id="f874b-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f874b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f874b-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f874b-108">說明</span><span class="sxs-lookup"><span data-stu-id="f874b-108">DESCRIPTION</span></span>
<span data-ttu-id="f874b-109">Get-AzSqlVMGroup Cmdlet 會取得一或多個 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="f874b-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="f874b-110">示例</span><span class="sxs-lookup"><span data-stu-id="f874b-110">EXAMPLES</span></span>

### <span data-ttu-id="f874b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f874b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="f874b-112">這個命令會取得目前訂閱中所有 Azure SQL 虛擬電腦群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f874b-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="f874b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f874b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="f874b-114">這個命令會取得目前訂閱中指派給資源群組 ResourceGroup01 的所有 Azure SQL 虛擬電腦群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f874b-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f874b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f874b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="f874b-116">這個命令會取得指派給資源群組 ResourceGroup01 之 SQL 虛擬電腦群組「測試群組」的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f874b-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f874b-117">參數</span><span class="sxs-lookup"><span data-stu-id="f874b-117">PARAMETERS</span></span>

### <span data-ttu-id="f874b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f874b-118">-DefaultProfile</span></span>
<span data-ttu-id="f874b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f874b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f874b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f874b-120">-Name</span></span>
<span data-ttu-id="f874b-121">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="f874b-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="f874b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f874b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f874b-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f874b-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f874b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f874b-124">-ResourceId</span></span>
<span data-ttu-id="f874b-125">[SQL virtual 電腦群組資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f874b-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="f874b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f874b-126">CommonParameters</span></span>
<span data-ttu-id="f874b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f874b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f874b-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f874b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f874b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f874b-129">INPUTS</span></span>

### <span data-ttu-id="f874b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f874b-130">System.String</span></span>

## <span data-ttu-id="f874b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f874b-131">OUTPUTS</span></span>

### <span data-ttu-id="f874b-132">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="f874b-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f874b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f874b-133">NOTES</span></span>

## <span data-ttu-id="f874b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f874b-134">RELATED LINKS</span></span>
