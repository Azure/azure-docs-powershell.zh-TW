---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447934"
---
# <span data-ttu-id="90b99-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="90b99-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="90b99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90b99-102">SYNOPSIS</span></span>
<span data-ttu-id="90b99-103">取得資料庫長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="90b99-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90b99-104">句法</span><span class="sxs-lookup"><span data-stu-id="90b99-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90b99-105">說明</span><span class="sxs-lookup"><span data-stu-id="90b99-105">DESCRIPTION</span></span>
<span data-ttu-id="90b99-106">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** Cmdlet 會取得向這個資料庫註冊的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="90b99-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="90b99-107">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="90b99-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="90b99-108">示例</span><span class="sxs-lookup"><span data-stu-id="90b99-108">EXAMPLES</span></span>

## <span data-ttu-id="90b99-109">參數</span><span class="sxs-lookup"><span data-stu-id="90b99-109">PARAMETERS</span></span>

### <span data-ttu-id="90b99-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90b99-110">-DatabaseName</span></span>
<span data-ttu-id="90b99-111">指定此 Cmdlet 取得其原則之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="90b99-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="90b99-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b99-112">-ResourceGroupName</span></span>
<span data-ttu-id="90b99-113">指定包含資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90b99-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="90b99-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90b99-114">-ServerName</span></span>
<span data-ttu-id="90b99-115">指定託管資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="90b99-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="90b99-116">-確認</span><span class="sxs-lookup"><span data-stu-id="90b99-116">-Confirm</span></span>
<span data-ttu-id="90b99-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90b99-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b99-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b99-118">-WhatIf</span></span>
<span data-ttu-id="90b99-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90b99-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b99-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90b99-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b99-121">-DefaultProfile</span></span>
<span data-ttu-id="90b99-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90b99-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b99-123">CommonParameters</span></span>
<span data-ttu-id="90b99-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90b99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b99-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90b99-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b99-126">輸入</span><span class="sxs-lookup"><span data-stu-id="90b99-126">INPUTS</span></span>

## <span data-ttu-id="90b99-127">輸出</span><span class="sxs-lookup"><span data-stu-id="90b99-127">OUTPUTS</span></span>

## <span data-ttu-id="90b99-128">筆記</span><span class="sxs-lookup"><span data-stu-id="90b99-128">NOTES</span></span>

## <span data-ttu-id="90b99-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="90b99-129">RELATED LINKS</span></span>

[<span data-ttu-id="90b99-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="90b99-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="90b99-131">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="90b99-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
