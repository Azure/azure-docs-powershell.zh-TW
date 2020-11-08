---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141241"
---
# <span data-ttu-id="7f378-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f378-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="7f378-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f378-102">SYNOPSIS</span></span>
<span data-ttu-id="7f378-103">刪除彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="7f378-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="7f378-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f378-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f378-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f378-105">DESCRIPTION</span></span>
<span data-ttu-id="7f378-106">**AzSqlElasticPool** Cmdlet 會刪除 Azure SQL 資料庫彈性池。</span><span class="sxs-lookup"><span data-stu-id="7f378-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="7f378-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f378-107">EXAMPLES</span></span>

### <span data-ttu-id="7f378-108">範例1：刪除彈性池</span><span class="sxs-lookup"><span data-stu-id="7f378-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="7f378-109">這個命令會刪除一個名為 ElasticPool01 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="7f378-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="7f378-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f378-110">PARAMETERS</span></span>

### <span data-ttu-id="7f378-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f378-111">-DefaultProfile</span></span>
<span data-ttu-id="7f378-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7f378-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f378-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7f378-113">-ElasticPoolName</span></span>
<span data-ttu-id="7f378-114">指定此 Cmdlet 刪除的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f378-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7f378-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7f378-115">-Force</span></span>
<span data-ttu-id="7f378-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7f378-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f378-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f378-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f378-118">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f378-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="7f378-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f378-119">-ServerName</span></span>
<span data-ttu-id="7f378-120">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="7f378-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="7f378-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7f378-121">-Confirm</span></span>
<span data-ttu-id="7f378-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f378-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f378-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f378-123">-WhatIf</span></span>
<span data-ttu-id="7f378-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f378-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f378-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f378-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f378-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f378-126">CommonParameters</span></span>
<span data-ttu-id="7f378-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f378-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f378-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f378-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f378-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7f378-129">INPUTS</span></span>

### <span data-ttu-id="7f378-130">System.object</span><span class="sxs-lookup"><span data-stu-id="7f378-130">System.String</span></span>

## <span data-ttu-id="7f378-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7f378-131">OUTPUTS</span></span>

### <span data-ttu-id="7f378-132">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="7f378-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7f378-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7f378-133">NOTES</span></span>

## <span data-ttu-id="7f378-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f378-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f378-135">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f378-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="7f378-136">AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7f378-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="7f378-137">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7f378-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="7f378-138">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f378-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="7f378-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7f378-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="7f378-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="7f378-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


