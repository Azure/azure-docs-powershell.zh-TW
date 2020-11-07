---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798121"
---
# <span data-ttu-id="a0b92-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="a0b92-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="a0b92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0b92-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b92-103">為 sql 虛擬機器建立新的配置。</span><span class="sxs-lookup"><span data-stu-id="a0b92-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="a0b92-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0b92-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b92-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0b92-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b92-106">New-AzSqlVMConfig Cmdlet 會為 sql 虛擬機器建立新的 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="a0b92-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="a0b92-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0b92-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b92-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a0b92-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a0b92-109">建立可供您用來建立 Azure sql 虛擬機器之 sql 虛擬機器的本機可設定物件。</span><span class="sxs-lookup"><span data-stu-id="a0b92-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="a0b92-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0b92-110">PARAMETERS</span></span>

### <span data-ttu-id="a0b92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b92-111">-DefaultProfile</span></span>
<span data-ttu-id="a0b92-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0b92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0b92-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a0b92-113">-LicenseType</span></span>
<span data-ttu-id="a0b92-114">SQL 虛擬機器授權類型。</span><span class="sxs-lookup"><span data-stu-id="a0b92-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="a0b92-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="a0b92-115">-Offer</span></span>
<span data-ttu-id="a0b92-116">SQL 虛擬機器提供。</span><span class="sxs-lookup"><span data-stu-id="a0b92-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="a0b92-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="a0b92-117">-Sku</span></span>
<span data-ttu-id="a0b92-118">SQL 虛擬機器 edition 類型。</span><span class="sxs-lookup"><span data-stu-id="a0b92-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="a0b92-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="a0b92-119">-SqlManagementType</span></span>
<span data-ttu-id="a0b92-120">SQL 虛擬機器管理類型。</span><span class="sxs-lookup"><span data-stu-id="a0b92-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="a0b92-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0b92-121">-Tag</span></span>
<span data-ttu-id="a0b92-122">要與 SQL 虛擬機器關聯的標記</span><span class="sxs-lookup"><span data-stu-id="a0b92-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="a0b92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b92-123">CommonParameters</span></span>
<span data-ttu-id="a0b92-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0b92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b92-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0b92-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b92-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a0b92-126">INPUTS</span></span>

### <span data-ttu-id="a0b92-127">所有</span><span class="sxs-lookup"><span data-stu-id="a0b92-127">None</span></span>

## <span data-ttu-id="a0b92-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a0b92-128">OUTPUTS</span></span>

### <span data-ttu-id="a0b92-129">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="a0b92-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a0b92-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a0b92-130">NOTES</span></span>

## <span data-ttu-id="a0b92-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0b92-131">RELATED LINKS</span></span>
