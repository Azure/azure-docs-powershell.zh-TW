---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798097"
---
# <span data-ttu-id="52338-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="52338-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="52338-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52338-102">SYNOPSIS</span></span>
<span data-ttu-id="52338-103">在伺服器上設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="52338-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="52338-104">句法</span><span class="sxs-lookup"><span data-stu-id="52338-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52338-105">說明</span><span class="sxs-lookup"><span data-stu-id="52338-105">DESCRIPTION</span></span>
<span data-ttu-id="52338-106">**AzSqlServerAdvancedThreatProtectionSetting** Cmdlet 會在 Azure SQL server 上設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="52338-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="52338-107">若要在伺服器上啟用高級威脅防護，必須在該伺服器上啟用 [審核] 設定。</span><span class="sxs-lookup"><span data-stu-id="52338-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="52338-108">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 ServerName 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="52338-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="52338-109">示例</span><span class="sxs-lookup"><span data-stu-id="52338-109">EXAMPLES</span></span>

### <span data-ttu-id="52338-110">範例1：為資料庫設定高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="52338-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="52338-111">這個命令會為名為 Server01 的伺服器設定高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="52338-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="52338-112">參數</span><span class="sxs-lookup"><span data-stu-id="52338-112">PARAMETERS</span></span>

### <span data-ttu-id="52338-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52338-113">-DefaultProfile</span></span>
<span data-ttu-id="52338-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="52338-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52338-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="52338-115">-EmailAdmins</span></span>
<span data-ttu-id="52338-116">指定 [高級威脅防護] 設定是否使用電子郵件與管理員聯絡。</span><span class="sxs-lookup"><span data-stu-id="52338-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="52338-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="52338-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="52338-118">指定要從設定中排除的偵測類型陣列。</span><span class="sxs-lookup"><span data-stu-id="52338-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="52338-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="52338-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52338-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="52338-120">Sql_Injection</span></span>
- <span data-ttu-id="52338-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="52338-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="52338-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="52338-122">Access_Anomaly</span></span>
- <span data-ttu-id="52338-123">所有</span><span class="sxs-lookup"><span data-stu-id="52338-123">None</span></span>

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

### <span data-ttu-id="52338-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="52338-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="52338-125">指定要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="52338-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="52338-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52338-126">-PassThru</span></span>
<span data-ttu-id="52338-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="52338-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52338-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="52338-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52338-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52338-129">-ResourceGroupName</span></span>
<span data-ttu-id="52338-130">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52338-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="52338-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="52338-131">-RetentionInDays</span></span>
<span data-ttu-id="52338-132">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="52338-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="52338-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52338-133">-ServerName</span></span>
<span data-ttu-id="52338-134">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="52338-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="52338-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="52338-135">-StorageAccountName</span></span>
<span data-ttu-id="52338-136">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="52338-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="52338-137">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="52338-137">Wildcards are not permitted.</span></span> <span data-ttu-id="52338-138">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="52338-138">This parameter is not required.</span></span> <span data-ttu-id="52338-139">如果未提供此參數，則此 Cmdlet 會使用先前在資料庫的高級威脅防護設定中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="52338-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="52338-140">如果這是已定義資料庫威脅偵測設定，且未提供此參數，則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="52338-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="52338-141">-確認</span><span class="sxs-lookup"><span data-stu-id="52338-141">-Confirm</span></span>
<span data-ttu-id="52338-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52338-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52338-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52338-143">-WhatIf</span></span>
<span data-ttu-id="52338-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52338-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52338-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52338-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52338-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52338-146">CommonParameters</span></span>
<span data-ttu-id="52338-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52338-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52338-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="52338-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52338-149">輸入</span><span class="sxs-lookup"><span data-stu-id="52338-149">INPUTS</span></span>

### <span data-ttu-id="52338-150">System.object</span><span class="sxs-lookup"><span data-stu-id="52338-150">System.String</span></span>

### <span data-ttu-id="52338-151">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52338-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="52338-152">DetectionType [] 的 ThreatDetection [）]</span><span class="sxs-lookup"><span data-stu-id="52338-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="52338-153">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52338-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52338-154">輸出</span><span class="sxs-lookup"><span data-stu-id="52338-154">OUTPUTS</span></span>

### <span data-ttu-id="52338-155">ServerThreatDetectionsettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="52338-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="52338-156">筆記</span><span class="sxs-lookup"><span data-stu-id="52338-156">NOTES</span></span>

## <span data-ttu-id="52338-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="52338-157">RELATED LINKS</span></span>

[<span data-ttu-id="52338-158">AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="52338-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="52338-159">移除-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="52338-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="52338-160">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="52338-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
