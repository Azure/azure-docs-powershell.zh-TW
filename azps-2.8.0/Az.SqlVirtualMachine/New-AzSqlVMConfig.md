---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: a2ee91815553b1de6ae21eb2afb344e010058deb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792848"
---
# <span data-ttu-id="9b71c-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="9b71c-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="9b71c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b71c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b71c-103">為 sql 虛擬機器建立新的配置。</span><span class="sxs-lookup"><span data-stu-id="9b71c-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="9b71c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b71c-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b71c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b71c-105">DESCRIPTION</span></span>
<span data-ttu-id="9b71c-106">New-AzSqlVMConfig Cmdlet 會為 sql 虛擬機器建立新的 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="9b71c-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="9b71c-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b71c-107">EXAMPLES</span></span>

### <span data-ttu-id="9b71c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9b71c-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="9b71c-109">建立可供您用來建立 Azure sql 虛擬機器之 sql 虛擬機器的本機可設定物件。</span><span class="sxs-lookup"><span data-stu-id="9b71c-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="9b71c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b71c-110">PARAMETERS</span></span>

### <span data-ttu-id="9b71c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b71c-111">-DefaultProfile</span></span>
<span data-ttu-id="9b71c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b71c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b71c-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9b71c-113">-LicenseType</span></span>
<span data-ttu-id="9b71c-114">SQL 虛擬機器授權類型。</span><span class="sxs-lookup"><span data-stu-id="9b71c-114">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="9b71c-115">-優惠</span><span class="sxs-lookup"><span data-stu-id="9b71c-115">-Offer</span></span>
<span data-ttu-id="9b71c-116">SQL 虛擬機器提供。</span><span class="sxs-lookup"><span data-stu-id="9b71c-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="9b71c-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="9b71c-117">-Sku</span></span>
<span data-ttu-id="9b71c-118">SQL 虛擬機器 edition 類型。</span><span class="sxs-lookup"><span data-stu-id="9b71c-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="9b71c-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="9b71c-119">-SqlManagementType</span></span>
<span data-ttu-id="9b71c-120">SQL 虛擬機器管理類型。</span><span class="sxs-lookup"><span data-stu-id="9b71c-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="9b71c-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b71c-121">-Tag</span></span>
<span data-ttu-id="9b71c-122">要與 SQL 虛擬機器關聯的標記</span><span class="sxs-lookup"><span data-stu-id="9b71c-122">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="9b71c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b71c-123">CommonParameters</span></span>
<span data-ttu-id="9b71c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b71c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b71c-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b71c-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b71c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9b71c-126">INPUTS</span></span>

### <span data-ttu-id="9b71c-127">所有</span><span class="sxs-lookup"><span data-stu-id="9b71c-127">None</span></span>

## <span data-ttu-id="9b71c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9b71c-128">OUTPUTS</span></span>

### <span data-ttu-id="9b71c-129">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="9b71c-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="9b71c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9b71c-130">NOTES</span></span>

## <span data-ttu-id="9b71c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b71c-131">RELATED LINKS</span></span>
