---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 4203609a97a9fc476292fca4020976539eb5d2b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456360"
---
# <span data-ttu-id="5bdd2-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="5bdd2-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="5bdd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bdd2-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdd2-103">取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bdd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bdd2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="5bdd2-105">DESCRIPTION</span></span>
<span data-ttu-id="5bdd2-106">**AzureRmSqlDatabaseAuditing** Cmdlet 會取得 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="5bdd2-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="5bdd2-108">示例</span><span class="sxs-lookup"><span data-stu-id="5bdd2-108">EXAMPLES</span></span>

### <span data-ttu-id="5bdd2-109">範例1：取得 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="5bdd2-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
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

## <span data-ttu-id="5bdd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="5bdd2-110">PARAMETERS</span></span>

### <span data-ttu-id="5bdd2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5bdd2-111">-DatabaseName</span></span>
<span data-ttu-id="5bdd2-112">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-112">SQL Database name.</span></span>

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

### <span data-ttu-id="5bdd2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bdd2-113">-ResourceGroupName</span></span>
<span data-ttu-id="5bdd2-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="5bdd2-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5bdd2-115">-ServerName</span></span>
<span data-ttu-id="5bdd2-116">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-116">SQL Database server name.</span></span>

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

### <span data-ttu-id="5bdd2-117">-確認</span><span class="sxs-lookup"><span data-stu-id="5bdd2-117">-Confirm</span></span>
<span data-ttu-id="5bdd2-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdd2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdd2-119">-WhatIf</span></span>
<span data-ttu-id="5bdd2-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bdd2-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdd2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdd2-122">-DefaultProfile</span></span>
<span data-ttu-id="5bdd2-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bdd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdd2-124">CommonParameters</span></span>
<span data-ttu-id="5bdd2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdd2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bdd2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdd2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5bdd2-127">INPUTS</span></span>

## <span data-ttu-id="5bdd2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5bdd2-128">OUTPUTS</span></span>

### <span data-ttu-id="5bdd2-129">DatabaseBlobAuditingSettingsModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="5bdd2-129">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="5bdd2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5bdd2-130">NOTES</span></span>

## <span data-ttu-id="5bdd2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bdd2-131">RELATED LINKS</span></span>

