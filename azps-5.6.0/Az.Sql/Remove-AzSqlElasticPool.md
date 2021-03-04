---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: 565d22bc2860acc69f5d919bf000a564d9295ce5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902713"
---
# <span data-ttu-id="1075f-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1075f-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="1075f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1075f-102">SYNOPSIS</span></span>
<span data-ttu-id="1075f-103">刪除彈性資料庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="1075f-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="1075f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1075f-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1075f-105">描述</span><span class="sxs-lookup"><span data-stu-id="1075f-105">DESCRIPTION</span></span>
<span data-ttu-id="1075f-106">**Remove-AzSqlElasticPool** Cmdlet 會刪除 Azure SQL Database 的集中式資料庫。</span><span class="sxs-lookup"><span data-stu-id="1075f-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="1075f-107">例子</span><span class="sxs-lookup"><span data-stu-id="1075f-107">EXAMPLES</span></span>

### <span data-ttu-id="1075f-108">範例 1：刪除彈性資料庫</span><span class="sxs-lookup"><span data-stu-id="1075f-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="1075f-109">此命令會刪除名為PoolsPool01 的彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="1075f-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="1075f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1075f-110">PARAMETERS</span></span>

### <span data-ttu-id="1075f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1075f-111">-DefaultProfile</span></span>
<span data-ttu-id="1075f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1075f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1075f-113">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="1075f-113">-ElasticPoolName</span></span>
<span data-ttu-id="1075f-114">指定此 Cmdlet 刪除的作業資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1075f-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1075f-115">-強制</span><span class="sxs-lookup"><span data-stu-id="1075f-115">-Force</span></span>
<span data-ttu-id="1075f-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1075f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1075f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1075f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1075f-118">指定指派了壓縮資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1075f-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="1075f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1075f-119">-ServerName</span></span>
<span data-ttu-id="1075f-120">指定主設備資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1075f-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="1075f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1075f-121">-Confirm</span></span>
<span data-ttu-id="1075f-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1075f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1075f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1075f-123">-WhatIf</span></span>
<span data-ttu-id="1075f-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1075f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1075f-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1075f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1075f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1075f-126">CommonParameters</span></span>
<span data-ttu-id="1075f-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1075f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1075f-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1075f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1075f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1075f-129">INPUTS</span></span>

### <span data-ttu-id="1075f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1075f-130">System.String</span></span>

## <span data-ttu-id="1075f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1075f-131">OUTPUTS</span></span>

### <span data-ttu-id="1075f-132">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="1075f-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="1075f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1075f-133">NOTES</span></span>

## <span data-ttu-id="1075f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1075f-134">RELATED LINKS</span></span>

[<span data-ttu-id="1075f-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1075f-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="1075f-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1075f-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="1075f-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="1075f-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="1075f-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1075f-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="1075f-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1075f-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="1075f-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1075f-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


