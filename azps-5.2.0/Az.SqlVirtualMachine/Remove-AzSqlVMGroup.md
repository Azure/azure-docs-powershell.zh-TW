---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276696"
---
# <span data-ttu-id="351f3-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="351f3-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="351f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="351f3-102">SYNOPSIS</span></span>
<span data-ttu-id="351f3-103">刪除 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="351f3-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="351f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="351f3-104">SYNTAX</span></span>

### <span data-ttu-id="351f3-105">ParamaterList (預設) </span><span class="sxs-lookup"><span data-stu-id="351f3-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="351f3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="351f3-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351f3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="351f3-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="351f3-108">列名</span><span class="sxs-lookup"><span data-stu-id="351f3-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="351f3-109">說明</span><span class="sxs-lookup"><span data-stu-id="351f3-109">DESCRIPTION</span></span>
<span data-ttu-id="351f3-110">Remove-AzSqlVMGroup Cmdlet 會刪除 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="351f3-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="351f3-111">示例</span><span class="sxs-lookup"><span data-stu-id="351f3-111">EXAMPLES</span></span>

### <span data-ttu-id="351f3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="351f3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="351f3-113">刪除 [資源群組] ResourceGroup01 中的 Azure SQL 虛擬電腦群組「測試群組」。</span><span class="sxs-lookup"><span data-stu-id="351f3-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="351f3-114">參數</span><span class="sxs-lookup"><span data-stu-id="351f3-114">PARAMETERS</span></span>

### <span data-ttu-id="351f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="351f3-115">-AsJob</span></span>
<span data-ttu-id="351f3-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="351f3-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="351f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351f3-117">-DefaultProfile</span></span>
<span data-ttu-id="351f3-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="351f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="351f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="351f3-119">-InputObject</span></span>
<span data-ttu-id="351f3-120">SQL 虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="351f3-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="351f3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="351f3-121">-Name</span></span>
<span data-ttu-id="351f3-122">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="351f3-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="351f3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="351f3-123">-PassThru</span></span>
<span data-ttu-id="351f3-124">指定是否要在 Cmdlet 執行結束時輸出已刪除的資源。</span><span class="sxs-lookup"><span data-stu-id="351f3-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="351f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="351f3-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="351f3-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="351f3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="351f3-127">-ResourceId</span></span>
<span data-ttu-id="351f3-128">[SQL virtual 電腦群組資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="351f3-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="351f3-129">-確認</span><span class="sxs-lookup"><span data-stu-id="351f3-129">-Confirm</span></span>
<span data-ttu-id="351f3-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="351f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="351f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="351f3-131">-WhatIf</span></span>
<span data-ttu-id="351f3-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="351f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="351f3-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="351f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="351f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351f3-134">CommonParameters</span></span>
<span data-ttu-id="351f3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="351f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351f3-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="351f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351f3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="351f3-137">INPUTS</span></span>

### <span data-ttu-id="351f3-138">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="351f3-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="351f3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="351f3-139">System.String</span></span>

## <span data-ttu-id="351f3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="351f3-140">OUTPUTS</span></span>

### <span data-ttu-id="351f3-141">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="351f3-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="351f3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="351f3-142">NOTES</span></span>

## <span data-ttu-id="351f3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="351f3-143">RELATED LINKS</span></span>
