---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447912"
---
# <span data-ttu-id="177c9-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="177c9-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="177c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="177c9-102">SYNOPSIS</span></span>
<span data-ttu-id="177c9-103">在資料庫上設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="177c9-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="177c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="177c9-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="177c9-105">說明</span><span class="sxs-lookup"><span data-stu-id="177c9-105">DESCRIPTION</span></span>
<span data-ttu-id="177c9-106">**AzureRmSqlDatabaseThreatDetectionPolicy** Cmdlet 會在 Azure SQL 資料庫上設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="177c9-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="177c9-107">若要在資料庫上啟用威脅偵測，必須在該資料庫上啟用審核原則。</span><span class="sxs-lookup"><span data-stu-id="177c9-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="177c9-108">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 、 *ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="177c9-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="177c9-109">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="177c9-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="177c9-110">示例</span><span class="sxs-lookup"><span data-stu-id="177c9-110">EXAMPLES</span></span>

### <span data-ttu-id="177c9-111">範例1：為資料庫設定威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="177c9-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="177c9-112">這個命令會針對名為 Server01 的伺服器上名為 Database01 的資料庫設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="177c9-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="177c9-113">參數</span><span class="sxs-lookup"><span data-stu-id="177c9-113">PARAMETERS</span></span>

### <span data-ttu-id="177c9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="177c9-114">-DatabaseName</span></span>
<span data-ttu-id="177c9-115">指定設定策略之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="177c9-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="177c9-116">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="177c9-116">-EmailAdmins</span></span>
<span data-ttu-id="177c9-117">指定威脅偵測原則是否使用電子郵件與管理員聯絡。</span><span class="sxs-lookup"><span data-stu-id="177c9-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="177c9-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="177c9-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="177c9-119">指定要從原則中排除的偵測類型陣列。</span><span class="sxs-lookup"><span data-stu-id="177c9-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="177c9-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="177c9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="177c9-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="177c9-121">Sql_Injection</span></span> 
- <span data-ttu-id="177c9-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="177c9-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="177c9-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="177c9-123">Access_Anomaly</span></span> 
- <span data-ttu-id="177c9-124">所有</span><span class="sxs-lookup"><span data-stu-id="177c9-124">None</span></span>

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

### <span data-ttu-id="177c9-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="177c9-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="177c9-126">指定原則要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="177c9-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="177c9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="177c9-127">-PassThru</span></span>
<span data-ttu-id="177c9-128">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="177c9-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="177c9-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="177c9-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="177c9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177c9-130">-ResourceGroupName</span></span>
<span data-ttu-id="177c9-131">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="177c9-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="177c9-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="177c9-132">-RetentionInDays</span></span>
<span data-ttu-id="177c9-133">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="177c9-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="177c9-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="177c9-134">-ServerName</span></span>
<span data-ttu-id="177c9-135">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="177c9-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="177c9-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="177c9-136">-StorageAccountName</span></span>
<span data-ttu-id="177c9-137">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="177c9-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="177c9-138">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="177c9-138">Wildcards are not permitted.</span></span> <span data-ttu-id="177c9-139">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="177c9-139">This parameter is not required.</span></span> <span data-ttu-id="177c9-140">如果未提供此參數，則 Cmdlet 會使用先前在資料庫的威脅偵測原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="177c9-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="177c9-141">如果這是已定義資料庫威脅偵測原則的第一次，且未提供此參數，則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="177c9-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="177c9-142">-確認</span><span class="sxs-lookup"><span data-stu-id="177c9-142">-Confirm</span></span>
<span data-ttu-id="177c9-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="177c9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177c9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177c9-144">-WhatIf</span></span>
<span data-ttu-id="177c9-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="177c9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177c9-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="177c9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177c9-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177c9-147">-DefaultProfile</span></span>
<span data-ttu-id="177c9-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="177c9-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="177c9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177c9-149">CommonParameters</span></span>
<span data-ttu-id="177c9-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="177c9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177c9-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="177c9-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177c9-152">輸入</span><span class="sxs-lookup"><span data-stu-id="177c9-152">INPUTS</span></span>

###  
<span data-ttu-id="177c9-153">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="177c9-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="177c9-154">輸出</span><span class="sxs-lookup"><span data-stu-id="177c9-154">OUTPUTS</span></span>

### <span data-ttu-id="177c9-155">DatabaseThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="177c9-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="177c9-156">這個 Cmdlet 會傳回 **DatabaseThreatDetectionPolicyModel** 物件。</span><span class="sxs-lookup"><span data-stu-id="177c9-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="177c9-157">筆記</span><span class="sxs-lookup"><span data-stu-id="177c9-157">NOTES</span></span>

## <span data-ttu-id="177c9-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="177c9-158">RELATED LINKS</span></span>

[<span data-ttu-id="177c9-159">AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="177c9-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="177c9-160">移除-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="177c9-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="177c9-161">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="177c9-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


