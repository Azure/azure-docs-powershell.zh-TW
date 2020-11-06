---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: e5452ef5b6d8b2e5535c5388d5d42698aa7c261f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447581"
---
# <span data-ttu-id="b412e-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="b412e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b412e-102">SYNOPSIS</span></span>
<span data-ttu-id="b412e-103">修改 Azure SQL Database 容錯移轉群組的設定。</span><span class="sxs-lookup"><span data-stu-id="b412e-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b412e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b412e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b412e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b412e-105">DESCRIPTION</span></span>
<span data-ttu-id="b412e-106">這個命令會修改 Azure SQL Database 容錯移轉群組的設定。</span><span class="sxs-lookup"><span data-stu-id="b412e-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="b412e-107">應使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="b412e-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="b412e-108">若要控制群組中的一組資料庫，請改用 [Add-AzureRmSqlDatabaseToFailoverGroup] 和 [Remove-AzureRmSqlDatabaseFromFailoverGroup]。</span><span class="sxs-lookup"><span data-stu-id="b412e-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="b412e-109">在容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="b412e-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="b412e-110">示例</span><span class="sxs-lookup"><span data-stu-id="b412e-110">EXAMPLES</span></span>

### <span data-ttu-id="b412e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b412e-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="b412e-112">將容錯移轉群組的容錯移轉原則設定為「自動」。</span><span class="sxs-lookup"><span data-stu-id="b412e-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="b412e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="b412e-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="b412e-114">透過 [轉移] 群組中的管道，將容錯移轉群組的容錯移轉原則設定為「手動」。</span><span class="sxs-lookup"><span data-stu-id="b412e-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="b412e-115">參數</span><span class="sxs-lookup"><span data-stu-id="b412e-115">PARAMETERS</span></span>

### <span data-ttu-id="b412e-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="b412e-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="b412e-117">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b412e-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="b412e-118">尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="b412e-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b412e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b412e-119">-DefaultProfile</span></span>
<span data-ttu-id="b412e-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b412e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b412e-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b412e-121">-FailoverGroupName</span></span>
<span data-ttu-id="b412e-122">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b412e-122">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b412e-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b412e-123">-FailoverPolicy</span></span>
<span data-ttu-id="b412e-124">Azure SQL Database 容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="b412e-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b412e-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="b412e-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="b412e-126">如果主要伺服器發生停機，就會啟動自動容錯移轉前的間隔。</span><span class="sxs-lookup"><span data-stu-id="b412e-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="b412e-127">這表示 Azure SQL 資料庫將不會在寬限期到期前啟動自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b412e-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="b412e-128">請注意，使用 AllowDataLoss 選項的容錯移轉作業可能會因非同步同步處理的性質而導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="b412e-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b412e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b412e-129">-ResourceGroupName</span></span>
<span data-ttu-id="b412e-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b412e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b412e-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b412e-131">-ServerName</span></span>
<span data-ttu-id="b412e-132">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b412e-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="b412e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b412e-133">CommonParameters</span></span>
<span data-ttu-id="b412e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b412e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b412e-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b412e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b412e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b412e-136">INPUTS</span></span>

### <span data-ttu-id="b412e-137">System.object</span><span class="sxs-lookup"><span data-stu-id="b412e-137">System.String</span></span>

## <span data-ttu-id="b412e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b412e-138">OUTPUTS</span></span>

### <span data-ttu-id="b412e-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b412e-139">System.Object</span></span>

## <span data-ttu-id="b412e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b412e-140">NOTES</span></span>

## <span data-ttu-id="b412e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b412e-141">RELATED LINKS</span></span>

[<span data-ttu-id="b412e-142">新-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b412e-143">AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b412e-144">附加 AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b412e-145">移除-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="b412e-146">切換 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b412e-147">移除-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b412e-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b412e-148">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b412e-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
