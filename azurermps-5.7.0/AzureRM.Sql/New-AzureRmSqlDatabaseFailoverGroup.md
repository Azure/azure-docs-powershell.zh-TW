---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444232"
---
# <span data-ttu-id="d8563-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d8563-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8563-102">SYNOPSIS</span></span>
<span data-ttu-id="d8563-103">這個命令會建立新的 Azure SQL Database 容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="d8563-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8563-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8563-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8563-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8563-105">DESCRIPTION</span></span>
<span data-ttu-id="d8563-106">針對指定的伺服器建立新的 Azure SQL Database 容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="d8563-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="d8563-107">兩個 Azure SQL Database TDS 端點是在 FailoverGroupName 建立。 SqlDatabaseDnsSuffix (例如，FailoverGroupName.database.windows.net) 和 FailoverGroupName. SqlDatabaseDnsSuffix。</span><span class="sxs-lookup"><span data-stu-id="d8563-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="d8563-108">這些端點可以用來分別連線到 [轉移] 群組中的主要和次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="d8563-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="d8563-109">如果主伺服器受到中斷影響，端點和資料庫的自動容錯移轉會根據容錯移轉群組的容錯移轉原則和寬限期來觸發。</span><span class="sxs-lookup"><span data-stu-id="d8563-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="d8563-110">新建立的容錯移轉群組不包含任何資料庫。</span><span class="sxs-lookup"><span data-stu-id="d8563-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="d8563-111">若要控制容錯移轉群組中的一組資料庫，請使用 [AzureRmSqlDatabaseToFailoverGroup] 和 [Remove-AzureRmSqlDatabaseFromFailoverGroup] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8563-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="d8563-112">在容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="d8563-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="d8563-113">示例</span><span class="sxs-lookup"><span data-stu-id="d8563-113">EXAMPLES</span></span>

### <span data-ttu-id="d8563-114">範例1</span><span class="sxs-lookup"><span data-stu-id="d8563-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="d8563-115">這個命令會針對相同資源群組中的兩個伺服器，建立一個新的容錯移轉群組，其中包含容錯移轉原則「自動」。</span><span class="sxs-lookup"><span data-stu-id="d8563-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="d8563-116">範例2</span><span class="sxs-lookup"><span data-stu-id="d8563-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="d8563-117">這個命令會針對不同資源群組中的兩個伺服器，建立一個新的容錯移轉群組，其中的容錯移轉原則為「手動」。</span><span class="sxs-lookup"><span data-stu-id="d8563-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="d8563-118">參數</span><span class="sxs-lookup"><span data-stu-id="d8563-118">PARAMETERS</span></span>

### <span data-ttu-id="d8563-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="d8563-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="d8563-120">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="d8563-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="d8563-121">尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="d8563-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="d8563-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8563-122">-DefaultProfile</span></span>
<span data-ttu-id="d8563-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d8563-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8563-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d8563-124">-FailoverGroupName</span></span>
<span data-ttu-id="d8563-125">要建立之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8563-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8563-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d8563-126">-FailoverPolicy</span></span>
<span data-ttu-id="d8563-127">Azure SQL Database 容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="d8563-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="d8563-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="d8563-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="d8563-129">啟動自動容錯移轉前的間隔如果主伺服器發生停機，而容錯移轉無法在不遺失資料的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="d8563-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="d8563-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8563-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d8563-131">Azure SQL Database 容錯移轉群組的次要資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8563-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8563-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d8563-132">-PartnerServerName</span></span>
<span data-ttu-id="d8563-133">Azure SQL Database 容錯移轉群組的次要伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d8563-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8563-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8563-134">-ResourceGroupName</span></span>
<span data-ttu-id="d8563-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8563-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8563-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8563-136">-ServerName</span></span>
<span data-ttu-id="d8563-137">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8563-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="d8563-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8563-138">CommonParameters</span></span>
<span data-ttu-id="d8563-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8563-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8563-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8563-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8563-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d8563-141">INPUTS</span></span>

### <span data-ttu-id="d8563-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d8563-142">System.String</span></span>

## <span data-ttu-id="d8563-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d8563-143">OUTPUTS</span></span>

### <span data-ttu-id="d8563-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d8563-144">System.Object</span></span>

## <span data-ttu-id="d8563-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d8563-145">NOTES</span></span>

## <span data-ttu-id="d8563-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8563-146">RELATED LINKS</span></span>

[<span data-ttu-id="d8563-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8563-148">AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8563-149">附加 AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d8563-150">移除-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d8563-151">切換 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8563-152">移除-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8563-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8563-153">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d8563-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
