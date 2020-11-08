---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137106"
---
# <span data-ttu-id="670a8-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="670a8-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="670a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="670a8-102">SYNOPSIS</span></span>
<span data-ttu-id="670a8-103">針對彈性池進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="670a8-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="670a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="670a8-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="670a8-105">DESCRIPTION</span></span>
<span data-ttu-id="670a8-106">Invoke-AzSqlElasticPoolFailover Cmdlet 會針對彈性池進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="670a8-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="670a8-107">在執行此 Cmdlet 之後，將會在彈性池中的所有資料庫上進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="670a8-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="670a8-108">示例</span><span class="sxs-lookup"><span data-stu-id="670a8-108">EXAMPLES</span></span>

### <span data-ttu-id="670a8-109">範例1</span><span class="sxs-lookup"><span data-stu-id="670a8-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="670a8-110">這個命令會將「Server01」伺服器上名為「ElasticPool01」的彈性池容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="670a8-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="670a8-111">這表示將會在彈性池（名為「ElasticPool01」）中的所有資料庫上進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="670a8-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="670a8-112">參數</span><span class="sxs-lookup"><span data-stu-id="670a8-112">PARAMETERS</span></span>

### <span data-ttu-id="670a8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="670a8-113">-AsJob</span></span>
<span data-ttu-id="670a8-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="670a8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="670a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670a8-115">-DefaultProfile</span></span>
<span data-ttu-id="670a8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="670a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670a8-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="670a8-117">-ElasticPoolName</span></span>
<span data-ttu-id="670a8-118">要移除之 Azure SQL 彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="670a8-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="670a8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="670a8-119">-Force</span></span>
<span data-ttu-id="670a8-120">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="670a8-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="670a8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="670a8-121">-PassThru</span></span>
<span data-ttu-id="670a8-122">成功執行時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="670a8-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="670a8-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="670a8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="670a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="670a8-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="670a8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="670a8-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="670a8-126">-ServerName</span></span>
<span data-ttu-id="670a8-127">彈性池所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="670a8-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="670a8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="670a8-128">-Confirm</span></span>
<span data-ttu-id="670a8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="670a8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="670a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670a8-130">-WhatIf</span></span>
<span data-ttu-id="670a8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="670a8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="670a8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="670a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="670a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670a8-133">CommonParameters</span></span>
<span data-ttu-id="670a8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="670a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670a8-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="670a8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670a8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="670a8-136">INPUTS</span></span>

### <span data-ttu-id="670a8-137">System.object</span><span class="sxs-lookup"><span data-stu-id="670a8-137">System.String</span></span>

## <span data-ttu-id="670a8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="670a8-138">OUTPUTS</span></span>

## <span data-ttu-id="670a8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="670a8-139">NOTES</span></span>

## <span data-ttu-id="670a8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="670a8-140">RELATED LINKS</span></span>

[<span data-ttu-id="670a8-141">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="670a8-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="670a8-142">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="670a8-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="670a8-143">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="670a8-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="670a8-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="670a8-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="670a8-145">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="670a8-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="670a8-146">移除-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="670a8-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="670a8-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="670a8-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="670a8-148">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="670a8-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)