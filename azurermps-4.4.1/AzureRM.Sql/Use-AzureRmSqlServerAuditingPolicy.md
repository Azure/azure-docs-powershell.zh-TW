---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 9e3e94109904bc14f22e2ca2c08936316ed597db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451583"
---
# <span data-ttu-id="150f8-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="150f8-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="150f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="150f8-102">SYNOPSIS</span></span>
<span data-ttu-id="150f8-103">指定資料庫使用其主機伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="150f8-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="150f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="150f8-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="150f8-105">DESCRIPTION</span></span>
<span data-ttu-id="150f8-106">**AzureRmSqlServerAuditingPolicy** Cmdlet 會指定資料庫使用其主機伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="150f8-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="150f8-107">指定 [ *ResourceGroupName* ]、[ *伺服器名稱* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="150f8-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="150f8-108">如果沒有為資料庫伺服器定義審核原則，此 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="150f8-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>

<span data-ttu-id="150f8-109">如果主機使用伺服器層級審核，就會移除威脅偵測。</span><span class="sxs-lookup"><span data-stu-id="150f8-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="150f8-110">示例</span><span class="sxs-lookup"><span data-stu-id="150f8-110">EXAMPLES</span></span>

### <span data-ttu-id="150f8-111">範例1：將資料庫設定為使用其伺服器的審核原則</span><span class="sxs-lookup"><span data-stu-id="150f8-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="150f8-112">這個命令指定 Server02 上名為 Database01 的資料庫會使用伺服器的審核原則。</span><span class="sxs-lookup"><span data-stu-id="150f8-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="150f8-113">參數</span><span class="sxs-lookup"><span data-stu-id="150f8-113">PARAMETERS</span></span>

### <span data-ttu-id="150f8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="150f8-114">-DatabaseName</span></span>
<span data-ttu-id="150f8-115">指定將使用審核原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="150f8-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="150f8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="150f8-116">-PassThru</span></span>
<span data-ttu-id="150f8-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="150f8-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="150f8-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="150f8-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="150f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="150f8-120">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="150f8-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="150f8-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="150f8-121">-ServerName</span></span>
<span data-ttu-id="150f8-122">指定託管使用審核原則之資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="150f8-122">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="150f8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150f8-123">-DefaultProfile</span></span>
<span data-ttu-id="150f8-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="150f8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150f8-125">CommonParameters</span></span>
<span data-ttu-id="150f8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="150f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150f8-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="150f8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150f8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="150f8-128">INPUTS</span></span>

## <span data-ttu-id="150f8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="150f8-129">OUTPUTS</span></span>

### <span data-ttu-id="150f8-130">DatabaseAuditingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="150f8-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="150f8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="150f8-131">NOTES</span></span>

## <span data-ttu-id="150f8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="150f8-132">RELATED LINKS</span></span>

[<span data-ttu-id="150f8-133">AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="150f8-133">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="150f8-134">AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="150f8-134">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="150f8-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="150f8-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="150f8-136">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="150f8-136">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="150f8-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="150f8-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


