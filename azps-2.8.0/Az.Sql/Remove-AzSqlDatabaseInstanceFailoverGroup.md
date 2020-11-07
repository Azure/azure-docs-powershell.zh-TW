---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792699"
---
# <span data-ttu-id="a419d-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a419d-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="a419d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a419d-102">SYNOPSIS</span></span>
<span data-ttu-id="a419d-103">移除實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a419d-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="a419d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a419d-104">SYNTAX</span></span>

### <span data-ttu-id="a419d-105">RemoveIFGDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="a419d-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a419d-106">從資源識別碼中移除實例容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="a419d-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a419d-107">從 AzureSqlInstanceFailoverGroupModel 實例定義中移除實例容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="a419d-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a419d-108">說明</span><span class="sxs-lookup"><span data-stu-id="a419d-108">DESCRIPTION</span></span>
<span data-ttu-id="a419d-109">這個命令會移除具有指定名稱的實例容錯移轉群組，並讓所有資料庫保持不變。</span><span class="sxs-lookup"><span data-stu-id="a419d-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="a419d-110">將會從 DNS 登出偵聽程式端點。</span><span class="sxs-lookup"><span data-stu-id="a419d-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="a419d-111">應使用實例容錯移轉群組的主要區域來執行命令。</span><span class="sxs-lookup"><span data-stu-id="a419d-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="a419d-112">示例</span><span class="sxs-lookup"><span data-stu-id="a419d-112">EXAMPLES</span></span>

### <span data-ttu-id="a419d-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a419d-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="a419d-114">移除實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a419d-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="a419d-115">參數</span><span class="sxs-lookup"><span data-stu-id="a419d-115">PARAMETERS</span></span>

### <span data-ttu-id="a419d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a419d-116">-DefaultProfile</span></span>
<span data-ttu-id="a419d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a419d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a419d-118">-Force</span></span>
<span data-ttu-id="a419d-119">跳過確認訊息以執行動作。</span><span class="sxs-lookup"><span data-stu-id="a419d-119">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a419d-120">-InputObject</span></span>
<span data-ttu-id="a419d-121">要移除的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="a419d-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-122">-位置</span><span class="sxs-lookup"><span data-stu-id="a419d-122">-Location</span></span>
<span data-ttu-id="a419d-123">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a419d-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a419d-124">-Name</span></span>
<span data-ttu-id="a419d-125">要移除之實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a419d-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a419d-126">-ResourceGroupName</span></span>
<span data-ttu-id="a419d-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a419d-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a419d-128">-ResourceId</span></span>
<span data-ttu-id="a419d-129">要移除之實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a419d-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a419d-130">-Confirm</span></span>
<span data-ttu-id="a419d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a419d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a419d-132">-WhatIf</span></span>
<span data-ttu-id="a419d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a419d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a419d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a419d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a419d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a419d-135">CommonParameters</span></span>
<span data-ttu-id="a419d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a419d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a419d-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a419d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a419d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a419d-138">INPUTS</span></span>

### <span data-ttu-id="a419d-139">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="a419d-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="a419d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a419d-140">System.String</span></span>

## <span data-ttu-id="a419d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a419d-141">OUTPUTS</span></span>

### <span data-ttu-id="a419d-142">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="a419d-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="a419d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a419d-143">NOTES</span></span>

## <span data-ttu-id="a419d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a419d-144">RELATED LINKS</span></span>
