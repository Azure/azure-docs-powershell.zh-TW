---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: a571621f7129b5d402521462f3d8273f55d9303d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614840"
---
# <span data-ttu-id="66da5-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="66da5-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="66da5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66da5-102">SYNOPSIS</span></span>
<span data-ttu-id="66da5-103">匯入 bacpac 檔案，然後在伺服器上建立新資料庫。</span><span class="sxs-lookup"><span data-stu-id="66da5-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="66da5-104">句法</span><span class="sxs-lookup"><span data-stu-id="66da5-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66da5-105">說明</span><span class="sxs-lookup"><span data-stu-id="66da5-105">DESCRIPTION</span></span>
<span data-ttu-id="66da5-106">**新的-AzSqlDatabaseImport** Cmdlet 會從 Azure 儲存空間帳戶將 bacpac 檔案匯入到新的 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="66da5-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="66da5-107">可能會傳送 [取得匯入資料庫狀態] 要求，以取得此要求的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="66da5-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="66da5-108">示例</span><span class="sxs-lookup"><span data-stu-id="66da5-108">EXAMPLES</span></span>

### <span data-ttu-id="66da5-109">範例1：建立 bacpac 檔案的匯入要求</span><span class="sxs-lookup"><span data-stu-id="66da5-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="66da5-110">這個命令會建立匯入要求，以便將 bacpac 匯入到新資料庫。</span><span class="sxs-lookup"><span data-stu-id="66da5-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="66da5-111">參數</span><span class="sxs-lookup"><span data-stu-id="66da5-111">PARAMETERS</span></span>

### <span data-ttu-id="66da5-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="66da5-112">-AdministratorLogin</span></span>
<span data-ttu-id="66da5-113">指定 SQL 系統管理員的名稱。</span><span class="sxs-lookup"><span data-stu-id="66da5-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="66da5-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="66da5-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="66da5-115">指定 SQL 系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="66da5-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66da5-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="66da5-116">-AuthenticationType</span></span>
<span data-ttu-id="66da5-117">指定用來存取伺服器的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="66da5-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="66da5-118">如果未設定驗證類型，此參數預設為 SQL。</span><span class="sxs-lookup"><span data-stu-id="66da5-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="66da5-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="66da5-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66da5-120">語句.</span><span class="sxs-lookup"><span data-stu-id="66da5-120">SQL.</span></span>
<span data-ttu-id="66da5-121">SQL 驗證。</span><span class="sxs-lookup"><span data-stu-id="66da5-121">SQL authentication.</span></span>
<span data-ttu-id="66da5-122">將 *AdministratorLogin* 和 *AdministratorLoginPassword* 參數設定為 SQL 系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="66da5-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="66da5-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="66da5-123">ADPassword.</span></span>
<span data-ttu-id="66da5-124">Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="66da5-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="66da5-125">將 *AdministratorLogin* 和 *AdministratorLoginPassword* 設定為 Azure Active Directory 系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="66da5-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="66da5-126">這個參數只適用于 SQL Database V12 伺服器。</span><span class="sxs-lookup"><span data-stu-id="66da5-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66da5-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="66da5-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="66da5-128">指定新匯入資料庫的大小上限。</span><span class="sxs-lookup"><span data-stu-id="66da5-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66da5-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66da5-129">-DatabaseName</span></span>
<span data-ttu-id="66da5-130">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="66da5-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="66da5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66da5-131">-DefaultProfile</span></span>
<span data-ttu-id="66da5-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="66da5-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66da5-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="66da5-133">-Edition</span></span>
<span data-ttu-id="66da5-134">指定要匯入的新資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="66da5-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="66da5-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="66da5-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66da5-136">佳</span><span class="sxs-lookup"><span data-stu-id="66da5-136">Premium</span></span>
- <span data-ttu-id="66da5-137">空白</span><span class="sxs-lookup"><span data-stu-id="66da5-137">Basic</span></span>
- <span data-ttu-id="66da5-138">標準</span><span class="sxs-lookup"><span data-stu-id="66da5-138">Standard</span></span>
- <span data-ttu-id="66da5-139">倉庫</span><span class="sxs-lookup"><span data-stu-id="66da5-139">DataWarehouse</span></span>
- <span data-ttu-id="66da5-140">空閒</span><span class="sxs-lookup"><span data-stu-id="66da5-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66da5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66da5-141">-ResourceGroupName</span></span>
<span data-ttu-id="66da5-142">指定 SQL 資料庫伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66da5-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="66da5-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66da5-143">-ServerName</span></span>
<span data-ttu-id="66da5-144">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="66da5-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="66da5-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="66da5-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="66da5-146">指定要指派給 Azure SQL 資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="66da5-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="66da5-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="66da5-147">-StorageKey</span></span>
<span data-ttu-id="66da5-148">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="66da5-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="66da5-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="66da5-149">-StorageKeyType</span></span>
<span data-ttu-id="66da5-150">指定儲存空間帳戶的便捷鍵類型。</span><span class="sxs-lookup"><span data-stu-id="66da5-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="66da5-151">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="66da5-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="66da5-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="66da5-152">StorageAccessKey.</span></span>
<span data-ttu-id="66da5-153">使用儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="66da5-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="66da5-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="66da5-154">SharedAccessKey.</span></span>
<span data-ttu-id="66da5-155">使用共用存取簽名 (SAS) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="66da5-155">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66da5-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="66da5-156">-StorageUri</span></span>
<span data-ttu-id="66da5-157">指定 bacpac 檔案的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="66da5-157">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66da5-158">-確認</span><span class="sxs-lookup"><span data-stu-id="66da5-158">-Confirm</span></span>
<span data-ttu-id="66da5-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66da5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66da5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66da5-160">-WhatIf</span></span>
<span data-ttu-id="66da5-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66da5-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66da5-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66da5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66da5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66da5-163">CommonParameters</span></span>
<span data-ttu-id="66da5-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66da5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66da5-165">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66da5-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66da5-166">輸入</span><span class="sxs-lookup"><span data-stu-id="66da5-166">INPUTS</span></span>

### <span data-ttu-id="66da5-167">System.object</span><span class="sxs-lookup"><span data-stu-id="66da5-167">System.String</span></span>

## <span data-ttu-id="66da5-168">輸出</span><span class="sxs-lookup"><span data-stu-id="66da5-168">OUTPUTS</span></span>

### <span data-ttu-id="66da5-169">AzureSqlDatabaseImportExportBaseModel 中的 [ImportExport]</span><span class="sxs-lookup"><span data-stu-id="66da5-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="66da5-170">筆記</span><span class="sxs-lookup"><span data-stu-id="66da5-170">NOTES</span></span>
* <span data-ttu-id="66da5-171">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="66da5-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="66da5-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="66da5-172">RELATED LINKS</span></span>

[<span data-ttu-id="66da5-173">AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="66da5-173">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="66da5-174">新-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="66da5-174">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="66da5-175">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="66da5-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

