---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798053"
---
# <span data-ttu-id="094db-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="094db-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="094db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="094db-102">SYNOPSIS</span></span>
<span data-ttu-id="094db-103">刪除 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="094db-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="094db-104">句法</span><span class="sxs-lookup"><span data-stu-id="094db-104">SYNTAX</span></span>

### <span data-ttu-id="094db-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="094db-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094db-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="094db-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="094db-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="094db-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="094db-108">說明</span><span class="sxs-lookup"><span data-stu-id="094db-108">DESCRIPTION</span></span>
<span data-ttu-id="094db-109">Remove-AzSqlVM Cmdlet 會刪除 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="094db-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="094db-110">示例</span><span class="sxs-lookup"><span data-stu-id="094db-110">EXAMPLES</span></span>

### <span data-ttu-id="094db-111">範例1</span><span class="sxs-lookup"><span data-stu-id="094db-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="094db-112">刪除 [資源群組 ResourceGroup01] 中的 Azure SQL 虛擬機器 "vm"。</span><span class="sxs-lookup"><span data-stu-id="094db-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="094db-113">參數</span><span class="sxs-lookup"><span data-stu-id="094db-113">PARAMETERS</span></span>

### <span data-ttu-id="094db-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="094db-114">-AsJob</span></span>
<span data-ttu-id="094db-115">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="094db-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="094db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094db-116">-DefaultProfile</span></span>
<span data-ttu-id="094db-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="094db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="094db-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="094db-118">-InputObject</span></span>
<span data-ttu-id="094db-119">SQL 虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="094db-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="094db-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="094db-120">-Name</span></span>
<span data-ttu-id="094db-121">[SQL 虛擬機器名稱]。</span><span class="sxs-lookup"><span data-stu-id="094db-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="094db-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="094db-122">-PassThru</span></span>
<span data-ttu-id="094db-123">指定是否要在 Cmdlet 執行結束時輸出已刪除的資源。</span><span class="sxs-lookup"><span data-stu-id="094db-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="094db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094db-124">-ResourceGroupName</span></span>
<span data-ttu-id="094db-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="094db-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="094db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="094db-126">-ResourceId</span></span>
<span data-ttu-id="094db-127">[SQL 虛擬機器資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="094db-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="094db-128">-確認</span><span class="sxs-lookup"><span data-stu-id="094db-128">-Confirm</span></span>
<span data-ttu-id="094db-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="094db-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="094db-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="094db-130">-WhatIf</span></span>
<span data-ttu-id="094db-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="094db-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="094db-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="094db-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="094db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094db-133">CommonParameters</span></span>
<span data-ttu-id="094db-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="094db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094db-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="094db-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094db-136">輸入</span><span class="sxs-lookup"><span data-stu-id="094db-136">INPUTS</span></span>

### <span data-ttu-id="094db-137">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="094db-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="094db-138">輸出</span><span class="sxs-lookup"><span data-stu-id="094db-138">OUTPUTS</span></span>

### <span data-ttu-id="094db-139">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="094db-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="094db-140">筆記</span><span class="sxs-lookup"><span data-stu-id="094db-140">NOTES</span></span>

## <span data-ttu-id="094db-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="094db-141">RELATED LINKS</span></span>
