---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 04a75ec50f985bb1cea0266c077946adbdab4f65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914261"
---
# <span data-ttu-id="26e37-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="26e37-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="26e37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26e37-102">SYNOPSIS</span></span>
<span data-ttu-id="26e37-103">更新 sql 虛擬機器群組。</span><span class="sxs-lookup"><span data-stu-id="26e37-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="26e37-104">語法</span><span class="sxs-lookup"><span data-stu-id="26e37-104">SYNTAX</span></span>

### <span data-ttu-id="26e37-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="26e37-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e37-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="26e37-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e37-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e37-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e37-108">描述</span><span class="sxs-lookup"><span data-stu-id="26e37-108">DESCRIPTION</span></span>
<span data-ttu-id="26e37-109">Cmdlet Update-AzSqlVMGroup更新 sql 虛擬機器群組。</span><span class="sxs-lookup"><span data-stu-id="26e37-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="26e37-110">例子</span><span class="sxs-lookup"><span data-stu-id="26e37-110">EXAMPLES</span></span>

### <span data-ttu-id="26e37-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="26e37-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="26e37-112">更新 sql 虛擬機器群組的標記。</span><span class="sxs-lookup"><span data-stu-id="26e37-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="26e37-113">參數</span><span class="sxs-lookup"><span data-stu-id="26e37-113">PARAMETERS</span></span>

### <span data-ttu-id="26e37-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26e37-114">-AsJob</span></span>
<span data-ttu-id="26e37-115">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e37-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="26e37-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="26e37-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="26e37-117">用於建立組組的名稱</span><span class="sxs-lookup"><span data-stu-id="26e37-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="26e37-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="26e37-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="26e37-119">用於作業組組的名稱</span><span class="sxs-lookup"><span data-stu-id="26e37-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="26e37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e37-120">-DefaultProfile</span></span>
<span data-ttu-id="26e37-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="26e37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e37-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="26e37-122">-DomainFqdn</span></span>
<span data-ttu-id="26e37-123">網域完整名稱</span><span class="sxs-lookup"><span data-stu-id="26e37-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="26e37-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="26e37-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="26e37-125">檔案共用見證的選擇性路徑</span><span class="sxs-lookup"><span data-stu-id="26e37-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="26e37-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e37-126">-InputObject</span></span>
<span data-ttu-id="26e37-127">SQL 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="26e37-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="26e37-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="26e37-128">-Name</span></span>
<span data-ttu-id="26e37-129">SQL 虛擬機器組名。</span><span class="sxs-lookup"><span data-stu-id="26e37-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="26e37-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="26e37-130">-OuPath</span></span>
<span data-ttu-id="26e37-131">節點和組會存在之組織單位路徑</span><span class="sxs-lookup"><span data-stu-id="26e37-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="26e37-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e37-132">-ResourceGroupName</span></span>
<span data-ttu-id="26e37-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26e37-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="26e37-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e37-134">-ResourceId</span></span>
<span data-ttu-id="26e37-135">SQL 虛擬機器群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="26e37-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="26e37-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="26e37-136">-SqlServiceAccount</span></span>
<span data-ttu-id="26e37-137">SQL 服務在組集中所有參與的 SQL 虛擬機器上執行的名稱</span><span class="sxs-lookup"><span data-stu-id="26e37-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="26e37-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="26e37-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="26e37-139">見證儲存帳戶的主鍵</span><span class="sxs-lookup"><span data-stu-id="26e37-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e37-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="26e37-140">-StorageAccountUrl</span></span>
<span data-ttu-id="26e37-141">見證儲存帳戶的主鍵</span><span class="sxs-lookup"><span data-stu-id="26e37-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="26e37-142">-標記</span><span class="sxs-lookup"><span data-stu-id="26e37-142">-Tag</span></span>
<span data-ttu-id="26e37-143">要與 SQL 虛擬機器群組關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="26e37-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="26e37-144">-確認</span><span class="sxs-lookup"><span data-stu-id="26e37-144">-Confirm</span></span>
<span data-ttu-id="26e37-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="26e37-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e37-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e37-146">-WhatIf</span></span>
<span data-ttu-id="26e37-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26e37-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e37-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e37-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e37-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e37-149">CommonParameters</span></span>
<span data-ttu-id="26e37-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26e37-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e37-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26e37-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e37-152">輸入</span><span class="sxs-lookup"><span data-stu-id="26e37-152">INPUTS</span></span>

### <span data-ttu-id="26e37-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="26e37-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="26e37-154">System.String</span><span class="sxs-lookup"><span data-stu-id="26e37-154">System.String</span></span>

## <span data-ttu-id="26e37-155">輸出</span><span class="sxs-lookup"><span data-stu-id="26e37-155">OUTPUTS</span></span>

### <span data-ttu-id="26e37-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlMODELGroupModel</span><span class="sxs-lookup"><span data-stu-id="26e37-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="26e37-157">筆記</span><span class="sxs-lookup"><span data-stu-id="26e37-157">NOTES</span></span>

## <span data-ttu-id="26e37-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="26e37-158">RELATED LINKS</span></span>
