---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: a6b5b21b8911aa8d156ced40476d1b0ecadad361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447610"
---
# <span data-ttu-id="ea924-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ea924-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="ea924-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea924-102">SYNOPSIS</span></span>
<span data-ttu-id="ea924-103">刪除彈性資料庫池。</span><span class="sxs-lookup"><span data-stu-id="ea924-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea924-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea924-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea924-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea924-105">DESCRIPTION</span></span>
<span data-ttu-id="ea924-106">**AzureRmSqlElasticPool** Cmdlet 會刪除 Azure SQL 資料庫彈性池。</span><span class="sxs-lookup"><span data-stu-id="ea924-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="ea924-107">示例</span><span class="sxs-lookup"><span data-stu-id="ea924-107">EXAMPLES</span></span>

### <span data-ttu-id="ea924-108">範例1：刪除彈性池</span><span class="sxs-lookup"><span data-stu-id="ea924-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ea924-109">這個命令會刪除一個名為 ElasticPool01 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="ea924-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="ea924-110">參數</span><span class="sxs-lookup"><span data-stu-id="ea924-110">PARAMETERS</span></span>

### <span data-ttu-id="ea924-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea924-111">-DefaultProfile</span></span>
<span data-ttu-id="ea924-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ea924-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ea924-113">-ElasticPoolName</span></span>
<span data-ttu-id="ea924-114">指定此 Cmdlet 刪除的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea924-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ea924-115">-Force</span></span>
<span data-ttu-id="ea924-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ea924-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea924-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea924-118">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea924-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea924-119">-ServerName</span></span>
<span data-ttu-id="ea924-120">指定主持彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ea924-120">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ea924-121">-Confirm</span></span>
<span data-ttu-id="ea924-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea924-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea924-123">-WhatIf</span></span>
<span data-ttu-id="ea924-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea924-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea924-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea924-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea924-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea924-126">CommonParameters</span></span>
<span data-ttu-id="ea924-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea924-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea924-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea924-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea924-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ea924-129">INPUTS</span></span>

### <span data-ttu-id="ea924-130">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="ea924-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="ea924-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ea924-131">OUTPUTS</span></span>

### <span data-ttu-id="ea924-132">AzureSqlElasticPoolModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="ea924-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="ea924-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ea924-133">NOTES</span></span>

## <span data-ttu-id="ea924-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea924-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea924-135">AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ea924-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ea924-136">AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ea924-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="ea924-137">AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ea924-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="ea924-138">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ea924-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ea924-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ea924-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ea924-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ea924-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


