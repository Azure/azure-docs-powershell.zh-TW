---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 741db1ddd4d2cce236d5a1d6787ea25179aa373f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908422"
---
# <span data-ttu-id="ddeff-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="ddeff-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="ddeff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddeff-102">SYNOPSIS</span></span>
<span data-ttu-id="ddeff-103">刪除 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ddeff-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="ddeff-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddeff-104">SYNTAX</span></span>

### <span data-ttu-id="ddeff-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="ddeff-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddeff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ddeff-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddeff-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddeff-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddeff-108">描述</span><span class="sxs-lookup"><span data-stu-id="ddeff-108">DESCRIPTION</span></span>
<span data-ttu-id="ddeff-109">Cmdlet Remove-AzSqlVM刪除 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ddeff-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="ddeff-110">例子</span><span class="sxs-lookup"><span data-stu-id="ddeff-110">EXAMPLES</span></span>

### <span data-ttu-id="ddeff-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ddeff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="ddeff-112">刪除資源群組 ResourceGroup01 中的 Azure SQL 虛擬機器 "vm"。</span><span class="sxs-lookup"><span data-stu-id="ddeff-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ddeff-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddeff-113">PARAMETERS</span></span>

### <span data-ttu-id="ddeff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddeff-114">-AsJob</span></span>
<span data-ttu-id="ddeff-115">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddeff-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ddeff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddeff-116">-DefaultProfile</span></span>
<span data-ttu-id="ddeff-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddeff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddeff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddeff-118">-InputObject</span></span>
<span data-ttu-id="ddeff-119">SQL 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="ddeff-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddeff-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddeff-120">-Name</span></span>
<span data-ttu-id="ddeff-121">SQL 虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="ddeff-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="ddeff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddeff-122">-PassThru</span></span>
<span data-ttu-id="ddeff-123">指定是否要在 Cmdlet 執行結束時輸出已刪除的資源。</span><span class="sxs-lookup"><span data-stu-id="ddeff-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="ddeff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddeff-124">-ResourceGroupName</span></span>
<span data-ttu-id="ddeff-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddeff-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddeff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddeff-126">-ResourceId</span></span>
<span data-ttu-id="ddeff-127">SQL 虛擬機器資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddeff-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="ddeff-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ddeff-128">-Confirm</span></span>
<span data-ttu-id="ddeff-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddeff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddeff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddeff-130">-WhatIf</span></span>
<span data-ttu-id="ddeff-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddeff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddeff-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddeff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddeff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddeff-133">CommonParameters</span></span>
<span data-ttu-id="ddeff-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddeff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddeff-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddeff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddeff-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ddeff-136">INPUTS</span></span>

### <span data-ttu-id="ddeff-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELModel</span><span class="sxs-lookup"><span data-stu-id="ddeff-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ddeff-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ddeff-138">OUTPUTS</span></span>

### <span data-ttu-id="ddeff-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELModel</span><span class="sxs-lookup"><span data-stu-id="ddeff-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="ddeff-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ddeff-140">NOTES</span></span>

## <span data-ttu-id="ddeff-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddeff-141">RELATED LINKS</span></span>
