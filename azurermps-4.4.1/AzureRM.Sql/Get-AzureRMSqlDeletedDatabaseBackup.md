---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 9ffccf1122ac9919758883100eacce7933f5fea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447935"
---
# <span data-ttu-id="3eb55-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="3eb55-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="3eb55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3eb55-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb55-103">取得您可以還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="3eb55-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb55-104">句法</span><span class="sxs-lookup"><span data-stu-id="3eb55-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb55-105">說明</span><span class="sxs-lookup"><span data-stu-id="3eb55-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb55-106">**AzureRMSqlDeletedDatabaseBackup** Cmdlet 會取得您可以還原的指定已刪除 SQL 資料庫備份，或是您可以還原的所有已刪除備份。</span><span class="sxs-lookup"><span data-stu-id="3eb55-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="3eb55-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eb55-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3eb55-108">示例</span><span class="sxs-lookup"><span data-stu-id="3eb55-108">EXAMPLES</span></span>

### <span data-ttu-id="3eb55-109">範例1：在伺服器上取得所有已刪除的資料庫備份</span><span class="sxs-lookup"><span data-stu-id="3eb55-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="3eb55-110">這個命令會在伺服器上取得所有已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="3eb55-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="3eb55-111">範例2：取得指定的已刪除資料庫備份</span><span class="sxs-lookup"><span data-stu-id="3eb55-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="3eb55-112">這個命令會取得 ContosoDatabase 的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="3eb55-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="3eb55-113">參數</span><span class="sxs-lookup"><span data-stu-id="3eb55-113">PARAMETERS</span></span>

### <span data-ttu-id="3eb55-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3eb55-114">-DatabaseName</span></span>
<span data-ttu-id="3eb55-115">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3eb55-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb55-116">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="3eb55-116">-DeletionDate</span></span>
<span data-ttu-id="3eb55-117">指定資料庫已刪除的日期，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="3eb55-117">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="3eb55-118">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eb55-118">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb55-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb55-119">-ResourceGroupName</span></span>
<span data-ttu-id="3eb55-120">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3eb55-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3eb55-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3eb55-121">-ServerName</span></span>
<span data-ttu-id="3eb55-122">指定資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3eb55-122">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="3eb55-123">-確認</span><span class="sxs-lookup"><span data-stu-id="3eb55-123">-Confirm</span></span>
<span data-ttu-id="3eb55-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3eb55-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb55-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb55-125">-WhatIf</span></span>
<span data-ttu-id="3eb55-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3eb55-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb55-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eb55-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb55-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb55-128">-DefaultProfile</span></span>
<span data-ttu-id="3eb55-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3eb55-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eb55-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb55-130">CommonParameters</span></span>
<span data-ttu-id="3eb55-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3eb55-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb55-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3eb55-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb55-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3eb55-133">INPUTS</span></span>

## <span data-ttu-id="3eb55-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3eb55-134">OUTPUTS</span></span>

## <span data-ttu-id="3eb55-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3eb55-135">NOTES</span></span>

## <span data-ttu-id="3eb55-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eb55-136">RELATED LINKS</span></span>

[<span data-ttu-id="3eb55-137">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3eb55-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="3eb55-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3eb55-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
