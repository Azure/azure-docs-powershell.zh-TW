---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: fe8a76ed0851393462ba94937d2ab92914b503b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625233"
---
# <span data-ttu-id="393fc-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="393fc-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="393fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="393fc-102">SYNOPSIS</span></span>
<span data-ttu-id="393fc-103">在資料庫上設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="393fc-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="393fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="393fc-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="393fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="393fc-105">DESCRIPTION</span></span>
<span data-ttu-id="393fc-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet 會在 Azure SQL 資料庫上設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="393fc-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="393fc-107">若要在資料庫上啟用威脅偵測，必須在該資料庫上啟用審核原則。</span><span class="sxs-lookup"><span data-stu-id="393fc-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="393fc-108">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 、 *ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="393fc-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="393fc-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="393fc-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="393fc-110">示例</span><span class="sxs-lookup"><span data-stu-id="393fc-110">EXAMPLES</span></span>

### <span data-ttu-id="393fc-111">範例1：為資料庫設定威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="393fc-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="393fc-112">這個命令會針對名為 Server01 的伺服器上名為 Database01 的資料庫設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="393fc-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="393fc-113">參數</span><span class="sxs-lookup"><span data-stu-id="393fc-113">PARAMETERS</span></span>

### <span data-ttu-id="393fc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="393fc-114">-DatabaseName</span></span>
<span data-ttu-id="393fc-115">指定設定策略之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="393fc-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="393fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393fc-116">-DefaultProfile</span></span>
<span data-ttu-id="393fc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="393fc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="393fc-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="393fc-118">-EmailAdmins</span></span>
<span data-ttu-id="393fc-119">指定威脅偵測原則是否使用電子郵件與管理員聯絡。</span><span class="sxs-lookup"><span data-stu-id="393fc-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="393fc-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="393fc-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="393fc-121">指定要從原則中排除的偵測類型陣列。</span><span class="sxs-lookup"><span data-stu-id="393fc-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="393fc-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="393fc-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="393fc-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="393fc-123">Sql_Injection</span></span> 
- <span data-ttu-id="393fc-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="393fc-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="393fc-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="393fc-125">Access_Anomaly</span></span> 
- <span data-ttu-id="393fc-126">所有</span><span class="sxs-lookup"><span data-stu-id="393fc-126">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393fc-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="393fc-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="393fc-128">指定原則要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="393fc-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="393fc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="393fc-129">-PassThru</span></span>
<span data-ttu-id="393fc-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="393fc-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="393fc-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="393fc-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="393fc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393fc-132">-ResourceGroupName</span></span>
<span data-ttu-id="393fc-133">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="393fc-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="393fc-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="393fc-134">-RetentionInDays</span></span>
<span data-ttu-id="393fc-135">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="393fc-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="393fc-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="393fc-136">-ServerName</span></span>
<span data-ttu-id="393fc-137">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="393fc-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="393fc-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="393fc-138">-StorageAccountName</span></span>
<span data-ttu-id="393fc-139">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="393fc-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="393fc-140">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="393fc-140">Wildcards are not permitted.</span></span> <span data-ttu-id="393fc-141">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="393fc-141">This parameter is not required.</span></span> <span data-ttu-id="393fc-142">如果未提供此參數，則 Cmdlet 會使用先前在資料庫的威脅偵測原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="393fc-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="393fc-143">如果這是已定義資料庫威脅偵測原則的第一次，且未提供此參數，則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="393fc-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="393fc-144">-確認</span><span class="sxs-lookup"><span data-stu-id="393fc-144">-Confirm</span></span>
<span data-ttu-id="393fc-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="393fc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="393fc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="393fc-146">-WhatIf</span></span>
<span data-ttu-id="393fc-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="393fc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="393fc-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="393fc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="393fc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393fc-149">CommonParameters</span></span>
<span data-ttu-id="393fc-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="393fc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393fc-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="393fc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393fc-152">輸入</span><span class="sxs-lookup"><span data-stu-id="393fc-152">INPUTS</span></span>

### <span data-ttu-id="393fc-153">System.object</span><span class="sxs-lookup"><span data-stu-id="393fc-153">System.String</span></span>

### <span data-ttu-id="393fc-154">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="393fc-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="393fc-155">DetectionType [] 的 ThreatDetection [）]</span><span class="sxs-lookup"><span data-stu-id="393fc-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="393fc-156">System.object "1 [[System. UInt32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="393fc-156">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="393fc-157">輸出</span><span class="sxs-lookup"><span data-stu-id="393fc-157">OUTPUTS</span></span>

### <span data-ttu-id="393fc-158">DatabaseThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="393fc-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="393fc-159">筆記</span><span class="sxs-lookup"><span data-stu-id="393fc-159">NOTES</span></span>

## <span data-ttu-id="393fc-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="393fc-160">RELATED LINKS</span></span>

[<span data-ttu-id="393fc-161">AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="393fc-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="393fc-162">移除-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="393fc-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="393fc-163">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="393fc-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


