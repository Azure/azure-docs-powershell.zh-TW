---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: ad5e5bb73b3611c3c56c7340f740947134f72d39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445451"
---
# <span data-ttu-id="7d46c-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="7d46c-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="7d46c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d46c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d46c-103">取得 Azure SQL 資料庫匯入或匯出的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7d46c-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d46c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d46c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d46c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d46c-105">DESCRIPTION</span></span>
<span data-ttu-id="7d46c-106">**AzureRmSqlDatabaseImportExportStatus** Cmdlet 會從儲存空間帳戶將 bacpac 檔案匯入到 Azure sql 資料庫，或是將 Azure SQL database 匯出為儲存空間帳戶的 bacpac 檔案。</span><span class="sxs-lookup"><span data-stu-id="7d46c-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="7d46c-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d46c-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7d46c-108">示例</span><span class="sxs-lookup"><span data-stu-id="7d46c-108">EXAMPLES</span></span>

### <span data-ttu-id="7d46c-109">範例1：取得 SQL 資料庫的匯入及匯出狀態</span><span class="sxs-lookup"><span data-stu-id="7d46c-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="7d46c-110">這個命令會在指定的 URL 取得資料庫的匯入或匯出要求狀態。</span><span class="sxs-lookup"><span data-stu-id="7d46c-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="7d46c-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d46c-111">PARAMETERS</span></span>

### <span data-ttu-id="7d46c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d46c-112">-DefaultProfile</span></span>
<span data-ttu-id="7d46c-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7d46c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d46c-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="7d46c-114">-OperationStatusLink</span></span>
<span data-ttu-id="7d46c-115">指定從 New-AzureRmSqlDatabaseExport 或 New-AzureRmSqlDatabaseImport Cmdlet 傳回的狀態連結。</span><span class="sxs-lookup"><span data-stu-id="7d46c-115">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="7d46c-116">-確認</span><span class="sxs-lookup"><span data-stu-id="7d46c-116">-Confirm</span></span>
<span data-ttu-id="7d46c-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d46c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d46c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d46c-118">-WhatIf</span></span>
<span data-ttu-id="7d46c-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d46c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d46c-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d46c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d46c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d46c-121">CommonParameters</span></span>
<span data-ttu-id="7d46c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d46c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d46c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d46c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d46c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7d46c-124">INPUTS</span></span>

### <span data-ttu-id="7d46c-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7d46c-125">System.String</span></span>

## <span data-ttu-id="7d46c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7d46c-126">OUTPUTS</span></span>

### <span data-ttu-id="7d46c-127">AzureSqlDatabaseImportExportStatusModel 中的 [ImportExport]</span><span class="sxs-lookup"><span data-stu-id="7d46c-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="7d46c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7d46c-128">NOTES</span></span>
* <span data-ttu-id="7d46c-129">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="7d46c-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="7d46c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d46c-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d46c-131">新-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="7d46c-131">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="7d46c-132">新-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="7d46c-132">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="7d46c-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="7d46c-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)