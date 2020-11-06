---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 51e2c480b9a374136f2b040b8884cf85949b5fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450466"
---
# <span data-ttu-id="1ae52-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ae52-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="1ae52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ae52-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae52-103">取得資料庫的安全連線原則。</span><span class="sxs-lookup"><span data-stu-id="1ae52-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae52-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ae52-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ae52-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ae52-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae52-106">**AzureRmSqlDatabaseSecureConnectionPolicy** Cmdlet 會取得 Azure SQL 資料庫的加密通道原則。</span><span class="sxs-lookup"><span data-stu-id="1ae52-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="1ae52-107">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="1ae52-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="1ae52-108">成功執行此 Cmdlet 之後，它會傳回描述目前加密通道原則以及資料庫識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="1ae52-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="1ae52-109">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="1ae52-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="1ae52-110">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ae52-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1ae52-111">示例</span><span class="sxs-lookup"><span data-stu-id="1ae52-111">EXAMPLES</span></span>

### <span data-ttu-id="1ae52-112">範例1：取得 Azure SQL 資料庫的加密通道原則</span><span class="sxs-lookup"><span data-stu-id="1ae52-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="1ae52-113">這個命令會取得在伺服器 server01 上名為 database01 的 Azure SQL database 加密通道原則。</span><span class="sxs-lookup"><span data-stu-id="1ae52-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="1ae52-114">參數</span><span class="sxs-lookup"><span data-stu-id="1ae52-114">PARAMETERS</span></span>

### <span data-ttu-id="1ae52-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ae52-115">-DatabaseName</span></span>
<span data-ttu-id="1ae52-116">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae52-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1ae52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae52-117">-DefaultProfile</span></span>
<span data-ttu-id="1ae52-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1ae52-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ae52-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae52-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ae52-120">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae52-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1ae52-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ae52-121">-ServerName</span></span>
<span data-ttu-id="1ae52-122">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae52-122">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="1ae52-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1ae52-123">-Confirm</span></span>
<span data-ttu-id="1ae52-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ae52-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae52-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae52-125">-WhatIf</span></span>
<span data-ttu-id="1ae52-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ae52-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae52-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ae52-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae52-128">CommonParameters</span></span>
<span data-ttu-id="1ae52-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ae52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae52-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ae52-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae52-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1ae52-131">INPUTS</span></span>

### <span data-ttu-id="1ae52-132">所有</span><span class="sxs-lookup"><span data-stu-id="1ae52-132">None</span></span>
<span data-ttu-id="1ae52-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1ae52-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ae52-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1ae52-134">OUTPUTS</span></span>

### <span data-ttu-id="1ae52-135">DatabaseSecureConnectionPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="1ae52-135">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="1ae52-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1ae52-136">NOTES</span></span>

## <span data-ttu-id="1ae52-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ae52-137">RELATED LINKS</span></span>
