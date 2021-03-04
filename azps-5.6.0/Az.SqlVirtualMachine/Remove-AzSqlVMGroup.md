---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: d9d5ee7159f5a7f237bd9194051c99801481f1d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908421"
---
# <span data-ttu-id="e7fb1-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="e7fb1-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="e7fb1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fb1-103">刪除 sql 虛擬機器群組。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="e7fb1-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7fb1-104">SYNTAX</span></span>

### <span data-ttu-id="e7fb1-105">ParamaterList (預設) </span><span class="sxs-lookup"><span data-stu-id="e7fb1-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7fb1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e7fb1-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fb1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7fb1-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fb1-108">名字</span><span class="sxs-lookup"><span data-stu-id="e7fb1-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7fb1-109">描述</span><span class="sxs-lookup"><span data-stu-id="e7fb1-109">DESCRIPTION</span></span>
<span data-ttu-id="e7fb1-110">Cmdlet Remove-AzSqlVMGroup刪除 sql 虛擬機器群組。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="e7fb1-111">例子</span><span class="sxs-lookup"><span data-stu-id="e7fb1-111">EXAMPLES</span></span>

### <span data-ttu-id="e7fb1-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="e7fb1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="e7fb1-113">刪除資源群組 ResourceGroup01 中的 Azure SQL 虛擬機器群組「測試群組」。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e7fb1-114">參數</span><span class="sxs-lookup"><span data-stu-id="e7fb1-114">PARAMETERS</span></span>

### <span data-ttu-id="e7fb1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7fb1-115">-AsJob</span></span>
<span data-ttu-id="e7fb1-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e7fb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fb1-117">-DefaultProfile</span></span>
<span data-ttu-id="e7fb1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7fb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7fb1-119">-InputObject</span></span>
<span data-ttu-id="e7fb1-120">SQL 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fb1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7fb1-121">-Name</span></span>
<span data-ttu-id="e7fb1-122">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="e7fb1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7fb1-123">-PassThru</span></span>
<span data-ttu-id="e7fb1-124">指定是否要在 Cmdlet 執行結束時輸出已刪除的資源。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="e7fb1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fb1-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7fb1-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7fb1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7fb1-127">-ResourceId</span></span>
<span data-ttu-id="e7fb1-128">SQL 虛擬機器群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="e7fb1-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e7fb1-129">-Confirm</span></span>
<span data-ttu-id="e7fb1-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7fb1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7fb1-131">-WhatIf</span></span>
<span data-ttu-id="e7fb1-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7fb1-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7fb1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fb1-134">CommonParameters</span></span>
<span data-ttu-id="e7fb1-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7fb1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fb1-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7fb1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fb1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e7fb1-137">INPUTS</span></span>

### <span data-ttu-id="e7fb1-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="e7fb1-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="e7fb1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e7fb1-139">System.String</span></span>

## <span data-ttu-id="e7fb1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e7fb1-140">OUTPUTS</span></span>

### <span data-ttu-id="e7fb1-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="e7fb1-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e7fb1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e7fb1-142">NOTES</span></span>

## <span data-ttu-id="e7fb1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7fb1-143">RELATED LINKS</span></span>
