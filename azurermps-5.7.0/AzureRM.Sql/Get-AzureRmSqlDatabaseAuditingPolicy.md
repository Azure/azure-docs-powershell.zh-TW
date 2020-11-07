---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 4d15400da4105f719f5948a53512f6c33cbd3bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624984"
---
# <span data-ttu-id="af2b1-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="af2b1-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="af2b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="af2b1-103">取得資料庫的審核原則。</span><span class="sxs-lookup"><span data-stu-id="af2b1-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af2b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="af2b1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af2b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="af2b1-105">DESCRIPTION</span></span>
<span data-ttu-id="af2b1-106">**AzureRmSqlDatabaseAuditingPolicy** Cmdlet 會取得 Azure SQL 資料庫的審核原則。</span><span class="sxs-lookup"><span data-stu-id="af2b1-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="af2b1-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="af2b1-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="af2b1-108">示例</span><span class="sxs-lookup"><span data-stu-id="af2b1-108">EXAMPLES</span></span>

### <span data-ttu-id="af2b1-109">範例1：取得 Azure SQL database 的審核原則，並在其上定義 [資料表審核]</span><span class="sxs-lookup"><span data-stu-id="af2b1-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="af2b1-110">範例2：取得 Azure SQL database 的審核原則，並在其上定義 Blob 審核</span><span class="sxs-lookup"><span data-stu-id="af2b1-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="af2b1-111">參數</span><span class="sxs-lookup"><span data-stu-id="af2b1-111">PARAMETERS</span></span>

### <span data-ttu-id="af2b1-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af2b1-112">-DatabaseName</span></span>
<span data-ttu-id="af2b1-113">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="af2b1-113">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2b1-114">-DefaultProfile</span></span>
<span data-ttu-id="af2b1-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="af2b1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2b1-116">-ResourceGroupName</span></span>
<span data-ttu-id="af2b1-117">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af2b1-117">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af2b1-118">-ServerName</span></span>
<span data-ttu-id="af2b1-119">指定資料庫所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="af2b1-119">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-120">-確認</span><span class="sxs-lookup"><span data-stu-id="af2b1-120">-Confirm</span></span>
<span data-ttu-id="af2b1-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af2b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2b1-122">-WhatIf</span></span>
<span data-ttu-id="af2b1-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af2b1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2b1-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af2b1-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2b1-125">CommonParameters</span></span>
<span data-ttu-id="af2b1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af2b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2b1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af2b1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2b1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="af2b1-128">INPUTS</span></span>

### <span data-ttu-id="af2b1-129">所有</span><span class="sxs-lookup"><span data-stu-id="af2b1-129">None</span></span>
<span data-ttu-id="af2b1-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="af2b1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af2b1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="af2b1-131">OUTPUTS</span></span>

### <span data-ttu-id="af2b1-132">DatabaseAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="af2b1-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="af2b1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="af2b1-133">NOTES</span></span>

## <span data-ttu-id="af2b1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="af2b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="af2b1-135">移除-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="af2b1-135">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="af2b1-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="af2b1-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



