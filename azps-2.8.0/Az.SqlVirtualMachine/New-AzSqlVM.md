---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 5129960e8a4dce02a9d67b6881c53502972db19b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792849"
---
# <span data-ttu-id="b2150-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="b2150-101">New-AzSqlVM</span></span>

## <span data-ttu-id="b2150-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2150-102">SYNOPSIS</span></span>
<span data-ttu-id="b2150-103">建立新的 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b2150-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="b2150-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2150-104">SYNTAX</span></span>

### <span data-ttu-id="b2150-105">NameParamaterList (預設) </span><span class="sxs-lookup"><span data-stu-id="b2150-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> [-Location <String>]
 [-AsJob] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2150-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="b2150-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> [-Location <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2150-107">說明</span><span class="sxs-lookup"><span data-stu-id="b2150-107">DESCRIPTION</span></span>
<span data-ttu-id="b2150-108">New-AzSqlVM Cmdlet 會建立 Azure SQL 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b2150-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="b2150-109">示例</span><span class="sxs-lookup"><span data-stu-id="b2150-109">EXAMPLES</span></span>

### <span data-ttu-id="b2150-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b2150-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="b2150-111">在 [資源] 群組 ResourceGroup01 中建立新的 Azure SQL 虛擬機器與 name vm</span><span class="sxs-lookup"><span data-stu-id="b2150-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="b2150-112">參數</span><span class="sxs-lookup"><span data-stu-id="b2150-112">PARAMETERS</span></span>

### <span data-ttu-id="b2150-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2150-113">-AsJob</span></span>
<span data-ttu-id="b2150-114">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2150-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b2150-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2150-115">-DefaultProfile</span></span>
<span data-ttu-id="b2150-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2150-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2150-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b2150-117">-LicenseType</span></span>
<span data-ttu-id="b2150-118">SQL 虛擬機器授權類型。</span><span class="sxs-lookup"><span data-stu-id="b2150-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-119">-位置</span><span class="sxs-lookup"><span data-stu-id="b2150-119">-Location</span></span>
<span data-ttu-id="b2150-120">[SQL 虛擬機器位置]。</span><span class="sxs-lookup"><span data-stu-id="b2150-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="b2150-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2150-121">-Name</span></span>
<span data-ttu-id="b2150-122">[SQL 虛擬機器名稱]。</span><span class="sxs-lookup"><span data-stu-id="b2150-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-123">-優惠</span><span class="sxs-lookup"><span data-stu-id="b2150-123">-Offer</span></span>
<span data-ttu-id="b2150-124">SQL 虛擬機器提供。</span><span class="sxs-lookup"><span data-stu-id="b2150-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2150-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2150-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2150-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2150-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="b2150-127">-Sku</span></span>
<span data-ttu-id="b2150-128">SQL 虛擬機器 edition 類型。</span><span class="sxs-lookup"><span data-stu-id="b2150-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="b2150-129">-SqlManagementType</span></span>
<span data-ttu-id="b2150-130">SQL 虛擬機器管理類型。</span><span class="sxs-lookup"><span data-stu-id="b2150-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="b2150-131">-SqlVM</span></span>
<span data-ttu-id="b2150-132">SQL 虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="b2150-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2150-133">-Tag</span></span>
<span data-ttu-id="b2150-134">要與 SQL 虛擬機器關聯的標記</span><span class="sxs-lookup"><span data-stu-id="b2150-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2150-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b2150-135">-Confirm</span></span>
<span data-ttu-id="b2150-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2150-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2150-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2150-137">-WhatIf</span></span>
<span data-ttu-id="b2150-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2150-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2150-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2150-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2150-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2150-140">CommonParameters</span></span>
<span data-ttu-id="b2150-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2150-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2150-142">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b2150-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2150-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b2150-143">INPUTS</span></span>

### <span data-ttu-id="b2150-144">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="b2150-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b2150-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b2150-145">OUTPUTS</span></span>

### <span data-ttu-id="b2150-146">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="b2150-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b2150-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b2150-147">NOTES</span></span>

## <span data-ttu-id="b2150-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2150-148">RELATED LINKS</span></span>
