---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449484"
---
# <span data-ttu-id="8f513-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f513-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="8f513-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f513-102">SYNOPSIS</span></span>
<span data-ttu-id="8f513-103">設定伺服器的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="8f513-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f513-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f513-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f513-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f513-105">DESCRIPTION</span></span>
<span data-ttu-id="8f513-106">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** Cmdlet 會設定已登錄到此資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="8f513-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="8f513-107">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="8f513-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="8f513-108">示例</span><span class="sxs-lookup"><span data-stu-id="8f513-108">EXAMPLES</span></span>

## <span data-ttu-id="8f513-109">參數</span><span class="sxs-lookup"><span data-stu-id="8f513-109">PARAMETERS</span></span>

### <span data-ttu-id="8f513-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f513-110">-DatabaseName</span></span>
<span data-ttu-id="8f513-111">指定此 Cmdlet 為其設定原則的 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f513-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="8f513-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f513-112">-ResourceGroupName</span></span>
<span data-ttu-id="8f513-113">指定包含資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f513-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="8f513-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f513-114">-ResourceId</span></span>
<span data-ttu-id="8f513-115">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f513-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f513-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f513-116">-ServerName</span></span>
<span data-ttu-id="8f513-117">指定託管資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8f513-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="8f513-118">-State</span><span class="sxs-lookup"><span data-stu-id="8f513-118">-State</span></span>
<span data-ttu-id="8f513-119">指定狀態。</span><span class="sxs-lookup"><span data-stu-id="8f513-119">Specifies a state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f513-120">-確認</span><span class="sxs-lookup"><span data-stu-id="8f513-120">-Confirm</span></span>
<span data-ttu-id="8f513-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f513-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f513-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f513-122">-WhatIf</span></span>
<span data-ttu-id="8f513-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f513-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f513-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f513-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f513-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f513-125">-DefaultProfile</span></span>
<span data-ttu-id="8f513-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f513-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f513-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f513-127">CommonParameters</span></span>
<span data-ttu-id="8f513-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f513-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f513-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f513-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f513-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8f513-130">INPUTS</span></span>

## <span data-ttu-id="8f513-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8f513-131">OUTPUTS</span></span>

## <span data-ttu-id="8f513-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8f513-132">NOTES</span></span>

## <span data-ttu-id="8f513-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f513-133">RELATED LINKS</span></span>

[<span data-ttu-id="8f513-134">AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f513-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8f513-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="8f513-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
