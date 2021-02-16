---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 079a1254865821b77ca48a94256dbe1a9e4cb431
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415320"
---
# <span data-ttu-id="8eb0e-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8eb0e-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8eb0e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8eb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb0e-103">設定伺服器上進位的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="8eb0e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8eb0e-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eb0e-105">描述</span><span class="sxs-lookup"><span data-stu-id="8eb0e-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb0e-106">**Update-AzSqlServerAdvancedThreatProtectionSetting** Cmdlet 在 Azure SQL 伺服器上設定進一步的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="8eb0e-107">若要在伺服器上啟用進位威脅防護，必須在伺服器上啟用稽核設定。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="8eb0e-108">若要使用此 Cmdlet，請指定 *ResourceGroupName* 和 ServerName 參數以識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="8eb0e-109">例子</span><span class="sxs-lookup"><span data-stu-id="8eb0e-109">EXAMPLES</span></span>

### <span data-ttu-id="8eb0e-110">範例 1：設定資料庫的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="8eb0e-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="8eb0e-111">此命令會設定伺服器名稱為 Server01 的進一威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="8eb0e-112">參數</span><span class="sxs-lookup"><span data-stu-id="8eb0e-112">PARAMETERS</span></span>

### <span data-ttu-id="8eb0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb0e-113">-DefaultProfile</span></span>
<span data-ttu-id="8eb0e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8eb0e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8eb0e-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="8eb0e-115">-EmailAdmins</span></span>
<span data-ttu-id="8eb0e-116">指定進一步威脅防護設定是否使用電子郵件與系統管理員聯繫。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="8eb0e-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="8eb0e-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="8eb0e-118">指定要排除于設定中的偵測類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="8eb0e-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8eb0e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8eb0e-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="8eb0e-120">Sql_Injection</span></span>
- <span data-ttu-id="8eb0e-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="8eb0e-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="8eb0e-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="8eb0e-122">Access_Anomaly</span></span>
- <span data-ttu-id="8eb0e-123">沒有</span><span class="sxs-lookup"><span data-stu-id="8eb0e-123">None</span></span>

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

### <span data-ttu-id="8eb0e-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="8eb0e-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="8eb0e-125">指定設定會傳送通知的電子郵件地址的分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="8eb0e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8eb0e-126">-PassThru</span></span>
<span data-ttu-id="8eb0e-127">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8eb0e-128">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8eb0e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb0e-129">-ResourceGroupName</span></span>
<span data-ttu-id="8eb0e-130">指定伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="8eb0e-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8eb0e-131">-RetentionInDays</span></span>
<span data-ttu-id="8eb0e-132">稽核記錄保留天數</span><span class="sxs-lookup"><span data-stu-id="8eb0e-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="8eb0e-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8eb0e-133">-ServerName</span></span>
<span data-ttu-id="8eb0e-134">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8eb0e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8eb0e-135">-StorageAccountName</span></span>
<span data-ttu-id="8eb0e-136">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="8eb0e-137">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-137">Wildcards are not permitted.</span></span> <span data-ttu-id="8eb0e-138">此參數不為必填專案。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-138">This parameter is not required.</span></span> <span data-ttu-id="8eb0e-139">未提供此參數時，Cmdlet 會使用先前定義為資料庫進一步威脅防護設定一部分的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="8eb0e-140">如果這是第一次定義資料庫威脅偵測設定，而且未提供此參數，Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="8eb0e-141">-確認</span><span class="sxs-lookup"><span data-stu-id="8eb0e-141">-Confirm</span></span>
<span data-ttu-id="8eb0e-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eb0e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb0e-143">-WhatIf</span></span>
<span data-ttu-id="8eb0e-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eb0e-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eb0e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb0e-146">CommonParameters</span></span>
<span data-ttu-id="8eb0e-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb0e-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8eb0e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb0e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="8eb0e-149">INPUTS</span></span>

### <span data-ttu-id="8eb0e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8eb0e-150">System.String</span></span>

### <span data-ttu-id="8eb0e-151">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8eb0e-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8eb0e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="8eb0e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="8eb0e-153">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8eb0e-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8eb0e-154">輸出</span><span class="sxs-lookup"><span data-stu-id="8eb0e-154">OUTPUTS</span></span>

### <span data-ttu-id="8eb0e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="8eb0e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="8eb0e-156">筆記</span><span class="sxs-lookup"><span data-stu-id="8eb0e-156">NOTES</span></span>

## <span data-ttu-id="8eb0e-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8eb0e-157">RELATED LINKS</span></span>

[<span data-ttu-id="8eb0e-158">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="8eb0e-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
