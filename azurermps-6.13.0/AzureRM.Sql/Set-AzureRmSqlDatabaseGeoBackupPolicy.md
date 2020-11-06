---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: c7aa097318f65cd2506ccfcd96e4d9eeeaf9d1bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447222"
---
# <span data-ttu-id="fcf1a-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fcf1a-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="fcf1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fcf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf1a-103">設定資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcf1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fcf1a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="fcf1a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf1a-106">**AzureRmSqlDatabaseGeoBackupPolicy** Cmdlet 會將 geo 備份策略設定為已登錄至資料庫。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="fcf1a-107">這是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="fcf1a-108">示例</span><span class="sxs-lookup"><span data-stu-id="fcf1a-108">EXAMPLES</span></span>

## <span data-ttu-id="fcf1a-109">參數</span><span class="sxs-lookup"><span data-stu-id="fcf1a-109">PARAMETERS</span></span>

### <span data-ttu-id="fcf1a-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fcf1a-110">-DatabaseName</span></span>
<span data-ttu-id="fcf1a-111">指定此 Cmdlet 設定 geo 備份原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="fcf1a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf1a-112">-DefaultProfile</span></span>
<span data-ttu-id="fcf1a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fcf1a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcf1a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf1a-114">-ResourceGroupName</span></span>
<span data-ttu-id="fcf1a-115">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="fcf1a-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fcf1a-116">-ServerName</span></span>
<span data-ttu-id="fcf1a-117">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fcf1a-118">-State</span><span class="sxs-lookup"><span data-stu-id="fcf1a-118">-State</span></span>
<span data-ttu-id="fcf1a-119">指定 geo 備份原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="fcf1a-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fcf1a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fcf1a-121">後</span><span class="sxs-lookup"><span data-stu-id="fcf1a-121">Enabled</span></span> 
- <span data-ttu-id="fcf1a-122">禁止</span><span class="sxs-lookup"><span data-stu-id="fcf1a-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf1a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="fcf1a-123">-Confirm</span></span>
<span data-ttu-id="fcf1a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf1a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf1a-125">-WhatIf</span></span>
<span data-ttu-id="fcf1a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf1a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf1a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf1a-128">CommonParameters</span></span>
<span data-ttu-id="fcf1a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf1a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf1a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fcf1a-131">INPUTS</span></span>

### <span data-ttu-id="fcf1a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="fcf1a-132">System.String</span></span>

## <span data-ttu-id="fcf1a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fcf1a-133">OUTPUTS</span></span>

### <span data-ttu-id="fcf1a-134">AzureSqlDatabaseGeoBackupPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="fcf1a-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="fcf1a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fcf1a-135">NOTES</span></span>

## <span data-ttu-id="fcf1a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcf1a-136">RELATED LINKS</span></span>

[<span data-ttu-id="fcf1a-137">AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="fcf1a-137">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="fcf1a-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="fcf1a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

