---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968009"
---
# <span data-ttu-id="675a9-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="675a9-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="675a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="675a9-102">SYNOPSIS</span></span>
<span data-ttu-id="675a9-103">取得 SQL 資料庫的大小與大小限制。</span><span class="sxs-lookup"><span data-stu-id="675a9-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="675a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="675a9-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="675a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="675a9-105">DESCRIPTION</span></span>
<span data-ttu-id="675a9-106">**AzureSqlDatabaseUsages** Cmdlet 會取得 Azure SQL 資料庫目前的大小和大小限制。</span><span class="sxs-lookup"><span data-stu-id="675a9-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="675a9-107">示例</span><span class="sxs-lookup"><span data-stu-id="675a9-107">EXAMPLES</span></span>

### <span data-ttu-id="675a9-108">範例1：取得 SQL 資料庫的使用資訊</span><span class="sxs-lookup"><span data-stu-id="675a9-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="675a9-109">這個命令會在 Server01 上取得名為 Database01 之 SQL Database 的大小和大小限制資訊。</span><span class="sxs-lookup"><span data-stu-id="675a9-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="675a9-110">參數</span><span class="sxs-lookup"><span data-stu-id="675a9-110">PARAMETERS</span></span>

### <span data-ttu-id="675a9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="675a9-111">-DatabaseName</span></span>
<span data-ttu-id="675a9-112">指定 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="675a9-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="675a9-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="675a9-113">-Profile</span></span>
<span data-ttu-id="675a9-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="675a9-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="675a9-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="675a9-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="675a9-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="675a9-116">-ServerName</span></span>
<span data-ttu-id="675a9-117">指定託管 Azure SQL 資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="675a9-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

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

### <span data-ttu-id="675a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675a9-118">CommonParameters</span></span>
<span data-ttu-id="675a9-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="675a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675a9-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="675a9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675a9-121">輸入</span><span class="sxs-lookup"><span data-stu-id="675a9-121">INPUTS</span></span>

## <span data-ttu-id="675a9-122">輸出</span><span class="sxs-lookup"><span data-stu-id="675a9-122">OUTPUTS</span></span>

## <span data-ttu-id="675a9-123">筆記</span><span class="sxs-lookup"><span data-stu-id="675a9-123">NOTES</span></span>

## <span data-ttu-id="675a9-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="675a9-124">RELATED LINKS</span></span>

