---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967554"
---
# <span data-ttu-id="4c6b1-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c6b1-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="4c6b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6b1-103">刪除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="4c6b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c6b1-104">SYNTAX</span></span>

### <span data-ttu-id="4c6b1-105">ByNameWithConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="4c6b1-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c6b1-106">ByObjectWithConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="4c6b1-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c6b1-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="4c6b1-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c6b1-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="4c6b1-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c6b1-109">說明</span><span class="sxs-lookup"><span data-stu-id="4c6b1-109">DESCRIPTION</span></span>
<span data-ttu-id="4c6b1-110">**AzureSqlDatabase** Cmdlet 會依伺服器連接內容或伺服器名稱來刪除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="4c6b1-111">您可以使用 **新的 AzureSqlDatabaseServerCoNtext** Cmdlet 來建立 Azure SQL Database server 連接內容，然後將它與此 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="4c6b1-112">當您透過指定 Azure SQL 資料庫伺服器名稱來刪除資料庫時， **AzureSqlDatabase** Cmdlet 會使用名稱和目前的 Azure 訂閱資訊來執行作業。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="4c6b1-113">示例</span><span class="sxs-lookup"><span data-stu-id="4c6b1-113">EXAMPLES</span></span>

### <span data-ttu-id="4c6b1-114">範例1：移除資料庫</span><span class="sxs-lookup"><span data-stu-id="4c6b1-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="4c6b1-115">這個命令會從 Azure SQL Database server 連接內容 $CoNtext 中移除名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="4c6b1-116">範例2：使用伺服器名稱移除資料庫</span><span class="sxs-lookup"><span data-stu-id="4c6b1-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="4c6b1-117">這個命令會從 Azure SQL Database server （名為 lpqd0zbr8y）移除名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="4c6b1-118">範例3：使用管線移除資料庫</span><span class="sxs-lookup"><span data-stu-id="4c6b1-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="4c6b1-119">這個範例示範透過管線傳遞資料庫物件的替代方法。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="4c6b1-120">參數</span><span class="sxs-lookup"><span data-stu-id="4c6b1-120">PARAMETERS</span></span>

### <span data-ttu-id="4c6b1-121">-ConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="4c6b1-121">-ConnectionContext</span></span>
<span data-ttu-id="4c6b1-122">指定此 Cmdlet 從中移除資料庫的伺服器的線上內容。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6b1-123">-資料庫</span><span class="sxs-lookup"><span data-stu-id="4c6b1-123">-Database</span></span>
<span data-ttu-id="4c6b1-124">指定代表此 Cmdlet 移除之資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6b1-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c6b1-125">-DatabaseName</span></span>
<span data-ttu-id="4c6b1-126">指定此 Cmdlet 移除之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6b1-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4c6b1-127">-Force</span></span>
<span data-ttu-id="4c6b1-128">允許動作完成，不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="4c6b1-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4c6b1-129">-Profile</span></span>
<span data-ttu-id="4c6b1-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c6b1-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6b1-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c6b1-132">-ServerName</span></span>
<span data-ttu-id="4c6b1-133">指定此 Cmdlet 刪除資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6b1-134">-確認</span><span class="sxs-lookup"><span data-stu-id="4c6b1-134">-Confirm</span></span>
<span data-ttu-id="4c6b1-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c6b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6b1-136">-WhatIf</span></span>
<span data-ttu-id="4c6b1-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c6b1-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c6b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6b1-139">CommonParameters</span></span>
<span data-ttu-id="4c6b1-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6b1-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6b1-142">輸入</span><span class="sxs-lookup"><span data-stu-id="4c6b1-142">INPUTS</span></span>

### <span data-ttu-id="4c6b1-143">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="4c6b1-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="4c6b1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4c6b1-144">OUTPUTS</span></span>

## <span data-ttu-id="4c6b1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4c6b1-145">NOTES</span></span>
* <span data-ttu-id="4c6b1-146">根據此操作的嚴重性，此 Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="4c6b1-147">若要略過確認，請指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="4c6b1-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="4c6b1-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c6b1-148">RELATED LINKS</span></span>

[<span data-ttu-id="4c6b1-149">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="4c6b1-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4c6b1-150">刪除資料庫</span><span class="sxs-lookup"><span data-stu-id="4c6b1-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="4c6b1-151">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="4c6b1-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4c6b1-152">AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c6b1-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="4c6b1-153">新-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c6b1-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="4c6b1-154">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="4c6b1-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="4c6b1-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4c6b1-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


