---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792537"
---
# <span data-ttu-id="73180-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73180-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="73180-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73180-102">SYNOPSIS</span></span>
<span data-ttu-id="73180-103">取得資料庫的安全連線原則。</span><span class="sxs-lookup"><span data-stu-id="73180-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="73180-104">安全連線已棄用，在未來版本中將會移除此命令。</span><span class="sxs-lookup"><span data-stu-id="73180-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="73180-105">請使用 Azure 入口網站中的 SQL 資料庫 blade 來查看連接字串</span><span class="sxs-lookup"><span data-stu-id="73180-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="73180-106">句法</span><span class="sxs-lookup"><span data-stu-id="73180-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73180-107">說明</span><span class="sxs-lookup"><span data-stu-id="73180-107">DESCRIPTION</span></span>
<span data-ttu-id="73180-108">**AzSqlDatabaseSecureConnectionPolicy** Cmdlet 會取得 Azure SQL 資料庫的加密通道原則。</span><span class="sxs-lookup"><span data-stu-id="73180-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="73180-109">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="73180-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="73180-110">成功執行此 Cmdlet 之後，它會傳回描述目前加密通道原則以及資料庫識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="73180-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="73180-111">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="73180-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="73180-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73180-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="73180-113">示例</span><span class="sxs-lookup"><span data-stu-id="73180-113">EXAMPLES</span></span>

### <span data-ttu-id="73180-114">範例1：取得 Azure SQL 資料庫的加密通道原則</span><span class="sxs-lookup"><span data-stu-id="73180-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="73180-115">這個命令會取得在伺服器 server01 上名為 database01 的 Azure SQL database 加密通道原則。</span><span class="sxs-lookup"><span data-stu-id="73180-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="73180-116">參數</span><span class="sxs-lookup"><span data-stu-id="73180-116">PARAMETERS</span></span>

### <span data-ttu-id="73180-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73180-117">-DatabaseName</span></span>
<span data-ttu-id="73180-118">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="73180-118">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="73180-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73180-119">-DefaultProfile</span></span>
<span data-ttu-id="73180-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="73180-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73180-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73180-121">-ResourceGroupName</span></span>
<span data-ttu-id="73180-122">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73180-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="73180-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73180-123">-ServerName</span></span>
<span data-ttu-id="73180-124">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="73180-124">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="73180-125">-確認</span><span class="sxs-lookup"><span data-stu-id="73180-125">-Confirm</span></span>
<span data-ttu-id="73180-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73180-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73180-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73180-127">-WhatIf</span></span>
<span data-ttu-id="73180-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73180-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73180-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73180-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73180-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73180-130">CommonParameters</span></span>
<span data-ttu-id="73180-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73180-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73180-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73180-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73180-133">輸入</span><span class="sxs-lookup"><span data-stu-id="73180-133">INPUTS</span></span>

### <span data-ttu-id="73180-134">System.object</span><span class="sxs-lookup"><span data-stu-id="73180-134">System.String</span></span>

## <span data-ttu-id="73180-135">輸出</span><span class="sxs-lookup"><span data-stu-id="73180-135">OUTPUTS</span></span>

### <span data-ttu-id="73180-136">DatabaseSecureConnectionPolicyModel 中的 [SecureConnection]</span><span class="sxs-lookup"><span data-stu-id="73180-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="73180-137">筆記</span><span class="sxs-lookup"><span data-stu-id="73180-137">NOTES</span></span>

## <span data-ttu-id="73180-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="73180-138">RELATED LINKS</span></span>
