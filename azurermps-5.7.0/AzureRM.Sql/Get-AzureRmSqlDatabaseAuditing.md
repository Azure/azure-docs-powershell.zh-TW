---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 9058863da0af6addd243f5e7ec544a8dad7b3b03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444292"
---
# <span data-ttu-id="5fd34-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="5fd34-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="5fd34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5fd34-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd34-103">取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5fd34-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fd34-104">句法</span><span class="sxs-lookup"><span data-stu-id="5fd34-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd34-105">說明</span><span class="sxs-lookup"><span data-stu-id="5fd34-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd34-106">**AzureRmSqlDatabaseAuditing** Cmdlet 會取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5fd34-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="5fd34-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="5fd34-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="5fd34-108">示例</span><span class="sxs-lookup"><span data-stu-id="5fd34-108">EXAMPLES</span></span>

### <span data-ttu-id="5fd34-109">範例1：取得 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="5fd34-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="5fd34-110">參數</span><span class="sxs-lookup"><span data-stu-id="5fd34-110">PARAMETERS</span></span>

### <span data-ttu-id="5fd34-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5fd34-111">-DatabaseName</span></span>
<span data-ttu-id="5fd34-112">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd34-112">SQL Database name.</span></span>

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

### <span data-ttu-id="5fd34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd34-113">-DefaultProfile</span></span>
<span data-ttu-id="5fd34-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5fd34-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fd34-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd34-115">-ResourceGroupName</span></span>
<span data-ttu-id="5fd34-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd34-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5fd34-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5fd34-117">-ServerName</span></span>
<span data-ttu-id="5fd34-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5fd34-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="5fd34-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5fd34-119">-Confirm</span></span>
<span data-ttu-id="5fd34-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5fd34-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd34-121">-WhatIf</span></span>
<span data-ttu-id="5fd34-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5fd34-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fd34-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5fd34-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd34-124">CommonParameters</span></span>
<span data-ttu-id="5fd34-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5fd34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd34-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5fd34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd34-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5fd34-127">INPUTS</span></span>

### <span data-ttu-id="5fd34-128">所有</span><span class="sxs-lookup"><span data-stu-id="5fd34-128">None</span></span>
<span data-ttu-id="5fd34-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5fd34-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fd34-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5fd34-130">OUTPUTS</span></span>

### <span data-ttu-id="5fd34-131">DatabaseBlobAuditingSettingsModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="5fd34-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="5fd34-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5fd34-132">NOTES</span></span>

## <span data-ttu-id="5fd34-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fd34-133">RELATED LINKS</span></span>
