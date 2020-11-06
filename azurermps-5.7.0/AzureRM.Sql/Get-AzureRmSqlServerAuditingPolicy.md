---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a12c9846b9e52d3c5e19c74b5a0f755acb27daf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447624"
---
# <span data-ttu-id="9543c-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9543c-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="9543c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9543c-102">SYNOPSIS</span></span>
<span data-ttu-id="9543c-103">取得 SQL server 的審核原則。</span><span class="sxs-lookup"><span data-stu-id="9543c-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9543c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9543c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9543c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9543c-105">DESCRIPTION</span></span>
<span data-ttu-id="9543c-106">**AzureRmSqlServerAuditingPolicy** Cmdlet 會取得 Azure SQL server 的審核原則。</span><span class="sxs-lookup"><span data-stu-id="9543c-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="9543c-107">指定 [ *ResourceGroupName* ]、[ *伺服器名稱* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="9543c-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9543c-108">這個 Cmdlet 會傳回在指定的 Azure SQL server 中定義且使用其審核原則的 Azure SQL 資料庫所使用的原則。</span><span class="sxs-lookup"><span data-stu-id="9543c-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="9543c-109">示例</span><span class="sxs-lookup"><span data-stu-id="9543c-109">EXAMPLES</span></span>

### <span data-ttu-id="9543c-110">範例1：取得 Azure SQL server 的審核原則，並在其上定義 [資料表審核]</span><span class="sxs-lookup"><span data-stu-id="9543c-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="9543c-111">範例2：取得已定義 Blob 審核的 Azure SQL server 審核原則</span><span class="sxs-lookup"><span data-stu-id="9543c-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

## <span data-ttu-id="9543c-112">參數</span><span class="sxs-lookup"><span data-stu-id="9543c-112">PARAMETERS</span></span>

### <span data-ttu-id="9543c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9543c-113">-DefaultProfile</span></span>
<span data-ttu-id="9543c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9543c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9543c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9543c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9543c-116">指定 Azure SQL server 指派至的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9543c-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="9543c-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9543c-117">-ServerName</span></span>
<span data-ttu-id="9543c-118">指定此 Cmdlet 取得審核原則之 Azure SQL server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9543c-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9543c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9543c-119">-Confirm</span></span>
<span data-ttu-id="9543c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9543c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9543c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9543c-121">-WhatIf</span></span>
<span data-ttu-id="9543c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9543c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9543c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9543c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9543c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9543c-124">CommonParameters</span></span>
<span data-ttu-id="9543c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9543c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9543c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9543c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9543c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9543c-127">INPUTS</span></span>

### <span data-ttu-id="9543c-128">所有</span><span class="sxs-lookup"><span data-stu-id="9543c-128">None</span></span>
<span data-ttu-id="9543c-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9543c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9543c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9543c-130">OUTPUTS</span></span>

### <span data-ttu-id="9543c-131">ServerAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="9543c-131">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="9543c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9543c-132">NOTES</span></span>

## <span data-ttu-id="9543c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9543c-133">RELATED LINKS</span></span>

[<span data-ttu-id="9543c-134">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9543c-134">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="9543c-135">使用-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9543c-135">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="9543c-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="9543c-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


