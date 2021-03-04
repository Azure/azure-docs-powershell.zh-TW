---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 013a7c40a5acfb4306d53e0ff5b8da1b54f86e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914345"
---
# <span data-ttu-id="d7d90-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="d7d90-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="d7d90-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7d90-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d90-103">在資訊資料庫上獲得作業狀態。</span><span class="sxs-lookup"><span data-stu-id="d7d90-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="d7d90-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7d90-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7d90-105">描述</span><span class="sxs-lookup"><span data-stu-id="d7d90-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d90-106">**Get-AzSqlElasticPoolActivity** Cmdlet 會取得 Azure SQL Database 的彈性資料庫作業狀態。</span><span class="sxs-lookup"><span data-stu-id="d7d90-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="d7d90-107">您可以同時查看資料庫建立和組組更新的狀態。</span><span class="sxs-lookup"><span data-stu-id="d7d90-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="d7d90-108">例子</span><span class="sxs-lookup"><span data-stu-id="d7d90-108">EXAMPLES</span></span>

### <span data-ttu-id="d7d90-109">範例 1：取得彈性資料庫的作業狀態</span><span class="sxs-lookup"><span data-stu-id="d7d90-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d7d90-110">此命令會獲得名為Pool01 之資料庫的作業狀態。</span><span class="sxs-lookup"><span data-stu-id="d7d90-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="d7d90-111">參數</span><span class="sxs-lookup"><span data-stu-id="d7d90-111">PARAMETERS</span></span>

### <span data-ttu-id="d7d90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d90-112">-DefaultProfile</span></span>
<span data-ttu-id="d7d90-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d7d90-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7d90-114">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="d7d90-114">-ElasticPoolName</span></span>
<span data-ttu-id="d7d90-115">指定泳層資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7d90-115">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d90-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d7d90-116">-OperationId</span></span>
<span data-ttu-id="d7d90-117">要取回之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7d90-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d90-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d90-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7d90-119">指定指派了壓縮資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d7d90-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="d7d90-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d7d90-120">-ServerName</span></span>
<span data-ttu-id="d7d90-121">指定包含集區集區的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d7d90-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="d7d90-122">-確認</span><span class="sxs-lookup"><span data-stu-id="d7d90-122">-Confirm</span></span>
<span data-ttu-id="d7d90-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d7d90-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d90-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d90-124">-WhatIf</span></span>
<span data-ttu-id="d7d90-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7d90-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d90-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7d90-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d90-127">CommonParameters</span></span>
<span data-ttu-id="d7d90-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7d90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d90-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7d90-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d90-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d7d90-130">INPUTS</span></span>

### <span data-ttu-id="d7d90-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d7d90-131">System.String</span></span>

### <span data-ttu-id="d7d90-132">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d7d90-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d7d90-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d7d90-133">OUTPUTS</span></span>

### <span data-ttu-id="d7d90-134">Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="d7d90-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="d7d90-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d7d90-135">NOTES</span></span>

## <span data-ttu-id="d7d90-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7d90-136">RELATED LINKS</span></span>

[<span data-ttu-id="d7d90-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d7d90-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="d7d90-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="d7d90-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="d7d90-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d7d90-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="d7d90-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d7d90-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="d7d90-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d7d90-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


