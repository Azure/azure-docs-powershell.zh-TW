---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 47b519b324018e4fc369d281f7fb7eac554ac571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957069"
---
# <span data-ttu-id="473cd-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="473cd-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="473cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="473cd-102">SYNOPSIS</span></span>
<span data-ttu-id="473cd-103">刪除現有的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="473cd-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="473cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="473cd-104">SYNTAX</span></span>

### <span data-ttu-id="473cd-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="473cd-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473cd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="473cd-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473cd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="473cd-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="473cd-108">說明</span><span class="sxs-lookup"><span data-stu-id="473cd-108">DESCRIPTION</span></span>
<span data-ttu-id="473cd-109">刪除現有的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="473cd-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="473cd-110">示例</span><span class="sxs-lookup"><span data-stu-id="473cd-110">EXAMPLES</span></span>

### <span data-ttu-id="473cd-111">範例 1-依名稱刪除現有的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="473cd-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="473cd-112">上述命令會刪除在資源群組 "testrg" 中找到的群集 "mykustocluster" 中名為 "mykustodatabase" 的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="473cd-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="473cd-113">範例 2-透過管道刪除現有的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="473cd-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="473cd-114">上述命令會在使用 Cmdlet 之資源群組 "testrg" 中找到的群集 "mykustocluster" 中，取得名為 "mykustodatabase" 的 Kusto 資料庫 `Get-AzKustoDatabase` ，然後再將結果設為 [ `Remove-AzKustoDatabase` 刪除]。</span><span class="sxs-lookup"><span data-stu-id="473cd-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="473cd-115">參數</span><span class="sxs-lookup"><span data-stu-id="473cd-115">PARAMETERS</span></span>

### <span data-ttu-id="473cd-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="473cd-116">-ClusterName</span></span>
<span data-ttu-id="473cd-117">資料庫所在之群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="473cd-117">Name of the cluster under which the database exists.</span></span>

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

### <span data-ttu-id="473cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473cd-118">-DefaultProfile</span></span>
<span data-ttu-id="473cd-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="473cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="473cd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="473cd-120">-InputObject</span></span>
<span data-ttu-id="473cd-121">Kusto 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="473cd-121">Kusto database object.</span></span>

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

### <span data-ttu-id="473cd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="473cd-122">-Name</span></span>
<span data-ttu-id="473cd-123">要移除之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="473cd-123">Name of database to be removed.</span></span>

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

### <span data-ttu-id="473cd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="473cd-124">-PassThru</span></span>
<span data-ttu-id="473cd-125">傳回是否已成功暫停指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="473cd-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="473cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="473cd-127">群集存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="473cd-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="473cd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="473cd-128">-ResourceId</span></span>
<span data-ttu-id="473cd-129">Kusto 資料庫 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="473cd-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="473cd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="473cd-130">-Confirm</span></span>
<span data-ttu-id="473cd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="473cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="473cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473cd-132">-WhatIf</span></span>
<span data-ttu-id="473cd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="473cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="473cd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="473cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="473cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473cd-135">CommonParameters</span></span>
<span data-ttu-id="473cd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="473cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473cd-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="473cd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473cd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="473cd-138">INPUTS</span></span>

### <span data-ttu-id="473cd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="473cd-139">System.String</span></span>

### <span data-ttu-id="473cd-140">PSKustoDatabase 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="473cd-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="473cd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="473cd-141">OUTPUTS</span></span>

### <span data-ttu-id="473cd-142">System.object</span><span class="sxs-lookup"><span data-stu-id="473cd-142">System.Boolean</span></span>

## <span data-ttu-id="473cd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="473cd-143">NOTES</span></span>

## <span data-ttu-id="473cd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="473cd-144">RELATED LINKS</span></span>
