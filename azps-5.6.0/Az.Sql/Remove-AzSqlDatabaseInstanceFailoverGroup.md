---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 0e3bfc112ee8c80d08b0b5a87eb574a4c5bdb29e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903406"
---
# <span data-ttu-id="2407c-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2407c-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="2407c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2407c-102">SYNOPSIS</span></span>
<span data-ttu-id="2407c-103">移除實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="2407c-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="2407c-104">語法</span><span class="sxs-lookup"><span data-stu-id="2407c-104">SYNTAX</span></span>

### <span data-ttu-id="2407c-105">RemoveIFGDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2407c-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2407c-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="2407c-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2407c-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="2407c-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2407c-108">描述</span><span class="sxs-lookup"><span data-stu-id="2407c-108">DESCRIPTION</span></span>
<span data-ttu-id="2407c-109">此命令會移除具有指定名稱的實例容錯移轉群組，讓所有資料庫保持不變。</span><span class="sxs-lookup"><span data-stu-id="2407c-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="2407c-110">會從 DNS 取消註冊聆聽者端點。</span><span class="sxs-lookup"><span data-stu-id="2407c-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="2407c-111">實例容錯移轉群組的主要區域應該用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="2407c-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="2407c-112">例子</span><span class="sxs-lookup"><span data-stu-id="2407c-112">EXAMPLES</span></span>

### <span data-ttu-id="2407c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2407c-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="2407c-114">移除實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="2407c-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="2407c-115">參數</span><span class="sxs-lookup"><span data-stu-id="2407c-115">PARAMETERS</span></span>

### <span data-ttu-id="2407c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2407c-116">-DefaultProfile</span></span>
<span data-ttu-id="2407c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2407c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2407c-118">-強制</span><span class="sxs-lookup"><span data-stu-id="2407c-118">-Force</span></span>
<span data-ttu-id="2407c-119">跳過執行動作的確認訊息。</span><span class="sxs-lookup"><span data-stu-id="2407c-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="2407c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2407c-120">-InputObject</span></span>
<span data-ttu-id="2407c-121">要移除的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="2407c-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2407c-122">-位置</span><span class="sxs-lookup"><span data-stu-id="2407c-122">-Location</span></span>
<span data-ttu-id="2407c-123">要從其中取回實例容錯移轉群組的當地地區名稱。</span><span class="sxs-lookup"><span data-stu-id="2407c-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2407c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2407c-124">-Name</span></span>
<span data-ttu-id="2407c-125">要移除的實例容錯移轉組名。</span><span class="sxs-lookup"><span data-stu-id="2407c-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2407c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2407c-126">-PassThru</span></span>
<span data-ttu-id="2407c-127">指定是否要傳遞 Cmdlet 執行輸出。</span><span class="sxs-lookup"><span data-stu-id="2407c-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="2407c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2407c-128">-ResourceGroupName</span></span>
<span data-ttu-id="2407c-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2407c-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2407c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2407c-130">-ResourceId</span></span>
<span data-ttu-id="2407c-131">要移除的實例容錯移轉群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2407c-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2407c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="2407c-132">-Confirm</span></span>
<span data-ttu-id="2407c-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2407c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2407c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2407c-134">-WhatIf</span></span>
<span data-ttu-id="2407c-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2407c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2407c-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2407c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2407c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2407c-137">CommonParameters</span></span>
<span data-ttu-id="2407c-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2407c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2407c-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2407c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2407c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="2407c-140">INPUTS</span></span>

### <span data-ttu-id="2407c-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="2407c-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="2407c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2407c-142">System.String</span></span>

## <span data-ttu-id="2407c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2407c-143">OUTPUTS</span></span>

### <span data-ttu-id="2407c-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="2407c-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="2407c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2407c-145">NOTES</span></span>

## <span data-ttu-id="2407c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2407c-146">RELATED LINKS</span></span>
