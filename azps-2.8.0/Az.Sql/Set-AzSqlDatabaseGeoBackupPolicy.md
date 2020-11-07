---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 6ac39ae2daba5f97b9046f3860eb34d3bb0f03ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792657"
---
# <span data-ttu-id="676cd-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="676cd-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="676cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="676cd-102">SYNOPSIS</span></span>
<span data-ttu-id="676cd-103">設定資料庫地域備份原則。</span><span class="sxs-lookup"><span data-stu-id="676cd-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="676cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="676cd-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="676cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="676cd-105">DESCRIPTION</span></span>
<span data-ttu-id="676cd-106">**AzSqlDatabaseGeoBackupPolicy** Cmdlet 會將 geo 備份策略設定為已登錄至資料庫。</span><span class="sxs-lookup"><span data-stu-id="676cd-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="676cd-107">這是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="676cd-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="676cd-108">示例</span><span class="sxs-lookup"><span data-stu-id="676cd-108">EXAMPLES</span></span>

## <span data-ttu-id="676cd-109">參數</span><span class="sxs-lookup"><span data-stu-id="676cd-109">PARAMETERS</span></span>

### <span data-ttu-id="676cd-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="676cd-110">-DatabaseName</span></span>
<span data-ttu-id="676cd-111">指定此 Cmdlet 設定 geo 備份原則之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="676cd-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="676cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="676cd-112">-DefaultProfile</span></span>
<span data-ttu-id="676cd-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="676cd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="676cd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="676cd-114">-ResourceGroupName</span></span>
<span data-ttu-id="676cd-115">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="676cd-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="676cd-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="676cd-116">-ServerName</span></span>
<span data-ttu-id="676cd-117">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="676cd-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="676cd-118">-State</span><span class="sxs-lookup"><span data-stu-id="676cd-118">-State</span></span>
<span data-ttu-id="676cd-119">指定 geo 備份原則的狀態。</span><span class="sxs-lookup"><span data-stu-id="676cd-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="676cd-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="676cd-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="676cd-121">後</span><span class="sxs-lookup"><span data-stu-id="676cd-121">Enabled</span></span> 
- <span data-ttu-id="676cd-122">禁止</span><span class="sxs-lookup"><span data-stu-id="676cd-122">Disabled</span></span>

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

### <span data-ttu-id="676cd-123">-確認</span><span class="sxs-lookup"><span data-stu-id="676cd-123">-Confirm</span></span>
<span data-ttu-id="676cd-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="676cd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="676cd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="676cd-125">-WhatIf</span></span>
<span data-ttu-id="676cd-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="676cd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="676cd-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="676cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="676cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676cd-128">CommonParameters</span></span>
<span data-ttu-id="676cd-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="676cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676cd-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="676cd-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676cd-131">輸入</span><span class="sxs-lookup"><span data-stu-id="676cd-131">INPUTS</span></span>

### <span data-ttu-id="676cd-132">System.object</span><span class="sxs-lookup"><span data-stu-id="676cd-132">System.String</span></span>

## <span data-ttu-id="676cd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="676cd-133">OUTPUTS</span></span>

### <span data-ttu-id="676cd-134">AzureSqlDatabaseGeoBackupPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="676cd-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="676cd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="676cd-135">NOTES</span></span>

## <span data-ttu-id="676cd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="676cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="676cd-137">AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="676cd-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="676cd-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="676cd-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

