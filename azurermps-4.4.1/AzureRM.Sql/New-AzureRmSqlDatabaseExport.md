---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: f7ede8432f8e833b3d309925daab591889836257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626200"
---
# <span data-ttu-id="d2d3a-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="d2d3a-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="d2d3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d3a-103">將 Azure SQL 資料庫作為 bacpac 檔案匯出至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2d3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2d3a-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="d2d3a-106">**新的-AzureRmSqlDatabaseExport** Cmdlet 會將 Azure SQL 資料庫匯出為儲存空間帳戶的 bacpac 檔案。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="d2d3a-107">可能會傳送取得匯出資料庫狀態要求，以取得此要求的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="d2d3a-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d2d3a-109">示例</span><span class="sxs-lookup"><span data-stu-id="d2d3a-109">EXAMPLES</span></span>

### <span data-ttu-id="d2d3a-110">範例1：建立資料庫的匯出要求</span><span class="sxs-lookup"><span data-stu-id="d2d3a-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="d2d3a-111">這個命令會為指定的資料庫建立匯出要求。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="d2d3a-112">參數</span><span class="sxs-lookup"><span data-stu-id="d2d3a-112">PARAMETERS</span></span>

### <span data-ttu-id="d2d3a-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="d2d3a-113">-AdministratorLogin</span></span>
<span data-ttu-id="d2d3a-114">指定 SQL 系統管理員的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="d2d3a-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d2d3a-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d2d3a-116">指定 SQL 系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="d2d3a-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d2d3a-117">-AuthenticationType</span></span>
<span data-ttu-id="d2d3a-118">指定用來存取伺服器的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="d2d3a-119">如果未設定驗證類型，則預設值為 SQL。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="d2d3a-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d2d3a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2d3a-121">語句.</span><span class="sxs-lookup"><span data-stu-id="d2d3a-121">Sql.</span></span>
<span data-ttu-id="d2d3a-122">SQL 驗證。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-122">SQL authentication.</span></span>
<span data-ttu-id="d2d3a-123">將 *AdministratorLogin* 和 *ADMINISTRATORLOGINPASSWORD* 設定為 SQL 系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="d2d3a-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="d2d3a-124">ADPassword.</span></span>
<span data-ttu-id="d2d3a-125">Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="d2d3a-126">將 *AdministratorLogin* 和 *AdministratorLoginPassword* 設定為 Azure AD 管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="d2d3a-127">這個參數只適用于 SQL Database V12 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="d2d3a-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2d3a-128">-DatabaseName</span></span>
<span data-ttu-id="d2d3a-129">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="d2d3a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d3a-130">-ResourceGroupName</span></span>
<span data-ttu-id="d2d3a-131">指定 SQL 資料庫伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-131">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="d2d3a-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2d3a-132">-ServerName</span></span>
<span data-ttu-id="d2d3a-133">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-133">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="d2d3a-134">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d2d3a-134">-StorageKey</span></span>
<span data-ttu-id="d2d3a-135">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-135">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="d2d3a-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d2d3a-136">-StorageKeyType</span></span>
<span data-ttu-id="d2d3a-137">指定儲存空間帳戶的便捷鍵類型。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-137">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="d2d3a-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d2d3a-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2d3a-139">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d2d3a-139">StorageAccessKey.</span></span>
<span data-ttu-id="d2d3a-140">此值會使用儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-140">This value uses a storage account key.</span></span> 
- <span data-ttu-id="d2d3a-141">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="d2d3a-141">SharedAccessKey.</span></span>
<span data-ttu-id="d2d3a-142">此值會使用共用存取簽名 (SAS) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-142">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="d2d3a-143">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d2d3a-143">-StorageUri</span></span>
<span data-ttu-id="d2d3a-144">指定指向 bacpac 檔案的 blob 連結（作為 URL）。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-144">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="d2d3a-145">-確認</span><span class="sxs-lookup"><span data-stu-id="d2d3a-145">-Confirm</span></span>
<span data-ttu-id="d2d3a-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d3a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d3a-147">-WhatIf</span></span>
<span data-ttu-id="d2d3a-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2d3a-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d3a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d3a-150">-DefaultProfile</span></span>
<span data-ttu-id="d2d3a-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2d3a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d3a-152">CommonParameters</span></span>
<span data-ttu-id="d2d3a-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d3a-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d3a-155">輸入</span><span class="sxs-lookup"><span data-stu-id="d2d3a-155">INPUTS</span></span>

## <span data-ttu-id="d2d3a-156">輸出</span><span class="sxs-lookup"><span data-stu-id="d2d3a-156">OUTPUTS</span></span>

### <span data-ttu-id="d2d3a-157">AzureSqlDatabaseImportExportBaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="d2d3a-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="d2d3a-158">筆記</span><span class="sxs-lookup"><span data-stu-id="d2d3a-158">NOTES</span></span>
* <span data-ttu-id="d2d3a-159">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="d2d3a-159">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d2d3a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2d3a-160">RELATED LINKS</span></span>

[<span data-ttu-id="d2d3a-161">AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="d2d3a-161">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="d2d3a-162">新-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="d2d3a-162">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="d2d3a-163">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d2d3a-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
