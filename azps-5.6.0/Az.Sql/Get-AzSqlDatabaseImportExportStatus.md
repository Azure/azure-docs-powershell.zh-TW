---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 218af86b3cdc97ecbfccb07e54a57646ab5ff414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914378"
---
# <span data-ttu-id="ec627-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="ec627-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="ec627-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec627-102">SYNOPSIS</span></span>
<span data-ttu-id="ec627-103">獲得 Azure SQL Database 匯進或匯出的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ec627-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="ec627-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec627-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec627-105">描述</span><span class="sxs-lookup"><span data-stu-id="ec627-105">DESCRIPTION</span></span>
<span data-ttu-id="ec627-106">**Get-AzSqlDatabaseImportExportStatus** Cmdlet 會取得從儲存帳戶匯至 Azure SQL 資料庫的 bacpac 檔案匯出詳細資料，或將 Azure SQL Database 匯出為 bacpac 檔案至儲存帳戶的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ec627-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="ec627-107">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec627-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ec627-108">例子</span><span class="sxs-lookup"><span data-stu-id="ec627-108">EXAMPLES</span></span>

### <span data-ttu-id="ec627-109">範例 1：取得 SQL 資料庫的匯進和匯出狀態</span><span class="sxs-lookup"><span data-stu-id="ec627-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="ec627-110">此命令會以指定的 URL 為資料庫的匯進或匯出要求狀態。</span><span class="sxs-lookup"><span data-stu-id="ec627-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="ec627-111">參數</span><span class="sxs-lookup"><span data-stu-id="ec627-111">PARAMETERS</span></span>

### <span data-ttu-id="ec627-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec627-112">-DefaultProfile</span></span>
<span data-ttu-id="ec627-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ec627-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec627-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="ec627-114">-OperationStatusLink</span></span>
<span data-ttu-id="ec627-115">指定從 Cmdlet 或 Cmdlet New-AzSqlDatabaseExport的狀態New-AzSqlDatabaseImport連結。</span><span class="sxs-lookup"><span data-stu-id="ec627-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="ec627-116">-確認</span><span class="sxs-lookup"><span data-stu-id="ec627-116">-Confirm</span></span>
<span data-ttu-id="ec627-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ec627-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec627-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec627-118">-WhatIf</span></span>
<span data-ttu-id="ec627-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec627-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec627-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec627-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec627-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec627-121">CommonParameters</span></span>
<span data-ttu-id="ec627-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec627-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec627-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec627-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec627-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ec627-124">INPUTS</span></span>

### <span data-ttu-id="ec627-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ec627-125">System.String</span></span>

## <span data-ttu-id="ec627-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ec627-126">OUTPUTS</span></span>

### <span data-ttu-id="ec627-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="ec627-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="ec627-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ec627-128">NOTES</span></span>
* <span data-ttu-id="ec627-129">關鍵字：azure、azurerm、arm、resource、management、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="ec627-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="ec627-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec627-130">RELATED LINKS</span></span>

[<span data-ttu-id="ec627-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="ec627-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="ec627-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="ec627-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="ec627-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ec627-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
