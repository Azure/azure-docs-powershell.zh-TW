---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9677f45e772cbcb48190f5792df97e96051180c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912273"
---
# <span data-ttu-id="c39e5-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="c39e5-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="c39e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c39e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c39e5-103">在資料庫中設定進一級的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="c39e5-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="c39e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="c39e5-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c39e5-105">描述</span><span class="sxs-lookup"><span data-stu-id="c39e5-105">DESCRIPTION</span></span>
<span data-ttu-id="c39e5-106">**Update-AzSqlDatabaseAdvancedThreatProtectionSetting** Cmdlet 會設定 Azure SQL 資料庫上的進一威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="c39e5-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="c39e5-107">若要在資料庫上啟用進位威脅防護，必須在該資料庫上啟用稽核設定。</span><span class="sxs-lookup"><span data-stu-id="c39e5-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="c39e5-108">若要使用此 Cmdlet，請指定 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數來識別資料庫。 </span><span class="sxs-lookup"><span data-stu-id="c39e5-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c39e5-109">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39e5-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c39e5-110">例子</span><span class="sxs-lookup"><span data-stu-id="c39e5-110">EXAMPLES</span></span>

### <span data-ttu-id="c39e5-111">範例 1：設定資料庫的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="c39e5-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="c39e5-112">此命令會針對伺服器名為 Database01 的伺服器上名為 Database01 的資料庫設定進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="c39e5-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="c39e5-113">參數</span><span class="sxs-lookup"><span data-stu-id="c39e5-113">PARAMETERS</span></span>

### <span data-ttu-id="c39e5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c39e5-114">-DatabaseName</span></span>
<span data-ttu-id="c39e5-115">指定設定之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c39e5-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="c39e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39e5-116">-DefaultProfile</span></span>
<span data-ttu-id="c39e5-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c39e5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c39e5-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="c39e5-118">-EmailAdmins</span></span>
<span data-ttu-id="c39e5-119">指定進一步威脅防護設定是否使用電子郵件與系統管理員聯繫。</span><span class="sxs-lookup"><span data-stu-id="c39e5-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39e5-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="c39e5-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="c39e5-121">指定要排除于設定中的偵測類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="c39e5-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="c39e5-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c39e5-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c39e5-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="c39e5-123">Sql_Injection</span></span> 
- <span data-ttu-id="c39e5-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="c39e5-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="c39e5-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="c39e5-125">Access_Anomaly</span></span> 
- <span data-ttu-id="c39e5-126">沒有</span><span class="sxs-lookup"><span data-stu-id="c39e5-126">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39e5-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="c39e5-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="c39e5-128">指定設定會傳送通知之電子郵件地址的分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="c39e5-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39e5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c39e5-129">-PassThru</span></span>
<span data-ttu-id="c39e5-130">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c39e5-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c39e5-131">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c39e5-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c39e5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39e5-132">-ResourceGroupName</span></span>
<span data-ttu-id="c39e5-133">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c39e5-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c39e5-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c39e5-134">-RetentionInDays</span></span>
<span data-ttu-id="c39e5-135">稽核記錄保留天數</span><span class="sxs-lookup"><span data-stu-id="c39e5-135">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39e5-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c39e5-136">-ServerName</span></span>
<span data-ttu-id="c39e5-137">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c39e5-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c39e5-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c39e5-138">-StorageAccountName</span></span>
<span data-ttu-id="c39e5-139">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c39e5-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="c39e5-140">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c39e5-140">Wildcards are not permitted.</span></span> <span data-ttu-id="c39e5-141">此參數不為必填專案。</span><span class="sxs-lookup"><span data-stu-id="c39e5-141">This parameter is not required.</span></span> <span data-ttu-id="c39e5-142">未提供此參數時，Cmdlet 會使用先前定義為資料庫進一步威脅防護設定一部分的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c39e5-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="c39e5-143">如果這是第一次定義資料庫進位威脅防護設定，而且未提供此參數，Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c39e5-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39e5-144">-確認</span><span class="sxs-lookup"><span data-stu-id="c39e5-144">-Confirm</span></span>
<span data-ttu-id="c39e5-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c39e5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39e5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39e5-146">-WhatIf</span></span>
<span data-ttu-id="c39e5-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c39e5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39e5-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c39e5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39e5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39e5-149">CommonParameters</span></span>
<span data-ttu-id="c39e5-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c39e5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39e5-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c39e5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39e5-152">輸入</span><span class="sxs-lookup"><span data-stu-id="c39e5-152">INPUTS</span></span>

### <span data-ttu-id="c39e5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c39e5-153">System.String</span></span>

### <span data-ttu-id="c39e5-154">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c39e5-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c39e5-155">Microsoft.Azure.Commands.sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="c39e5-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="c39e5-156">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c39e5-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c39e5-157">輸出</span><span class="sxs-lookup"><span data-stu-id="c39e5-157">OUTPUTS</span></span>

### <span data-ttu-id="c39e5-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="c39e5-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="c39e5-159">筆記</span><span class="sxs-lookup"><span data-stu-id="c39e5-159">NOTES</span></span>

## <span data-ttu-id="c39e5-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="c39e5-160">RELATED LINKS</span></span>

[<span data-ttu-id="c39e5-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="c39e5-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="c39e5-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="c39e5-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="c39e5-163">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c39e5-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


