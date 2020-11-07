---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 2bbbe4e2b553055e4643cff973941095e0a468f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792870"
---
# <span data-ttu-id="e6343-101">Update-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="e6343-101">Update-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="e6343-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6343-102">SYNOPSIS</span></span>
<span data-ttu-id="e6343-103">在資料庫上設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="e6343-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="e6343-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6343-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6343-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6343-105">DESCRIPTION</span></span>
<span data-ttu-id="e6343-106">**AzSqlDatabaseAdvancedThreatProtectionSettings** Cmdlet 會針對 Azure SQL 資料庫設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="e6343-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="e6343-107">若要在資料庫上啟用高級威脅防護，必須在該資料庫上啟用 [審核] 設定。</span><span class="sxs-lookup"><span data-stu-id="e6343-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="e6343-108">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 、 *ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="e6343-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e6343-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6343-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e6343-110">示例</span><span class="sxs-lookup"><span data-stu-id="e6343-110">EXAMPLES</span></span>

### <span data-ttu-id="e6343-111">範例1：為資料庫設定高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="e6343-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e6343-112">這個命令會在名為 Server01 的伺服器上，為名為 Database01 的資料庫設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="e6343-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="e6343-113">參數</span><span class="sxs-lookup"><span data-stu-id="e6343-113">PARAMETERS</span></span>

### <span data-ttu-id="e6343-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6343-114">-DatabaseName</span></span>
<span data-ttu-id="e6343-115">指定設定設定之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6343-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="e6343-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6343-116">-DefaultProfile</span></span>
<span data-ttu-id="e6343-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e6343-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6343-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e6343-118">-EmailAdmins</span></span>
<span data-ttu-id="e6343-119">指定 [高級威脅防護] 設定是否使用電子郵件與管理員聯絡。</span><span class="sxs-lookup"><span data-stu-id="e6343-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="e6343-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e6343-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="e6343-121">指定要從設定中排除的偵測類型陣列。</span><span class="sxs-lookup"><span data-stu-id="e6343-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="e6343-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e6343-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6343-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e6343-123">Sql_Injection</span></span> 
- <span data-ttu-id="e6343-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e6343-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="e6343-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e6343-125">Access_Anomaly</span></span> 
- <span data-ttu-id="e6343-126">所有</span><span class="sxs-lookup"><span data-stu-id="e6343-126">None</span></span>

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

### <span data-ttu-id="e6343-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e6343-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e6343-128">指定要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="e6343-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="e6343-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6343-129">-PassThru</span></span>
<span data-ttu-id="e6343-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e6343-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6343-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e6343-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6343-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6343-132">-ResourceGroupName</span></span>
<span data-ttu-id="e6343-133">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6343-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e6343-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e6343-134">-RetentionInDays</span></span>
<span data-ttu-id="e6343-135">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="e6343-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e6343-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6343-136">-ServerName</span></span>
<span data-ttu-id="e6343-137">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6343-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e6343-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e6343-138">-StorageAccountName</span></span>
<span data-ttu-id="e6343-139">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e6343-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e6343-140">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e6343-140">Wildcards are not permitted.</span></span> <span data-ttu-id="e6343-141">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="e6343-141">This parameter is not required.</span></span> <span data-ttu-id="e6343-142">如果未提供此參數，則此 Cmdlet 會使用先前在資料庫的高級威脅防護設定中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e6343-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="e6343-143">如果這是已定義資料庫高級威脅防護設定且未提供此參數的第一次，則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6343-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e6343-144">-確認</span><span class="sxs-lookup"><span data-stu-id="e6343-144">-Confirm</span></span>
<span data-ttu-id="e6343-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6343-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6343-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6343-146">-WhatIf</span></span>
<span data-ttu-id="e6343-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6343-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6343-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6343-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6343-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6343-149">CommonParameters</span></span>
<span data-ttu-id="e6343-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6343-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6343-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6343-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6343-152">輸入</span><span class="sxs-lookup"><span data-stu-id="e6343-152">INPUTS</span></span>

### <span data-ttu-id="e6343-153">System.object</span><span class="sxs-lookup"><span data-stu-id="e6343-153">System.String</span></span>

### <span data-ttu-id="e6343-154">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6343-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e6343-155">DetectionType [] 的 ThreatDetection [）]</span><span class="sxs-lookup"><span data-stu-id="e6343-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="e6343-156">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6343-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e6343-157">輸出</span><span class="sxs-lookup"><span data-stu-id="e6343-157">OUTPUTS</span></span>

### <span data-ttu-id="e6343-158">DatabaseThreatDetectionsettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="e6343-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="e6343-159">筆記</span><span class="sxs-lookup"><span data-stu-id="e6343-159">NOTES</span></span>

## <span data-ttu-id="e6343-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6343-160">RELATED LINKS</span></span>

[<span data-ttu-id="e6343-161">AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="e6343-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="e6343-162">移除-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="e6343-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="e6343-163">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e6343-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


