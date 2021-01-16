---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282779"
---
# <span data-ttu-id="38192-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="38192-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="38192-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38192-102">SYNOPSIS</span></span>
<span data-ttu-id="38192-103">取得一或多個 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="38192-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="38192-104">句法</span><span class="sxs-lookup"><span data-stu-id="38192-104">SYNTAX</span></span>

### <span data-ttu-id="38192-105">ResourceGroupOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="38192-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38192-106">列名</span><span class="sxs-lookup"><span data-stu-id="38192-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38192-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38192-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38192-108">說明</span><span class="sxs-lookup"><span data-stu-id="38192-108">DESCRIPTION</span></span>
<span data-ttu-id="38192-109">Get-AzSqlVM Cmdlet 會取得一或多個 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="38192-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="38192-110">示例</span><span class="sxs-lookup"><span data-stu-id="38192-110">EXAMPLES</span></span>

### <span data-ttu-id="38192-111">範例1</span><span class="sxs-lookup"><span data-stu-id="38192-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="38192-112">此命令會取得目前訂閱中所有 Azure SQL 虛擬機器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="38192-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="38192-113">範例2</span><span class="sxs-lookup"><span data-stu-id="38192-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="38192-114">這個命令會取得目前訂閱中指派給資源群組 ResourceGroup01 的所有 Azure SQL 虛擬機器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="38192-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="38192-115">範例3</span><span class="sxs-lookup"><span data-stu-id="38192-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="38192-116">這個命令會取得指派給資源群組 ResourceGroup01 之 SQL 虛擬機器「vm」的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="38192-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="38192-117">參數</span><span class="sxs-lookup"><span data-stu-id="38192-117">PARAMETERS</span></span>

### <span data-ttu-id="38192-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38192-118">-DefaultProfile</span></span>
<span data-ttu-id="38192-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38192-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38192-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="38192-120">-Name</span></span>
<span data-ttu-id="38192-121">[SQL 虛擬機器名稱]。</span><span class="sxs-lookup"><span data-stu-id="38192-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="38192-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38192-122">-ResourceGroupName</span></span>
<span data-ttu-id="38192-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38192-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="38192-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38192-124">-ResourceId</span></span>
<span data-ttu-id="38192-125">[SQL 虛擬機器資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="38192-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="38192-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38192-126">CommonParameters</span></span>
<span data-ttu-id="38192-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38192-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38192-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38192-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38192-129">輸入</span><span class="sxs-lookup"><span data-stu-id="38192-129">INPUTS</span></span>

### <span data-ttu-id="38192-130">所有</span><span class="sxs-lookup"><span data-stu-id="38192-130">None</span></span>

## <span data-ttu-id="38192-131">輸出</span><span class="sxs-lookup"><span data-stu-id="38192-131">OUTPUTS</span></span>

### <span data-ttu-id="38192-132">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="38192-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="38192-133">筆記</span><span class="sxs-lookup"><span data-stu-id="38192-133">NOTES</span></span>

## <span data-ttu-id="38192-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="38192-134">RELATED LINKS</span></span>
