---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a4440601610af0b55282cbe0e78209379f570edb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444276"
---
# <span data-ttu-id="766ae-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="766ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="766ae-102">SYNOPSIS</span></span>
<span data-ttu-id="766ae-103">取得或列出 Azure SQL Database 容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="766ae-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="766ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="766ae-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="766ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="766ae-105">DESCRIPTION</span></span>
<span data-ttu-id="766ae-106">取得特定的 Azure SQL Database 容錯移轉群組，或列出伺服器上的容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="766ae-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="766ae-107">[容錯移轉] 群組中的任何一個伺服器都可以用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="766ae-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="766ae-108">傳回的值將反映特定伺服器相對於容錯移轉群組的狀態。</span><span class="sxs-lookup"><span data-stu-id="766ae-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="766ae-109">示例</span><span class="sxs-lookup"><span data-stu-id="766ae-109">EXAMPLES</span></span>

### <span data-ttu-id="766ae-110">範例1</span><span class="sxs-lookup"><span data-stu-id="766ae-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="766ae-111">列出伺服器上的所有容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="766ae-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="766ae-112">範例2</span><span class="sxs-lookup"><span data-stu-id="766ae-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="766ae-113">取得特定的容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="766ae-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="766ae-114">參數</span><span class="sxs-lookup"><span data-stu-id="766ae-114">PARAMETERS</span></span>

### <span data-ttu-id="766ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766ae-115">-DefaultProfile</span></span>
<span data-ttu-id="766ae-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="766ae-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="766ae-117">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="766ae-117">-FailoverGroupName</span></span>
<span data-ttu-id="766ae-118">要檢索之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="766ae-118">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="766ae-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="766ae-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="766ae-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="766ae-121">-ServerName</span></span>
<span data-ttu-id="766ae-122">要從中檢索容錯移轉群組的 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="766ae-122">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="766ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766ae-123">CommonParameters</span></span>
<span data-ttu-id="766ae-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="766ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766ae-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="766ae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766ae-126">輸入</span><span class="sxs-lookup"><span data-stu-id="766ae-126">INPUTS</span></span>

### <span data-ttu-id="766ae-127">System.object</span><span class="sxs-lookup"><span data-stu-id="766ae-127">System.String</span></span>

## <span data-ttu-id="766ae-128">輸出</span><span class="sxs-lookup"><span data-stu-id="766ae-128">OUTPUTS</span></span>

### <span data-ttu-id="766ae-129">System.object</span><span class="sxs-lookup"><span data-stu-id="766ae-129">System.Object</span></span>

## <span data-ttu-id="766ae-130">筆記</span><span class="sxs-lookup"><span data-stu-id="766ae-130">NOTES</span></span>

## <span data-ttu-id="766ae-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="766ae-131">RELATED LINKS</span></span>

[<span data-ttu-id="766ae-132">新-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="766ae-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="766ae-134">附加 AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="766ae-135">移除-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="766ae-136">切換 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="766ae-137">移除-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="766ae-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="766ae-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="766ae-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
