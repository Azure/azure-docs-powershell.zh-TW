---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967017"
---
# <span data-ttu-id="529c3-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="529c3-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="529c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="529c3-102">SYNOPSIS</span></span>
<span data-ttu-id="529c3-103">取得有關 Azure SQL 資料庫伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="529c3-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="529c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="529c3-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="529c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="529c3-105">DESCRIPTION</span></span>
<span data-ttu-id="529c3-106">**AzureSqlDatabaseServer** Cmdlet 會在目前的訂閱中取得 Azure SQL Database Server 實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="529c3-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="529c3-107">如果您依名稱指定伺服器，這個 Cmdlet 會傳回包含該伺服器相關資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="529c3-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="529c3-108">否則，Cmdlet 會傳回所有伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="529c3-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="529c3-109">示例</span><span class="sxs-lookup"><span data-stu-id="529c3-109">EXAMPLES</span></span>

### <span data-ttu-id="529c3-110">範例1：取得所有伺服器的相關資訊</span><span class="sxs-lookup"><span data-stu-id="529c3-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="529c3-111">這個命令會傳回目前訂閱中所有 Azure SQL Database Server 實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="529c3-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="529c3-112">範例2：取得特定伺服器的相關資訊</span><span class="sxs-lookup"><span data-stu-id="529c3-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="529c3-113">這個命令會傳回名為 lpqd0zbr8y 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="529c3-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="529c3-114">參數</span><span class="sxs-lookup"><span data-stu-id="529c3-114">PARAMETERS</span></span>

### <span data-ttu-id="529c3-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="529c3-115">-Profile</span></span>
<span data-ttu-id="529c3-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="529c3-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="529c3-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="529c3-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529c3-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="529c3-118">-ServerName</span></span>
<span data-ttu-id="529c3-119">指定此 Cmdlet 移除的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="529c3-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="529c3-120">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="529c3-120">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529c3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529c3-121">CommonParameters</span></span>
<span data-ttu-id="529c3-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="529c3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529c3-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="529c3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529c3-124">輸入</span><span class="sxs-lookup"><span data-stu-id="529c3-124">INPUTS</span></span>

### <span data-ttu-id="529c3-125">WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="529c3-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="529c3-126">輸出</span><span class="sxs-lookup"><span data-stu-id="529c3-126">OUTPUTS</span></span>

### <span data-ttu-id="529c3-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="529c3-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="529c3-128">筆記</span><span class="sxs-lookup"><span data-stu-id="529c3-128">NOTES</span></span>

## <span data-ttu-id="529c3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="529c3-129">RELATED LINKS</span></span>

[<span data-ttu-id="529c3-130">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="529c3-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="529c3-131">清單伺服器</span><span class="sxs-lookup"><span data-stu-id="529c3-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="529c3-132">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="529c3-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="529c3-133">新-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="529c3-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="529c3-134">移除-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="529c3-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="529c3-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="529c3-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


