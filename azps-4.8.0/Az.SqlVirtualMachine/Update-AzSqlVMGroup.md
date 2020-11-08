---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129782"
---
# <span data-ttu-id="37bae-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="37bae-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="37bae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37bae-102">SYNOPSIS</span></span>
<span data-ttu-id="37bae-103">更新 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="37bae-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="37bae-104">句法</span><span class="sxs-lookup"><span data-stu-id="37bae-104">SYNTAX</span></span>

### <span data-ttu-id="37bae-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="37bae-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37bae-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="37bae-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37bae-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="37bae-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37bae-108">說明</span><span class="sxs-lookup"><span data-stu-id="37bae-108">DESCRIPTION</span></span>
<span data-ttu-id="37bae-109">Update-AzSqlVMGroup Cmdlet 會更新 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="37bae-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="37bae-110">示例</span><span class="sxs-lookup"><span data-stu-id="37bae-110">EXAMPLES</span></span>

### <span data-ttu-id="37bae-111">範例1</span><span class="sxs-lookup"><span data-stu-id="37bae-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="37bae-112">更新 sql 虛擬電腦群組的標記。</span><span class="sxs-lookup"><span data-stu-id="37bae-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="37bae-113">參數</span><span class="sxs-lookup"><span data-stu-id="37bae-113">PARAMETERS</span></span>

### <span data-ttu-id="37bae-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37bae-114">-AsJob</span></span>
<span data-ttu-id="37bae-115">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37bae-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="37bae-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="37bae-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="37bae-117">用於建立群集的名稱</span><span class="sxs-lookup"><span data-stu-id="37bae-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="37bae-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="37bae-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="37bae-119">用於運營群集的名稱</span><span class="sxs-lookup"><span data-stu-id="37bae-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="37bae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37bae-120">-DefaultProfile</span></span>
<span data-ttu-id="37bae-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37bae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37bae-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="37bae-122">-DomainFqdn</span></span>
<span data-ttu-id="37bae-123">網域的完整名稱</span><span class="sxs-lookup"><span data-stu-id="37bae-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="37bae-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="37bae-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="37bae-125">可供共用見證的選用路徑</span><span class="sxs-lookup"><span data-stu-id="37bae-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="37bae-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37bae-126">-InputObject</span></span>
<span data-ttu-id="37bae-127">SQL 虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="37bae-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="37bae-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="37bae-128">-Name</span></span>
<span data-ttu-id="37bae-129">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="37bae-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="37bae-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="37bae-130">-OuPath</span></span>
<span data-ttu-id="37bae-131">節點與群集將出現的組織單位路徑</span><span class="sxs-lookup"><span data-stu-id="37bae-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="37bae-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37bae-132">-ResourceGroupName</span></span>
<span data-ttu-id="37bae-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37bae-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="37bae-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37bae-134">-ResourceId</span></span>
<span data-ttu-id="37bae-135">[SQL virtual 電腦群組資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="37bae-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="37bae-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="37bae-136">-SqlServiceAccount</span></span>
<span data-ttu-id="37bae-137">SQL 服務將在群集中所有參與的 SQL 虛擬機器上執行的名稱</span><span class="sxs-lookup"><span data-stu-id="37bae-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="37bae-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="37bae-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="37bae-139">見證儲存空間帳戶的主鍵</span><span class="sxs-lookup"><span data-stu-id="37bae-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="37bae-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="37bae-140">-StorageAccountUrl</span></span>
<span data-ttu-id="37bae-141">見證儲存空間帳戶的主鍵</span><span class="sxs-lookup"><span data-stu-id="37bae-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="37bae-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="37bae-142">-Tag</span></span>
<span data-ttu-id="37bae-143">要與 SQL 虛擬電腦群組相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="37bae-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="37bae-144">-確認</span><span class="sxs-lookup"><span data-stu-id="37bae-144">-Confirm</span></span>
<span data-ttu-id="37bae-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37bae-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37bae-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37bae-146">-WhatIf</span></span>
<span data-ttu-id="37bae-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37bae-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37bae-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37bae-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37bae-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bae-149">CommonParameters</span></span>
<span data-ttu-id="37bae-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37bae-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bae-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37bae-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bae-152">輸入</span><span class="sxs-lookup"><span data-stu-id="37bae-152">INPUTS</span></span>

### <span data-ttu-id="37bae-153">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="37bae-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="37bae-154">System.object</span><span class="sxs-lookup"><span data-stu-id="37bae-154">System.String</span></span>

## <span data-ttu-id="37bae-155">輸出</span><span class="sxs-lookup"><span data-stu-id="37bae-155">OUTPUTS</span></span>

### <span data-ttu-id="37bae-156">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="37bae-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="37bae-157">筆記</span><span class="sxs-lookup"><span data-stu-id="37bae-157">NOTES</span></span>

## <span data-ttu-id="37bae-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="37bae-158">RELATED LINKS</span></span>
