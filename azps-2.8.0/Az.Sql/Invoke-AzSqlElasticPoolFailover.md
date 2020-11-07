---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: c07141d8a91974d511653217885b21a50a0b87f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792463"
---
# <span data-ttu-id="ccfb3-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="ccfb3-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="ccfb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccfb3-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfb3-103">針對彈性池進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="ccfb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="ccfb3-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccfb3-105">說明</span><span class="sxs-lookup"><span data-stu-id="ccfb3-105">DESCRIPTION</span></span>
<span data-ttu-id="ccfb3-106">Invoke-AzSqlElasticPoolFailover Cmdlet 會針對彈性池進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="ccfb3-107">在執行此 Cmdlet 之後，將會在彈性池中的所有資料庫上進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="ccfb3-108">示例</span><span class="sxs-lookup"><span data-stu-id="ccfb3-108">EXAMPLES</span></span>

### <span data-ttu-id="ccfb3-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ccfb3-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ccfb3-110">這個命令會將「Server01」伺服器上名為「ElasticPool01」的彈性池容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="ccfb3-111">這表示將會在彈性池（名為「ElasticPool01」）中的所有資料庫上進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="ccfb3-112">參數</span><span class="sxs-lookup"><span data-stu-id="ccfb3-112">PARAMETERS</span></span>

### <span data-ttu-id="ccfb3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccfb3-113">-AsJob</span></span>
<span data-ttu-id="ccfb3-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ccfb3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccfb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccfb3-115">-DefaultProfile</span></span>
<span data-ttu-id="ccfb3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccfb3-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ccfb3-117">-ElasticPoolName</span></span>
<span data-ttu-id="ccfb3-118">要移除之 Azure SQL 彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="ccfb3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ccfb3-119">-Force</span></span>
<span data-ttu-id="ccfb3-120">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="ccfb3-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ccfb3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccfb3-121">-PassThru</span></span>
<span data-ttu-id="ccfb3-122">成功執行時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="ccfb3-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccfb3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccfb3-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccfb3-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccfb3-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ccfb3-126">-ServerName</span></span>
<span data-ttu-id="ccfb3-127">彈性池所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="ccfb3-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ccfb3-128">-Confirm</span></span>
<span data-ttu-id="ccfb3-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccfb3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccfb3-130">-WhatIf</span></span>
<span data-ttu-id="ccfb3-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccfb3-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccfb3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfb3-133">CommonParameters</span></span>
<span data-ttu-id="ccfb3-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfb3-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ccfb3-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfb3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ccfb3-136">INPUTS</span></span>

### <span data-ttu-id="ccfb3-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ccfb3-137">System.String</span></span>

## <span data-ttu-id="ccfb3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ccfb3-138">OUTPUTS</span></span>

## <span data-ttu-id="ccfb3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ccfb3-139">NOTES</span></span>

## <span data-ttu-id="ccfb3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccfb3-140">RELATED LINKS</span></span>

[<span data-ttu-id="ccfb3-141">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccfb3-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="ccfb3-142">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ccfb3-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="ccfb3-143">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ccfb3-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="ccfb3-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="ccfb3-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="ccfb3-145">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccfb3-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ccfb3-146">移除-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccfb3-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="ccfb3-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccfb3-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="ccfb3-148">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ccfb3-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)