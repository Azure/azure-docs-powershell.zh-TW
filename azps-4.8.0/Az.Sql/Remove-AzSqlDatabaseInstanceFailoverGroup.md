---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127275"
---
# <span data-ttu-id="ed758-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ed758-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ed758-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed758-102">SYNOPSIS</span></span>
<span data-ttu-id="ed758-103">移除實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="ed758-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="ed758-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed758-104">SYNTAX</span></span>

### <span data-ttu-id="ed758-105">RemoveIFGDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ed758-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed758-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed758-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed758-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="ed758-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed758-108">說明</span><span class="sxs-lookup"><span data-stu-id="ed758-108">DESCRIPTION</span></span>
<span data-ttu-id="ed758-109">這個命令會移除具有指定名稱的實例容錯移轉群組，並讓所有資料庫保持不變。</span><span class="sxs-lookup"><span data-stu-id="ed758-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="ed758-110">將會從 DNS 登出偵聽程式端點。</span><span class="sxs-lookup"><span data-stu-id="ed758-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="ed758-111">應使用實例容錯移轉群組的主要區域來執行命令。</span><span class="sxs-lookup"><span data-stu-id="ed758-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="ed758-112">示例</span><span class="sxs-lookup"><span data-stu-id="ed758-112">EXAMPLES</span></span>

### <span data-ttu-id="ed758-113">範例1</span><span class="sxs-lookup"><span data-stu-id="ed758-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="ed758-114">移除實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="ed758-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="ed758-115">參數</span><span class="sxs-lookup"><span data-stu-id="ed758-115">PARAMETERS</span></span>

### <span data-ttu-id="ed758-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed758-116">-DefaultProfile</span></span>
<span data-ttu-id="ed758-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed758-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed758-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ed758-118">-Force</span></span>
<span data-ttu-id="ed758-119">跳過確認訊息以執行動作。</span><span class="sxs-lookup"><span data-stu-id="ed758-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="ed758-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed758-120">-InputObject</span></span>
<span data-ttu-id="ed758-121">要移除的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="ed758-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="ed758-122">-位置</span><span class="sxs-lookup"><span data-stu-id="ed758-122">-Location</span></span>
<span data-ttu-id="ed758-123">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="ed758-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ed758-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed758-124">-Name</span></span>
<span data-ttu-id="ed758-125">要移除之實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed758-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="ed758-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed758-126">-PassThru</span></span>
<span data-ttu-id="ed758-127">指定是否要透過 Cmdlet 執行輸出進行傳遞。</span><span class="sxs-lookup"><span data-stu-id="ed758-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="ed758-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed758-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed758-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed758-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed758-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed758-130">-ResourceId</span></span>
<span data-ttu-id="ed758-131">要移除之實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed758-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="ed758-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ed758-132">-Confirm</span></span>
<span data-ttu-id="ed758-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed758-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed758-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed758-134">-WhatIf</span></span>
<span data-ttu-id="ed758-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed758-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed758-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed758-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed758-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed758-137">CommonParameters</span></span>
<span data-ttu-id="ed758-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed758-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed758-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ed758-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed758-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ed758-140">INPUTS</span></span>

### <span data-ttu-id="ed758-141">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="ed758-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="ed758-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ed758-142">System.String</span></span>

## <span data-ttu-id="ed758-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ed758-143">OUTPUTS</span></span>

### <span data-ttu-id="ed758-144">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="ed758-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ed758-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ed758-145">NOTES</span></span>

## <span data-ttu-id="ed758-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed758-146">RELATED LINKS</span></span>
