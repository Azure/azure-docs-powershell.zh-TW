---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a7cf769b1150ef7e209bd02234674bb26927f9a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450165"
---
# <span data-ttu-id="92ff2-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="92ff2-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="92ff2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="92ff2-103">移除資料庫的審核。</span><span class="sxs-lookup"><span data-stu-id="92ff2-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92ff2-104">句法</span><span class="sxs-lookup"><span data-stu-id="92ff2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92ff2-105">說明</span><span class="sxs-lookup"><span data-stu-id="92ff2-105">DESCRIPTION</span></span>
<span data-ttu-id="92ff2-106">**AzureRmSqlDatabaseAuditing** Cmdlet 會移除 Azure SQL 資料庫的審核。</span><span class="sxs-lookup"><span data-stu-id="92ff2-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="92ff2-107">若要使用這個 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="92ff2-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="92ff2-108">在您執行此 Cmdlet 之後，就不會執行資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="92ff2-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="92ff2-109">如果命令成功且您已使用 *PassThru* 參數，則除了資料庫識別碼之外，該 Cmdlet 還會傳回描述目前審核原則的物件。</span><span class="sxs-lookup"><span data-stu-id="92ff2-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="92ff2-110">資料庫識別碼包括但不限於 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="92ff2-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>
<span data-ttu-id="92ff2-111">如果您移除 Azure SQL 資料庫的審核，也會移除威脅檢測。</span><span class="sxs-lookup"><span data-stu-id="92ff2-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>
<span data-ttu-id="92ff2-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92ff2-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="92ff2-113">示例</span><span class="sxs-lookup"><span data-stu-id="92ff2-113">EXAMPLES</span></span>

### <span data-ttu-id="92ff2-114">範例1：移除 Azure SQL 資料庫的審核</span><span class="sxs-lookup"><span data-stu-id="92ff2-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="92ff2-115">這個命令會移除名為 Database01 的資料庫審核。</span><span class="sxs-lookup"><span data-stu-id="92ff2-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="92ff2-116">該資料庫位於 Server01，該資料庫會指派給名為 ResourceGroup01 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="92ff2-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="92ff2-117">參數</span><span class="sxs-lookup"><span data-stu-id="92ff2-117">PARAMETERS</span></span>

### <span data-ttu-id="92ff2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92ff2-118">-DatabaseName</span></span>
<span data-ttu-id="92ff2-119">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="92ff2-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="92ff2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ff2-120">-DefaultProfile</span></span>
<span data-ttu-id="92ff2-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="92ff2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92ff2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92ff2-122">-PassThru</span></span>
<span data-ttu-id="92ff2-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="92ff2-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="92ff2-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="92ff2-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ff2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ff2-125">-ResourceGroupName</span></span>
<span data-ttu-id="92ff2-126">指定包含資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92ff2-126">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="92ff2-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="92ff2-127">-ServerName</span></span>
<span data-ttu-id="92ff2-128">指定包含資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="92ff2-128">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="92ff2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="92ff2-129">-Confirm</span></span>
<span data-ttu-id="92ff2-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92ff2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ff2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ff2-131">-WhatIf</span></span>
<span data-ttu-id="92ff2-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92ff2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92ff2-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92ff2-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ff2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ff2-134">CommonParameters</span></span>
<span data-ttu-id="92ff2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92ff2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ff2-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92ff2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ff2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="92ff2-137">INPUTS</span></span>

### <span data-ttu-id="92ff2-138">System.object</span><span class="sxs-lookup"><span data-stu-id="92ff2-138">System.String</span></span>

## <span data-ttu-id="92ff2-139">輸出</span><span class="sxs-lookup"><span data-stu-id="92ff2-139">OUTPUTS</span></span>

### <span data-ttu-id="92ff2-140">AuditingPolicyModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="92ff2-140">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="92ff2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="92ff2-141">NOTES</span></span>

## <span data-ttu-id="92ff2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="92ff2-142">RELATED LINKS</span></span>

[<span data-ttu-id="92ff2-143">AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="92ff2-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="92ff2-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="92ff2-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="92ff2-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="92ff2-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


