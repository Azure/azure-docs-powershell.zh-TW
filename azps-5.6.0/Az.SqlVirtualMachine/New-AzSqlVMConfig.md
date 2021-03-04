---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: e12f69cbb36c5fabccffc4102723175c9f6b8909
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912242"
---
# <span data-ttu-id="65d8b-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="65d8b-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="65d8b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="65d8b-103">為 sql 虛擬機器建立新組配置。</span><span class="sxs-lookup"><span data-stu-id="65d8b-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="65d8b-104">語法</span><span class="sxs-lookup"><span data-stu-id="65d8b-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d8b-105">描述</span><span class="sxs-lookup"><span data-stu-id="65d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="65d8b-106">Cmdlet New-AzSqlVMConfig建立 Sql 虛擬機器的新組組物件。</span><span class="sxs-lookup"><span data-stu-id="65d8b-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="65d8b-107">例子</span><span class="sxs-lookup"><span data-stu-id="65d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="65d8b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="65d8b-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="65d8b-109">建立本機可配置的 sql 虛擬機器物件，可用來建立 Azure sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="65d8b-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="65d8b-110">參數</span><span class="sxs-lookup"><span data-stu-id="65d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="65d8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d8b-111">-DefaultProfile</span></span>
<span data-ttu-id="65d8b-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="65d8b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d8b-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="65d8b-113">-LicenseType</span></span>
<span data-ttu-id="65d8b-114">SQL 虛擬機器授權類型。</span><span class="sxs-lookup"><span data-stu-id="65d8b-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d8b-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="65d8b-115">-Offer</span></span>
<span data-ttu-id="65d8b-116">SQL 虛擬機器優惠。</span><span class="sxs-lookup"><span data-stu-id="65d8b-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="65d8b-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="65d8b-117">-Sku</span></span>
<span data-ttu-id="65d8b-118">SQL 虛擬機器版本類型。</span><span class="sxs-lookup"><span data-stu-id="65d8b-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="65d8b-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="65d8b-119">-SqlManagementType</span></span>
<span data-ttu-id="65d8b-120">SQL 虛擬機器管理類型。</span><span class="sxs-lookup"><span data-stu-id="65d8b-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="65d8b-121">-標記</span><span class="sxs-lookup"><span data-stu-id="65d8b-121">-Tag</span></span>
<span data-ttu-id="65d8b-122">要與 SQL 虛擬機器關聯的標記</span><span class="sxs-lookup"><span data-stu-id="65d8b-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d8b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d8b-123">CommonParameters</span></span>
<span data-ttu-id="65d8b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65d8b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d8b-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65d8b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d8b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="65d8b-126">INPUTS</span></span>

### <span data-ttu-id="65d8b-127">沒有</span><span class="sxs-lookup"><span data-stu-id="65d8b-127">None</span></span>

## <span data-ttu-id="65d8b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="65d8b-128">OUTPUTS</span></span>

### <span data-ttu-id="65d8b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELModel</span><span class="sxs-lookup"><span data-stu-id="65d8b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="65d8b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="65d8b-130">NOTES</span></span>

## <span data-ttu-id="65d8b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="65d8b-131">RELATED LINKS</span></span>
