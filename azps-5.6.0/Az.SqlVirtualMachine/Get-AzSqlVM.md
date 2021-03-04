---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b3678b52f55e09fdcad8c1d116cd349b2cc5ab45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912258"
---
# <span data-ttu-id="cf1fe-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="cf1fe-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="cf1fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1fe-103">使用一或多個 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="cf1fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf1fe-104">SYNTAX</span></span>

### <span data-ttu-id="cf1fe-105">ResourceGroupOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="cf1fe-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf1fe-106">名字</span><span class="sxs-lookup"><span data-stu-id="cf1fe-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf1fe-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1fe-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf1fe-108">描述</span><span class="sxs-lookup"><span data-stu-id="cf1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="cf1fe-109">Cmdlet Get-AzSqlVM一或多個 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="cf1fe-110">例子</span><span class="sxs-lookup"><span data-stu-id="cf1fe-110">EXAMPLES</span></span>

### <span data-ttu-id="cf1fe-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="cf1fe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cf1fe-112">此命令會獲得目前訂閱中所有 Azure SQL 虛擬機器的資訊。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="cf1fe-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="cf1fe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cf1fe-114">此命令會獲得目前訂閱中指派給資源群組 ResourceGroup01 的所有 Azure SQL 虛擬機器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="cf1fe-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="cf1fe-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cf1fe-116">此命令會獲得指派給資源群組 ResourceGroup01 的 SQL 虛擬機器 "vm" 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="cf1fe-117">參數</span><span class="sxs-lookup"><span data-stu-id="cf1fe-117">PARAMETERS</span></span>

### <span data-ttu-id="cf1fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1fe-118">-DefaultProfile</span></span>
<span data-ttu-id="cf1fe-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf1fe-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf1fe-120">-Name</span></span>
<span data-ttu-id="cf1fe-121">SQL 虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf1fe-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf1fe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf1fe-124">-ResourceId</span></span>
<span data-ttu-id="cf1fe-125">SQL 虛擬機器資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1fe-126">CommonParameters</span></span>
<span data-ttu-id="cf1fe-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf1fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1fe-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf1fe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1fe-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cf1fe-129">INPUTS</span></span>

### <span data-ttu-id="cf1fe-130">沒有</span><span class="sxs-lookup"><span data-stu-id="cf1fe-130">None</span></span>

## <span data-ttu-id="cf1fe-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cf1fe-131">OUTPUTS</span></span>

### <span data-ttu-id="cf1fe-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELModel</span><span class="sxs-lookup"><span data-stu-id="cf1fe-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="cf1fe-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cf1fe-133">NOTES</span></span>

## <span data-ttu-id="cf1fe-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf1fe-134">RELATED LINKS</span></span>
