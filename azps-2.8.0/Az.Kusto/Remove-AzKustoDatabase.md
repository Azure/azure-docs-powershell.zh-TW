---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612048"
---
# <span data-ttu-id="97492-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="97492-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="97492-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97492-102">SYNOPSIS</span></span>
<span data-ttu-id="97492-103">刪除現有的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="97492-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="97492-104">句法</span><span class="sxs-lookup"><span data-stu-id="97492-104">SYNTAX</span></span>

### <span data-ttu-id="97492-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="97492-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97492-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97492-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97492-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="97492-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97492-108">說明</span><span class="sxs-lookup"><span data-stu-id="97492-108">DESCRIPTION</span></span>
<span data-ttu-id="97492-109">刪除現有的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="97492-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="97492-110">示例</span><span class="sxs-lookup"><span data-stu-id="97492-110">EXAMPLES</span></span>

### <span data-ttu-id="97492-111">範例 1-依名稱刪除現有的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="97492-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="97492-112">上述命令會刪除在資源群組 "testrg" 中找到的群集 "mykustocluster" 中名為 "mykustodatabase" 的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="97492-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="97492-113">範例 2-透過管道刪除現有的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="97492-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="97492-114">上述命令會在使用 Cmdlet 之資源群組 "testrg" 中找到的群集 "mykustocluster" 中，取得名為 "mykustodatabase" 的 Kusto 資料庫 `Get-AzKustoDatabase` ，然後再將結果設為 [ `Remove-AzKustoDatabase` 刪除]。</span><span class="sxs-lookup"><span data-stu-id="97492-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="97492-115">參數</span><span class="sxs-lookup"><span data-stu-id="97492-115">PARAMETERS</span></span>

### <span data-ttu-id="97492-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="97492-116">-ClusterName</span></span>
<span data-ttu-id="97492-117">資料庫所在之群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="97492-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97492-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97492-118">-DefaultProfile</span></span>
<span data-ttu-id="97492-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97492-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97492-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97492-120">-InputObject</span></span>
<span data-ttu-id="97492-121">Kusto 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="97492-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97492-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="97492-122">-Name</span></span>
<span data-ttu-id="97492-123">要移除之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="97492-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97492-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97492-124">-PassThru</span></span>
<span data-ttu-id="97492-125">傳回是否已成功暫停指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="97492-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="97492-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97492-126">-ResourceGroupName</span></span>
<span data-ttu-id="97492-127">群集存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97492-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97492-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97492-128">-ResourceId</span></span>
<span data-ttu-id="97492-129">Kusto 資料庫 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="97492-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97492-130">-確認</span><span class="sxs-lookup"><span data-stu-id="97492-130">-Confirm</span></span>
<span data-ttu-id="97492-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97492-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97492-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97492-132">-WhatIf</span></span>
<span data-ttu-id="97492-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97492-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97492-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97492-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97492-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97492-135">CommonParameters</span></span>
<span data-ttu-id="97492-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97492-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97492-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97492-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97492-138">輸入</span><span class="sxs-lookup"><span data-stu-id="97492-138">INPUTS</span></span>

### <span data-ttu-id="97492-139">System.object</span><span class="sxs-lookup"><span data-stu-id="97492-139">System.String</span></span>

### <span data-ttu-id="97492-140">PSKustoDatabase 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="97492-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="97492-141">輸出</span><span class="sxs-lookup"><span data-stu-id="97492-141">OUTPUTS</span></span>

### <span data-ttu-id="97492-142">System.object</span><span class="sxs-lookup"><span data-stu-id="97492-142">System.Boolean</span></span>

## <span data-ttu-id="97492-143">筆記</span><span class="sxs-lookup"><span data-stu-id="97492-143">NOTES</span></span>

## <span data-ttu-id="97492-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="97492-144">RELATED LINKS</span></span>
