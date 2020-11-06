---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: f74abc2daab0c79c9d070d206a82b33fb15f23f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452984"
---
# <span data-ttu-id="f85b5-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f85b5-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="f85b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f85b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f85b5-103">指定資料庫使用其主機伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="f85b5-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f85b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f85b5-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f85b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f85b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f85b5-106">**AzureRmSqlServerAuditingPolicy** Cmdlet 會指定資料庫使用其主機伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="f85b5-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="f85b5-107">指定 [ *ResourceGroupName* ]、[ *伺服器名稱* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="f85b5-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f85b5-108">如果沒有為資料庫伺服器定義審核原則，此 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="f85b5-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="f85b5-109">如果主機使用伺服器層級審核，就會移除威脅偵測。</span><span class="sxs-lookup"><span data-stu-id="f85b5-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="f85b5-110">示例</span><span class="sxs-lookup"><span data-stu-id="f85b5-110">EXAMPLES</span></span>

### <span data-ttu-id="f85b5-111">範例1：將資料庫設定為使用其伺服器的審核原則</span><span class="sxs-lookup"><span data-stu-id="f85b5-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="f85b5-112">這個命令指定 Server02 上名為 Database01 的資料庫會使用伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="f85b5-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="f85b5-113">參數</span><span class="sxs-lookup"><span data-stu-id="f85b5-113">PARAMETERS</span></span>

### <span data-ttu-id="f85b5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f85b5-114">-DatabaseName</span></span>
<span data-ttu-id="f85b5-115">指定將使用審核原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f85b5-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="f85b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85b5-116">-DefaultProfile</span></span>
<span data-ttu-id="f85b5-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f85b5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f85b5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f85b5-118">-PassThru</span></span>
<span data-ttu-id="f85b5-119">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f85b5-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f85b5-120">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f85b5-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="f85b5-122">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f85b5-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f85b5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f85b5-123">-ServerName</span></span>
<span data-ttu-id="f85b5-124">指定託管使用審核原則之資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f85b5-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="f85b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85b5-125">CommonParameters</span></span>
<span data-ttu-id="f85b5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f85b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85b5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f85b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85b5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f85b5-128">INPUTS</span></span>

### <span data-ttu-id="f85b5-129">所有</span><span class="sxs-lookup"><span data-stu-id="f85b5-129">None</span></span>
<span data-ttu-id="f85b5-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f85b5-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f85b5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f85b5-131">OUTPUTS</span></span>

### <span data-ttu-id="f85b5-132">DatabaseAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="f85b5-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="f85b5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f85b5-133">NOTES</span></span>

## <span data-ttu-id="f85b5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f85b5-134">RELATED LINKS</span></span>

[<span data-ttu-id="f85b5-135">AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f85b5-135">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f85b5-136">AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f85b5-136">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f85b5-137">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f85b5-137">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="f85b5-138">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="f85b5-138">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="f85b5-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f85b5-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


