---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448830"
---
# <span data-ttu-id="ae729-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="ae729-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="ae729-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae729-102">SYNOPSIS</span></span>
<span data-ttu-id="ae729-103">匯入 bacpac 檔案，然後在伺服器上建立新資料庫。</span><span class="sxs-lookup"><span data-stu-id="ae729-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae729-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae729-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae729-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae729-105">DESCRIPTION</span></span>
<span data-ttu-id="ae729-106">**新的-AzureRmSqlDatabaseImport** Cmdlet 會從 Azure 儲存空間帳戶將 bacpac 檔案匯入到新的 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ae729-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="ae729-107">可能會傳送 [取得匯入資料庫狀態] 要求，以取得此要求的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="ae729-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="ae729-108">示例</span><span class="sxs-lookup"><span data-stu-id="ae729-108">EXAMPLES</span></span>

### <span data-ttu-id="ae729-109">範例1：建立 bacpac 檔案的匯入要求</span><span class="sxs-lookup"><span data-stu-id="ae729-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
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

<span data-ttu-id="ae729-110">這個命令會建立匯入要求，以便將 bacpac 匯入到新資料庫。</span><span class="sxs-lookup"><span data-stu-id="ae729-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="ae729-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae729-111">PARAMETERS</span></span>

### <span data-ttu-id="ae729-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="ae729-112">-AdministratorLogin</span></span>
<span data-ttu-id="ae729-113">指定 SQL 系統管理員的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae729-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="ae729-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ae729-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ae729-115">指定 SQL 系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="ae729-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="ae729-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="ae729-116">-AuthenticationType</span></span>
<span data-ttu-id="ae729-117">指定用來存取伺服器的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="ae729-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="ae729-118">如果未設定驗證類型，此參數預設為 SQL。</span><span class="sxs-lookup"><span data-stu-id="ae729-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="ae729-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ae729-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae729-120">語句.</span><span class="sxs-lookup"><span data-stu-id="ae729-120">SQL.</span></span>
<span data-ttu-id="ae729-121">SQL 驗證。</span><span class="sxs-lookup"><span data-stu-id="ae729-121">SQL authentication.</span></span>
<span data-ttu-id="ae729-122">將 *AdministratorLogin* 和 *AdministratorLoginPassword* 參數設定為 SQL 系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ae729-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="ae729-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="ae729-123">ADPassword.</span></span>
<span data-ttu-id="ae729-124">Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ae729-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="ae729-125">將 *AdministratorLogin* 和 *AdministratorLoginPassword* 設定為 Azure Active Directory 系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ae729-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="ae729-126">這個參數只適用于 SQL Database V12 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae729-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="ae729-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ae729-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="ae729-128">指定新匯入資料庫的大小上限。</span><span class="sxs-lookup"><span data-stu-id="ae729-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="ae729-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae729-129">-DatabaseName</span></span>
<span data-ttu-id="ae729-130">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae729-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="ae729-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="ae729-131">-Edition</span></span>
<span data-ttu-id="ae729-132">指定要匯入的新資料庫版本。</span><span class="sxs-lookup"><span data-stu-id="ae729-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="ae729-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ae729-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae729-134">佳</span><span class="sxs-lookup"><span data-stu-id="ae729-134">Premium</span></span>
- <span data-ttu-id="ae729-135">空白</span><span class="sxs-lookup"><span data-stu-id="ae729-135">Basic</span></span>
- <span data-ttu-id="ae729-136">標準</span><span class="sxs-lookup"><span data-stu-id="ae729-136">Standard</span></span>
- <span data-ttu-id="ae729-137">倉庫</span><span class="sxs-lookup"><span data-stu-id="ae729-137">DataWarehouse</span></span>
- <span data-ttu-id="ae729-138">空閒</span><span class="sxs-lookup"><span data-stu-id="ae729-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae729-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae729-139">-ResourceGroupName</span></span>
<span data-ttu-id="ae729-140">指定 SQL 資料庫伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae729-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="ae729-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ae729-141">-ServerName</span></span>
<span data-ttu-id="ae729-142">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae729-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="ae729-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ae729-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="ae729-144">指定要指派給 Azure SQL 資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae729-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ae729-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ae729-145">-StorageKey</span></span>
<span data-ttu-id="ae729-146">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ae729-146">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="ae729-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ae729-147">-StorageKeyType</span></span>
<span data-ttu-id="ae729-148">指定儲存空間帳戶的便捷鍵類型。</span><span class="sxs-lookup"><span data-stu-id="ae729-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="ae729-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ae729-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae729-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="ae729-150">StorageAccessKey.</span></span>
<span data-ttu-id="ae729-151">使用儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="ae729-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="ae729-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="ae729-152">SharedAccessKey.</span></span>
<span data-ttu-id="ae729-153">使用共用存取簽名 (SAS) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="ae729-153">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="ae729-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="ae729-154">-StorageUri</span></span>
<span data-ttu-id="ae729-155">指定 bacpac 檔案的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="ae729-155">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="ae729-156">-確認</span><span class="sxs-lookup"><span data-stu-id="ae729-156">-Confirm</span></span>
<span data-ttu-id="ae729-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae729-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae729-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae729-158">-WhatIf</span></span>
<span data-ttu-id="ae729-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae729-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae729-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae729-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae729-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae729-161">-DefaultProfile</span></span>
<span data-ttu-id="ae729-162">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae729-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae729-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae729-163">CommonParameters</span></span>
<span data-ttu-id="ae729-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae729-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae729-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae729-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae729-166">輸入</span><span class="sxs-lookup"><span data-stu-id="ae729-166">INPUTS</span></span>

## <span data-ttu-id="ae729-167">輸出</span><span class="sxs-lookup"><span data-stu-id="ae729-167">OUTPUTS</span></span>

### <span data-ttu-id="ae729-168">AzureSqlDatabaseImportExportBaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="ae729-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="ae729-169">筆記</span><span class="sxs-lookup"><span data-stu-id="ae729-169">NOTES</span></span>
* <span data-ttu-id="ae729-170">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="ae729-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="ae729-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae729-171">RELATED LINKS</span></span>

[<span data-ttu-id="ae729-172">AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="ae729-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="ae729-173">新-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="ae729-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="ae729-174">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ae729-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

