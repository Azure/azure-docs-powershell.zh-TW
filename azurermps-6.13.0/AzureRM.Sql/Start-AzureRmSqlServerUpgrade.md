---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448169"
---
# <span data-ttu-id="39546-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="39546-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="39546-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39546-102">SYNOPSIS</span></span>
<span data-ttu-id="39546-103">開始升級 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="39546-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39546-104">句法</span><span class="sxs-lookup"><span data-stu-id="39546-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39546-105">說明</span><span class="sxs-lookup"><span data-stu-id="39546-105">DESCRIPTION</span></span>
<span data-ttu-id="39546-106">**AzureRmSqlServerUpgrade** Cmdlet 會開始將 Azure SQL Database server 版本11升級到版本12。</span><span class="sxs-lookup"><span data-stu-id="39546-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="39546-107">您可以使用 Get-AzureRmSqlServerUpgrade Cmdlet 監視升級的進度。</span><span class="sxs-lookup"><span data-stu-id="39546-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="39546-108">示例</span><span class="sxs-lookup"><span data-stu-id="39546-108">EXAMPLES</span></span>

### <span data-ttu-id="39546-109">範例1：升級伺服器</span><span class="sxs-lookup"><span data-stu-id="39546-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="39546-110">這個命令會升級指派給資源群組 TesourceGroup01 的名為 server01 的伺服器。</span><span class="sxs-lookup"><span data-stu-id="39546-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="39546-111">範例2：使用排程時間和資料庫建議來升級伺服器</span><span class="sxs-lookup"><span data-stu-id="39546-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="39546-112">第一個命令會在未來使用 Get-Date Cmdlet 來建立5分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="39546-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="39546-113">該命令會將 $ScheduleTime 中的日期儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="39546-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="39546-114">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="39546-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="39546-115">第二個命令會建立 **RecommendedDatabaseProperties** 物件，然後將該物件儲存在 $DatabaseMap 的變數中。</span><span class="sxs-lookup"><span data-stu-id="39546-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>
<span data-ttu-id="39546-116">接下來的三個命令會將值指派給儲存在 $DatabaseMap 的物件屬性。</span><span class="sxs-lookup"><span data-stu-id="39546-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>
<span data-ttu-id="39546-117">最後一個命令會將名為 Server01 的現有伺服器升級為版本12.0。</span><span class="sxs-lookup"><span data-stu-id="39546-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="39546-118">在執行命令之後，最早要升級的時間是由 $ScheduleTime 變數所指定。</span><span class="sxs-lookup"><span data-stu-id="39546-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="39546-119">升級之後，資料庫 contosodb 將執行標準版，並擁有服務層級目標 S0。</span><span class="sxs-lookup"><span data-stu-id="39546-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="39546-120">參數</span><span class="sxs-lookup"><span data-stu-id="39546-120">PARAMETERS</span></span>

### <span data-ttu-id="39546-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="39546-121">-DatabaseCollection</span></span>
<span data-ttu-id="39546-122">指定此 Cmdlet 用來進行伺服器升級的 **RecommendedDatabaseProperties** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="39546-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39546-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39546-123">-DefaultProfile</span></span>
<span data-ttu-id="39546-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="39546-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39546-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="39546-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="39546-126">指定要用於伺服器升級的 **UpgradeRecommendedElasticPoolProperties** 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="39546-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39546-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39546-127">-ResourceGroupName</span></span>
<span data-ttu-id="39546-128">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39546-128">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="39546-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="39546-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="39546-130">指定要升級伺服器的最早時間（做為 **DateTime** 物件）。</span><span class="sxs-lookup"><span data-stu-id="39546-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="39546-131">在 ISO8601 格式中指定一個值，並以 [ (UTC]) 的 [協調世界時間]。</span><span class="sxs-lookup"><span data-stu-id="39546-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="39546-132">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="39546-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39546-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="39546-133">-ServerName</span></span>
<span data-ttu-id="39546-134">指定此 Cmdlet 升級的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="39546-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39546-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="39546-135">-ServerVersion</span></span>
<span data-ttu-id="39546-136">指定此 Cmdlet 升級伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="39546-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="39546-137">唯一有效的值是12.0。</span><span class="sxs-lookup"><span data-stu-id="39546-137">The only valid value is 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39546-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39546-138">CommonParameters</span></span>
<span data-ttu-id="39546-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39546-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39546-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39546-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39546-141">輸入</span><span class="sxs-lookup"><span data-stu-id="39546-141">INPUTS</span></span>

### <span data-ttu-id="39546-142">System.object</span><span class="sxs-lookup"><span data-stu-id="39546-142">System.String</span></span>

## <span data-ttu-id="39546-143">輸出</span><span class="sxs-lookup"><span data-stu-id="39546-143">OUTPUTS</span></span>

### <span data-ttu-id="39546-144">AzureSqlServerUpgradeStartModel 中的 [ServerUpgrade]</span><span class="sxs-lookup"><span data-stu-id="39546-144">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeStartModel</span></span>

## <span data-ttu-id="39546-145">筆記</span><span class="sxs-lookup"><span data-stu-id="39546-145">NOTES</span></span>

## <span data-ttu-id="39546-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="39546-146">RELATED LINKS</span></span>

[<span data-ttu-id="39546-147">AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="39546-147">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="39546-148">停止 AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="39546-148">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="39546-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="39546-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


