---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967553"
---
# <span data-ttu-id="c05a6-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c05a6-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="c05a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c05a6-102">SYNOPSIS</span></span>
<span data-ttu-id="c05a6-103">移除 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="c05a6-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="c05a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c05a6-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c05a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c05a6-105">DESCRIPTION</span></span>
<span data-ttu-id="c05a6-106">**AzureSqlDatabaseServer** Cmdlet 會從目前的訂閱中移除指定的 Azure SQL Database Server 實例。</span><span class="sxs-lookup"><span data-stu-id="c05a6-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="c05a6-107">這個 Cmdlet 會刪除伺服器上的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="c05a6-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="c05a6-108">示例</span><span class="sxs-lookup"><span data-stu-id="c05a6-108">EXAMPLES</span></span>

### <span data-ttu-id="c05a6-109">範例1：移除資料庫伺服器</span><span class="sxs-lookup"><span data-stu-id="c05a6-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="c05a6-110">這個命令會移除名為 lpqd0zbr8y 的 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="c05a6-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c05a6-111">參數</span><span class="sxs-lookup"><span data-stu-id="c05a6-111">PARAMETERS</span></span>

### <span data-ttu-id="c05a6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c05a6-112">-Force</span></span>
<span data-ttu-id="c05a6-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c05a6-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c05a6-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c05a6-114">-Profile</span></span>
<span data-ttu-id="c05a6-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c05a6-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c05a6-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c05a6-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c05a6-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c05a6-117">-ServerName</span></span>
<span data-ttu-id="c05a6-118">指定此 Cmdlet 移除的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c05a6-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="c05a6-119">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="c05a6-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="c05a6-120">-確認</span><span class="sxs-lookup"><span data-stu-id="c05a6-120">-Confirm</span></span>
<span data-ttu-id="c05a6-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c05a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c05a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c05a6-122">-WhatIf</span></span>
<span data-ttu-id="c05a6-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c05a6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c05a6-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c05a6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c05a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05a6-125">CommonParameters</span></span>
<span data-ttu-id="c05a6-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c05a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05a6-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c05a6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05a6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c05a6-128">INPUTS</span></span>

### <span data-ttu-id="c05a6-129">WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="c05a6-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="c05a6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c05a6-130">OUTPUTS</span></span>

## <span data-ttu-id="c05a6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c05a6-131">NOTES</span></span>

## <span data-ttu-id="c05a6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c05a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="c05a6-133">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="c05a6-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c05a6-134">刪除伺服器</span><span class="sxs-lookup"><span data-stu-id="c05a6-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="c05a6-135">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="c05a6-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c05a6-136">AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c05a6-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c05a6-137">新-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c05a6-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c05a6-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c05a6-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


