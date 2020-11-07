---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: bfc64aeb344e9913bf72ae7b51559bb613209994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792839"
---
# <span data-ttu-id="48dd8-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="48dd8-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="48dd8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="48dd8-103">更新 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="48dd8-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="48dd8-104">句法</span><span class="sxs-lookup"><span data-stu-id="48dd8-104">SYNTAX</span></span>

### <span data-ttu-id="48dd8-105">NameParamaterList (預設) </span><span class="sxs-lookup"><span data-stu-id="48dd8-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48dd8-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="48dd8-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48dd8-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="48dd8-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48dd8-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="48dd8-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48dd8-109">說明</span><span class="sxs-lookup"><span data-stu-id="48dd8-109">DESCRIPTION</span></span>
<span data-ttu-id="48dd8-110">Update-AzSqlVM Cmdlet 會更新 sql 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="48dd8-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="48dd8-111">示例</span><span class="sxs-lookup"><span data-stu-id="48dd8-111">EXAMPLES</span></span>

### <span data-ttu-id="48dd8-112">範例1</span><span class="sxs-lookup"><span data-stu-id="48dd8-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="48dd8-113">更新 sql 虛擬機器的標記。</span><span class="sxs-lookup"><span data-stu-id="48dd8-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="48dd8-114">參數</span><span class="sxs-lookup"><span data-stu-id="48dd8-114">PARAMETERS</span></span>

### <span data-ttu-id="48dd8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48dd8-115">-AsJob</span></span>
<span data-ttu-id="48dd8-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48dd8-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="48dd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48dd8-117">-DefaultProfile</span></span>
<span data-ttu-id="48dd8-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48dd8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48dd8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48dd8-119">-InputObject</span></span>
<span data-ttu-id="48dd8-120">SQL 虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="48dd8-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="48dd8-121">-LicenseType</span></span>
<span data-ttu-id="48dd8-122">SQL 虛擬機器授權類型。</span><span class="sxs-lookup"><span data-stu-id="48dd8-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="48dd8-123">-Name</span></span>
<span data-ttu-id="48dd8-124">[SQL 虛擬機器名稱]。</span><span class="sxs-lookup"><span data-stu-id="48dd8-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-125">-優惠</span><span class="sxs-lookup"><span data-stu-id="48dd8-125">-Offer</span></span>
<span data-ttu-id="48dd8-126">SQL 虛擬機器提供。</span><span class="sxs-lookup"><span data-stu-id="48dd8-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48dd8-127">-ResourceGroupName</span></span>
<span data-ttu-id="48dd8-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48dd8-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48dd8-129">-ResourceId</span></span>
<span data-ttu-id="48dd8-130">[SQL 虛擬機器資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="48dd8-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="48dd8-131">-Sku</span></span>
<span data-ttu-id="48dd8-132">SQL 虛擬機器 edition 類型。</span><span class="sxs-lookup"><span data-stu-id="48dd8-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="48dd8-133">-SqlManagementType</span></span>
<span data-ttu-id="48dd8-134">SQL 虛擬機器管理類型。</span><span class="sxs-lookup"><span data-stu-id="48dd8-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="48dd8-135">-Tag</span></span>
<span data-ttu-id="48dd8-136">要與 SQL 虛擬機器關聯的標記</span><span class="sxs-lookup"><span data-stu-id="48dd8-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48dd8-137">-確認</span><span class="sxs-lookup"><span data-stu-id="48dd8-137">-Confirm</span></span>
<span data-ttu-id="48dd8-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48dd8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48dd8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48dd8-139">-WhatIf</span></span>
<span data-ttu-id="48dd8-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48dd8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48dd8-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48dd8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48dd8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48dd8-142">CommonParameters</span></span>
<span data-ttu-id="48dd8-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48dd8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48dd8-144">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48dd8-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48dd8-145">輸入</span><span class="sxs-lookup"><span data-stu-id="48dd8-145">INPUTS</span></span>

### <span data-ttu-id="48dd8-146">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="48dd8-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="48dd8-147">輸出</span><span class="sxs-lookup"><span data-stu-id="48dd8-147">OUTPUTS</span></span>

### <span data-ttu-id="48dd8-148">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMModel （）</span><span class="sxs-lookup"><span data-stu-id="48dd8-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="48dd8-149">筆記</span><span class="sxs-lookup"><span data-stu-id="48dd8-149">NOTES</span></span>

## <span data-ttu-id="48dd8-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="48dd8-150">RELATED LINKS</span></span>
