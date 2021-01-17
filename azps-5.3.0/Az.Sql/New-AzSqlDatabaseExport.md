---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 737b7170b774be712fb316f5c76b95d326e22fdb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436162"
---
# <span data-ttu-id="9bf2e-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="9bf2e-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="9bf2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9bf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf2e-103">將 Azure SQL 資料庫作為 bacpac 檔案匯出至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="9bf2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9bf2e-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9bf2e-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf2e-106">**新的-AzSqlDatabaseExport** Cmdlet 會將 Azure SQL 資料庫匯出為儲存空間帳戶的 bacpac 檔案。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="9bf2e-107">可能會傳送取得匯出資料庫狀態要求，以取得此要求的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="9bf2e-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9bf2e-109">若要使用這個 Cmdlet，Azure SQL Server 上的防火牆將需要設定為「允許 Azure 服務和資源存取此伺服器」。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="9bf2e-110">如果未設定此選項，則會遇到 GatewayTimeout 錯誤。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="9bf2e-111">示例</span><span class="sxs-lookup"><span data-stu-id="9bf2e-111">EXAMPLES</span></span>

### <span data-ttu-id="9bf2e-112">範例1：建立資料庫的匯出要求</span><span class="sxs-lookup"><span data-stu-id="9bf2e-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="9bf2e-113">這個命令會為指定的資料庫建立匯出要求。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="9bf2e-114">參數</span><span class="sxs-lookup"><span data-stu-id="9bf2e-114">PARAMETERS</span></span>

### <span data-ttu-id="9bf2e-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="9bf2e-115">-AdministratorLogin</span></span>
<span data-ttu-id="9bf2e-116">指定 SQL 系統管理員的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="9bf2e-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="9bf2e-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="9bf2e-118">指定 SQL 系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="9bf2e-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="9bf2e-119">-AuthenticationType</span></span>
<span data-ttu-id="9bf2e-120">指定用來存取伺服器的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="9bf2e-121">如果未設定驗證類型，則預設值為 SQL。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="9bf2e-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9bf2e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9bf2e-123">語句.</span><span class="sxs-lookup"><span data-stu-id="9bf2e-123">Sql.</span></span>
<span data-ttu-id="9bf2e-124">SQL 驗證。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-124">SQL authentication.</span></span>
<span data-ttu-id="9bf2e-125">將 *AdministratorLogin* 和 *ADMINISTRATORLOGINPASSWORD* 設定為 SQL 系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="9bf2e-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="9bf2e-126">ADPassword.</span></span>
<span data-ttu-id="9bf2e-127">Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="9bf2e-128">將 *AdministratorLogin* 和 *AdministratorLoginPassword* 設定為 Azure AD 管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="9bf2e-129">這個參數只適用于 SQL Database V12 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="9bf2e-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bf2e-130">-DatabaseName</span></span>
<span data-ttu-id="9bf2e-131">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="9bf2e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf2e-132">-DefaultProfile</span></span>
<span data-ttu-id="9bf2e-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9bf2e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bf2e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf2e-134">-ResourceGroupName</span></span>
<span data-ttu-id="9bf2e-135">指定 SQL 資料庫伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="9bf2e-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9bf2e-136">-ServerName</span></span>
<span data-ttu-id="9bf2e-137">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="9bf2e-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="9bf2e-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="9bf2e-139">要建立私人連結的 sql server 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9bf2e-139">The sql server resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf2e-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="9bf2e-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="9bf2e-141">要建立私人連結的儲存空間帳戶資源 id</span><span class="sxs-lookup"><span data-stu-id="9bf2e-141">The storage account resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf2e-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="9bf2e-142">-StorageKey</span></span>
<span data-ttu-id="9bf2e-143">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="9bf2e-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="9bf2e-144">-StorageKeyType</span></span>
<span data-ttu-id="9bf2e-145">指定儲存空間帳戶的便捷鍵類型。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="9bf2e-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9bf2e-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9bf2e-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="9bf2e-147">StorageAccessKey.</span></span>
<span data-ttu-id="9bf2e-148">此值會使用儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="9bf2e-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="9bf2e-149">SharedAccessKey.</span></span>
<span data-ttu-id="9bf2e-150">此值會使用共用存取簽名 (SAS) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="9bf2e-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="9bf2e-151">-StorageUri</span></span>
<span data-ttu-id="9bf2e-152">指定指向 bacpac 檔案的 blob 連結（作為 URL）。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="9bf2e-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="9bf2e-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="9bf2e-154">如果設定，將會建立儲存空間帳戶和/或 SQL server 的私人連結</span><span class="sxs-lookup"><span data-stu-id="9bf2e-154">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bf2e-155">-確認</span><span class="sxs-lookup"><span data-stu-id="9bf2e-155">-Confirm</span></span>
<span data-ttu-id="9bf2e-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf2e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf2e-157">-WhatIf</span></span>
<span data-ttu-id="9bf2e-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf2e-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf2e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf2e-160">CommonParameters</span></span>
<span data-ttu-id="9bf2e-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf2e-162">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9bf2e-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf2e-163">輸入</span><span class="sxs-lookup"><span data-stu-id="9bf2e-163">INPUTS</span></span>

### <span data-ttu-id="9bf2e-164">System.object</span><span class="sxs-lookup"><span data-stu-id="9bf2e-164">System.String</span></span>

## <span data-ttu-id="9bf2e-165">輸出</span><span class="sxs-lookup"><span data-stu-id="9bf2e-165">OUTPUTS</span></span>

### <span data-ttu-id="9bf2e-166">AzureSqlDatabaseImportExportBaseModel 中的 [ImportExport]</span><span class="sxs-lookup"><span data-stu-id="9bf2e-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="9bf2e-167">筆記</span><span class="sxs-lookup"><span data-stu-id="9bf2e-167">NOTES</span></span>
* <span data-ttu-id="9bf2e-168">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="9bf2e-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="9bf2e-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bf2e-169">RELATED LINKS</span></span>

[<span data-ttu-id="9bf2e-170">AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="9bf2e-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="9bf2e-171">新-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="9bf2e-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="9bf2e-172">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="9bf2e-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
