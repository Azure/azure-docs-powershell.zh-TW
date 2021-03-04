---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908357"
---
# <span data-ttu-id="1a351-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="1a351-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="1a351-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a351-102">SYNOPSIS</span></span>
<span data-ttu-id="1a351-103">容錯移轉資料庫。</span><span class="sxs-lookup"><span data-stu-id="1a351-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="1a351-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a351-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a351-105">描述</span><span class="sxs-lookup"><span data-stu-id="1a351-105">DESCRIPTION</span></span>
<span data-ttu-id="1a351-106">Cmdlet Invoke-AzSqlElasticPoolFailover容錯移轉會建立一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="1a351-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="1a351-107">執行此 Cmdlet 之後，資料庫集中的所有資料庫都會發生容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="1a351-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="1a351-108">例子</span><span class="sxs-lookup"><span data-stu-id="1a351-108">EXAMPLES</span></span>

### <span data-ttu-id="1a351-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="1a351-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="1a351-110">此命令將會容錯移轉名為「Server01」伺服器上名為「Pool01」的集中資料庫。</span><span class="sxs-lookup"><span data-stu-id="1a351-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="1a351-111">這表示容錯移轉會發生在名為「Pool01」的集中資料庫的所有資料庫中。</span><span class="sxs-lookup"><span data-stu-id="1a351-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="1a351-112">參數</span><span class="sxs-lookup"><span data-stu-id="1a351-112">PARAMETERS</span></span>

### <span data-ttu-id="1a351-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a351-113">-AsJob</span></span>
<span data-ttu-id="1a351-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1a351-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a351-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a351-115">-DefaultProfile</span></span>
<span data-ttu-id="1a351-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a351-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a351-117">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="1a351-117">-ElasticPoolName</span></span>
<span data-ttu-id="1a351-118">要移除的 Azure SQL 集中資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1a351-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a351-119">-強制</span><span class="sxs-lookup"><span data-stu-id="1a351-119">-Force</span></span>
<span data-ttu-id="1a351-120">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="1a351-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1a351-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a351-121">-PassThru</span></span>
<span data-ttu-id="1a351-122">成功執行時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="1a351-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="1a351-123">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1a351-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1a351-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a351-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a351-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a351-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a351-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a351-126">-ServerName</span></span>
<span data-ttu-id="1a351-127">位於 Azure SQL Server 的 Azure Sql Server 中 ，即是其中一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="1a351-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a351-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1a351-128">-Confirm</span></span>
<span data-ttu-id="1a351-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1a351-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a351-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a351-130">-WhatIf</span></span>
<span data-ttu-id="1a351-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a351-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a351-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a351-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a351-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a351-133">CommonParameters</span></span>
<span data-ttu-id="1a351-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a351-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a351-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a351-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a351-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1a351-136">INPUTS</span></span>

### <span data-ttu-id="1a351-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1a351-137">System.String</span></span>

## <span data-ttu-id="1a351-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1a351-138">OUTPUTS</span></span>

## <span data-ttu-id="1a351-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1a351-139">NOTES</span></span>

## <span data-ttu-id="1a351-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a351-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a351-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a351-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="1a351-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1a351-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="1a351-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="1a351-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="1a351-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="1a351-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="1a351-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a351-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="1a351-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a351-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="1a351-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a351-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="1a351-148">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1a351-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)