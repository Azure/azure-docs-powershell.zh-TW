---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 0a7874079b7de782fa7471e9087f04fdc3a9e754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905774"
---
# <span data-ttu-id="0a73a-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="0a73a-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="0a73a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a73a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a73a-103">移除 Azure SQL 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a73a-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0a73a-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a73a-104">SYNTAX</span></span>

### <span data-ttu-id="0a73a-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0a73a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a73a-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a73a-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a73a-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a73a-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a73a-108">描述</span><span class="sxs-lookup"><span data-stu-id="0a73a-108">DESCRIPTION</span></span>
<span data-ttu-id="0a73a-109">**Remove-AzSqlInstancePool** Cmdlet 會移除 Azure SQL 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a73a-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0a73a-110">例子</span><span class="sxs-lookup"><span data-stu-id="0a73a-110">EXAMPLES</span></span>

### <span data-ttu-id="0a73a-111">範例 1：移除實例資料庫</span><span class="sxs-lookup"><span data-stu-id="0a73a-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="0a73a-112">範例 2：根據實例資料庫的資源識別碼移除實例資料庫</span><span class="sxs-lookup"><span data-stu-id="0a73a-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="0a73a-113">範例 3：根據實例資料庫物件移除實例資料庫</span><span class="sxs-lookup"><span data-stu-id="0a73a-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="0a73a-114">此命令會移除名為 instancePool0 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="0a73a-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="0a73a-115">參數</span><span class="sxs-lookup"><span data-stu-id="0a73a-115">PARAMETERS</span></span>

### <span data-ttu-id="0a73a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a73a-116">-DefaultProfile</span></span>
<span data-ttu-id="0a73a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a73a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a73a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a73a-118">-InputObject</span></span>
<span data-ttu-id="0a73a-119">要移除的實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="0a73a-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a73a-120">-Name</span></span>
<span data-ttu-id="0a73a-121">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a73a-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a73a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a73a-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a73a-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a73a-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a73a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a73a-124">-ResourceId</span></span>
<span data-ttu-id="0a73a-125">要移除的實例資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a73a-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73a-126">-確認</span><span class="sxs-lookup"><span data-stu-id="0a73a-126">-Confirm</span></span>
<span data-ttu-id="0a73a-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a73a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a73a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a73a-128">-WhatIf</span></span>
<span data-ttu-id="0a73a-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a73a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a73a-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a73a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a73a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a73a-131">CommonParameters</span></span>
<span data-ttu-id="0a73a-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a73a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a73a-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a73a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a73a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0a73a-134">INPUTS</span></span>

### <span data-ttu-id="0a73a-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="0a73a-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="0a73a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0a73a-136">System.String</span></span>

## <span data-ttu-id="0a73a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0a73a-137">OUTPUTS</span></span>

### <span data-ttu-id="0a73a-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a73a-138">System.Object</span></span>
## <span data-ttu-id="0a73a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0a73a-139">NOTES</span></span>

## <span data-ttu-id="0a73a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a73a-140">RELATED LINKS</span></span>
