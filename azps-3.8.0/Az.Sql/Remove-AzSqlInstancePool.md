---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958887"
---
# <span data-ttu-id="26fce-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="26fce-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="26fce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26fce-102">SYNOPSIS</span></span>
<span data-ttu-id="26fce-103">移除 Azure SQL 實例池。</span><span class="sxs-lookup"><span data-stu-id="26fce-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="26fce-104">句法</span><span class="sxs-lookup"><span data-stu-id="26fce-104">SYNTAX</span></span>

### <span data-ttu-id="26fce-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="26fce-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26fce-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26fce-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26fce-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26fce-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26fce-108">說明</span><span class="sxs-lookup"><span data-stu-id="26fce-108">DESCRIPTION</span></span>
<span data-ttu-id="26fce-109">**AzSqlInstancePool** Cmdlet 會移除 Azure SQL 實例池。</span><span class="sxs-lookup"><span data-stu-id="26fce-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="26fce-110">示例</span><span class="sxs-lookup"><span data-stu-id="26fce-110">EXAMPLES</span></span>

### <span data-ttu-id="26fce-111">範例1：移除實例池</span><span class="sxs-lookup"><span data-stu-id="26fce-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="26fce-112">範例2：依資源識別碼移除實例池</span><span class="sxs-lookup"><span data-stu-id="26fce-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="26fce-113">範例3：以實例池物件移除實例池</span><span class="sxs-lookup"><span data-stu-id="26fce-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="26fce-114">這個命令會移除一個名為 instancePool0 的實例池。</span><span class="sxs-lookup"><span data-stu-id="26fce-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="26fce-115">參數</span><span class="sxs-lookup"><span data-stu-id="26fce-115">PARAMETERS</span></span>

### <span data-ttu-id="26fce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fce-116">-DefaultProfile</span></span>
<span data-ttu-id="26fce-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26fce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26fce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26fce-118">-InputObject</span></span>
<span data-ttu-id="26fce-119">要移除的實例池物件。</span><span class="sxs-lookup"><span data-stu-id="26fce-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="26fce-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="26fce-120">-Name</span></span>
<span data-ttu-id="26fce-121">實例池的名稱。</span><span class="sxs-lookup"><span data-stu-id="26fce-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="26fce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26fce-122">-ResourceGroupName</span></span>
<span data-ttu-id="26fce-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26fce-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="26fce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26fce-124">-ResourceId</span></span>
<span data-ttu-id="26fce-125">要移除的實例池資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="26fce-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="26fce-126">-確認</span><span class="sxs-lookup"><span data-stu-id="26fce-126">-Confirm</span></span>
<span data-ttu-id="26fce-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26fce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26fce-128">-WhatIf</span></span>
<span data-ttu-id="26fce-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26fce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26fce-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26fce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fce-131">CommonParameters</span></span>
<span data-ttu-id="26fce-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26fce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fce-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26fce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fce-134">輸入</span><span class="sxs-lookup"><span data-stu-id="26fce-134">INPUTS</span></span>

### <span data-ttu-id="26fce-135">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="26fce-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="26fce-136">System.object</span><span class="sxs-lookup"><span data-stu-id="26fce-136">System.String</span></span>

## <span data-ttu-id="26fce-137">輸出</span><span class="sxs-lookup"><span data-stu-id="26fce-137">OUTPUTS</span></span>

### <span data-ttu-id="26fce-138">System.object</span><span class="sxs-lookup"><span data-stu-id="26fce-138">System.Object</span></span>
## <span data-ttu-id="26fce-139">筆記</span><span class="sxs-lookup"><span data-stu-id="26fce-139">NOTES</span></span>

## <span data-ttu-id="26fce-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="26fce-140">RELATED LINKS</span></span>