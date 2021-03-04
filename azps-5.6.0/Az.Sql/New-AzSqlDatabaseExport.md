---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 198692c73609f6e3e88be0ccbe270c60bc679020
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908725"
---
# <span data-ttu-id="10e58-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="10e58-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="10e58-102">簡介</span><span class="sxs-lookup"><span data-stu-id="10e58-102">SYNOPSIS</span></span>
<span data-ttu-id="10e58-103">將 Azure SQL Database 匯出為 .bacpac 檔案至儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="10e58-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="10e58-104">語法</span><span class="sxs-lookup"><span data-stu-id="10e58-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10e58-105">描述</span><span class="sxs-lookup"><span data-stu-id="10e58-105">DESCRIPTION</span></span>
<span data-ttu-id="10e58-106">**New-AzSqlDatabaseExport** Cmdlet 將 Azure SQL Database 匯出為 .bacpac 檔案至儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="10e58-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="10e58-107">系統可能會送出取得匯出資料庫狀態要求，以取得此要求的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="10e58-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="10e58-108">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10e58-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10e58-109">若要使用此 Cmdlet，Azure SQL Server 上的防火牆必須被組成「允許 Azure 服務和資源存取此伺服器」。</span><span class="sxs-lookup"><span data-stu-id="10e58-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="10e58-110">如果未進行此配置，將會遇到 GatewayTimeout 錯誤。</span><span class="sxs-lookup"><span data-stu-id="10e58-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="10e58-111">例子</span><span class="sxs-lookup"><span data-stu-id="10e58-111">EXAMPLES</span></span>

### <span data-ttu-id="10e58-112">範例 1：建立資料庫的匯出要求</span><span class="sxs-lookup"><span data-stu-id="10e58-112">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="10e58-113">此命令會建立指定資料庫的匯出要求。</span><span class="sxs-lookup"><span data-stu-id="10e58-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="10e58-114">參數</span><span class="sxs-lookup"><span data-stu-id="10e58-114">PARAMETERS</span></span>

### <span data-ttu-id="10e58-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="10e58-115">-AdministratorLogin</span></span>
<span data-ttu-id="10e58-116">指定 SQL 系統管理員的名稱。</span><span class="sxs-lookup"><span data-stu-id="10e58-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="10e58-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="10e58-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="10e58-118">指定 SQL 系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="10e58-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="10e58-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="10e58-119">-AuthenticationType</span></span>
<span data-ttu-id="10e58-120">指定用來存取伺服器的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="10e58-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="10e58-121">如果未設定驗證類型，預設值為 SQL。</span><span class="sxs-lookup"><span data-stu-id="10e58-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="10e58-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="10e58-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10e58-123">Sql。</span><span class="sxs-lookup"><span data-stu-id="10e58-123">Sql.</span></span>
<span data-ttu-id="10e58-124">SQL 驗證。</span><span class="sxs-lookup"><span data-stu-id="10e58-124">SQL authentication.</span></span>
<span data-ttu-id="10e58-125">將 *AdministratorLogin 和* *AdministratorLoginPassword* 設定為 SQL 系統管理員使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="10e58-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="10e58-126">ADPassword。</span><span class="sxs-lookup"><span data-stu-id="10e58-126">ADPassword.</span></span>
<span data-ttu-id="10e58-127">Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="10e58-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="10e58-128">將 *AdministratorLogin 和* *AdministratorLoginPassword* 設定為 Azure AD 系統管理員使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="10e58-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="10e58-129">此參數僅適用于 SQL Database V12 伺服器。</span><span class="sxs-lookup"><span data-stu-id="10e58-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="10e58-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="10e58-130">-DatabaseName</span></span>
<span data-ttu-id="10e58-131">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="10e58-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="10e58-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e58-132">-DefaultProfile</span></span>
<span data-ttu-id="10e58-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="10e58-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10e58-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e58-134">-ResourceGroupName</span></span>
<span data-ttu-id="10e58-135">指定 SQL Database 伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="10e58-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="10e58-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10e58-136">-ServerName</span></span>
<span data-ttu-id="10e58-137">指定 SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="10e58-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="10e58-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="10e58-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="10e58-139">建立私人連結的 sql Server 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="10e58-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="10e58-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="10e58-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="10e58-141">儲存空間帳戶資源識別碼以建立私人連結</span><span class="sxs-lookup"><span data-stu-id="10e58-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="10e58-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="10e58-142">-StorageKey</span></span>
<span data-ttu-id="10e58-143">指定儲存空間帳戶的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="10e58-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="10e58-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="10e58-144">-StorageKeyType</span></span>
<span data-ttu-id="10e58-145">指定儲存空間帳戶的存取金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="10e58-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="10e58-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="10e58-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10e58-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="10e58-147">StorageAccessKey.</span></span>
<span data-ttu-id="10e58-148">此值使用儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="10e58-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="10e58-149">SharedAccessKey。</span><span class="sxs-lookup"><span data-stu-id="10e58-149">SharedAccessKey.</span></span>
<span data-ttu-id="10e58-150">此值使用共用存取簽章 (SAS) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="10e58-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="10e58-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="10e58-151">-StorageUri</span></span>
<span data-ttu-id="10e58-152">指定 .bacpac 檔案的 Blob 連結做為 URL。</span><span class="sxs-lookup"><span data-stu-id="10e58-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="10e58-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="10e58-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="10e58-154">如果設定好，將會為儲存空間帳戶和/或 SQL 伺服器建立私人連結</span><span class="sxs-lookup"><span data-stu-id="10e58-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="10e58-155">-確認</span><span class="sxs-lookup"><span data-stu-id="10e58-155">-Confirm</span></span>
<span data-ttu-id="10e58-156">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="10e58-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e58-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e58-157">-WhatIf</span></span>
<span data-ttu-id="10e58-158">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10e58-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e58-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10e58-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e58-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e58-160">CommonParameters</span></span>
<span data-ttu-id="10e58-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="10e58-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e58-162">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10e58-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e58-163">輸入</span><span class="sxs-lookup"><span data-stu-id="10e58-163">INPUTS</span></span>

### <span data-ttu-id="10e58-164">System.String</span><span class="sxs-lookup"><span data-stu-id="10e58-164">System.String</span></span>

## <span data-ttu-id="10e58-165">輸出</span><span class="sxs-lookup"><span data-stu-id="10e58-165">OUTPUTS</span></span>

### <span data-ttu-id="10e58-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="10e58-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="10e58-167">筆記</span><span class="sxs-lookup"><span data-stu-id="10e58-167">NOTES</span></span>
* <span data-ttu-id="10e58-168">關鍵字：azure、azurerm、arm、resource、management、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="10e58-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="10e58-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="10e58-169">RELATED LINKS</span></span>

[<span data-ttu-id="10e58-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="10e58-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="10e58-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="10e58-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="10e58-172">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="10e58-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
