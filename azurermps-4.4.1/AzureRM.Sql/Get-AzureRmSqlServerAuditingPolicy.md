---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449487"
---
# <span data-ttu-id="abaff-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="abaff-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="abaff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abaff-102">SYNOPSIS</span></span>
<span data-ttu-id="abaff-103">取得 SQL server 的審核原則。</span><span class="sxs-lookup"><span data-stu-id="abaff-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abaff-104">句法</span><span class="sxs-lookup"><span data-stu-id="abaff-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abaff-105">說明</span><span class="sxs-lookup"><span data-stu-id="abaff-105">DESCRIPTION</span></span>
<span data-ttu-id="abaff-106">**AzureRmSqlServerAuditingPolicy** Cmdlet 會取得 Azure SQL server 的審核原則。</span><span class="sxs-lookup"><span data-stu-id="abaff-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="abaff-107">指定 [ *ResourceGroupName* ]、[ *伺服器名稱* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="abaff-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="abaff-108">這個 Cmdlet 會傳回在指定的 Azure SQL server 中定義且使用其審核原則的 Azure SQL 資料庫所使用的原則。</span><span class="sxs-lookup"><span data-stu-id="abaff-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="abaff-109">示例</span><span class="sxs-lookup"><span data-stu-id="abaff-109">EXAMPLES</span></span>

### <span data-ttu-id="abaff-110">範例1：取得 Azure SQL server 的審核原則，並在其上定義 [資料表審核]</span><span class="sxs-lookup"><span data-stu-id="abaff-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
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

### <span data-ttu-id="abaff-111">範例2：取得已定義 Blob 審核的 Azure SQL server 審核原則</span><span class="sxs-lookup"><span data-stu-id="abaff-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="abaff-112">參數</span><span class="sxs-lookup"><span data-stu-id="abaff-112">PARAMETERS</span></span>

### <span data-ttu-id="abaff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abaff-113">-ResourceGroupName</span></span>
<span data-ttu-id="abaff-114">指定 Azure SQL server 指派至的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="abaff-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="abaff-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="abaff-115">-ServerName</span></span>
<span data-ttu-id="abaff-116">指定此 Cmdlet 取得審核原則之 Azure SQL server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="abaff-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abaff-117">-確認</span><span class="sxs-lookup"><span data-stu-id="abaff-117">-Confirm</span></span>
<span data-ttu-id="abaff-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="abaff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abaff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abaff-119">-WhatIf</span></span>
<span data-ttu-id="abaff-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="abaff-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abaff-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="abaff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abaff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abaff-122">-DefaultProfile</span></span>
<span data-ttu-id="abaff-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="abaff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abaff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abaff-124">CommonParameters</span></span>
<span data-ttu-id="abaff-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abaff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abaff-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abaff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abaff-127">輸入</span><span class="sxs-lookup"><span data-stu-id="abaff-127">INPUTS</span></span>

## <span data-ttu-id="abaff-128">輸出</span><span class="sxs-lookup"><span data-stu-id="abaff-128">OUTPUTS</span></span>

### <span data-ttu-id="abaff-129">ServerAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="abaff-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="abaff-130">筆記</span><span class="sxs-lookup"><span data-stu-id="abaff-130">NOTES</span></span>

## <span data-ttu-id="abaff-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="abaff-131">RELATED LINKS</span></span>

[<span data-ttu-id="abaff-132">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="abaff-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="abaff-133">使用-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="abaff-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="abaff-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="abaff-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


