---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 3e43a61c95120b0f07f89e3f3fb64aab2dee8dff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449705"
---
# <span data-ttu-id="3fabb-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="3fabb-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="3fabb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fabb-102">SYNOPSIS</span></span>
<span data-ttu-id="3fabb-103">移除 SQL server 的審核。</span><span class="sxs-lookup"><span data-stu-id="3fabb-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fabb-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fabb-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fabb-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fabb-105">DESCRIPTION</span></span>
<span data-ttu-id="3fabb-106">**AzureRmSqlServerAuditing** Cmdlet 會移除 Azure SQL server 的審核。</span><span class="sxs-lookup"><span data-stu-id="3fabb-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="3fabb-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="3fabb-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="3fabb-108">在您執行此 Cmdlet 之後，就不會執行在 Azure SQL server 上審核資料庫的工作。</span><span class="sxs-lookup"><span data-stu-id="3fabb-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="3fabb-109">如果命令成功，且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述目前審核原則和 Azure SQL server 識別碼的物件。</span><span class="sxs-lookup"><span data-stu-id="3fabb-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="3fabb-110">伺服器識別碼包括 **ResourceGroupName** 和 **ServerName** 。</span><span class="sxs-lookup"><span data-stu-id="3fabb-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="3fabb-111">示例</span><span class="sxs-lookup"><span data-stu-id="3fabb-111">EXAMPLES</span></span>

### <span data-ttu-id="3fabb-112">範例1：移除 Azure SQL server 的審核</span><span class="sxs-lookup"><span data-stu-id="3fabb-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlServerAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="3fabb-113">這個命令會移除位於 [資源群組] 中 Server01 的所有資料庫的審核。</span><span class="sxs-lookup"><span data-stu-id="3fabb-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="3fabb-114">參數</span><span class="sxs-lookup"><span data-stu-id="3fabb-114">PARAMETERS</span></span>

### <span data-ttu-id="3fabb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fabb-115">-DefaultProfile</span></span>
<span data-ttu-id="3fabb-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3fabb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fabb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fabb-117">-PassThru</span></span>
<span data-ttu-id="3fabb-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3fabb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3fabb-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3fabb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fabb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fabb-120">-ResourceGroupName</span></span>
<span data-ttu-id="3fabb-121">指定 Azure SQL server 指派至的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fabb-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="3fabb-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3fabb-122">-ServerName</span></span>
<span data-ttu-id="3fabb-123">指定 Azure SQL server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fabb-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fabb-124">-確認</span><span class="sxs-lookup"><span data-stu-id="3fabb-124">-Confirm</span></span>
<span data-ttu-id="3fabb-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fabb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fabb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fabb-126">-WhatIf</span></span>
<span data-ttu-id="3fabb-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fabb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fabb-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fabb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fabb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fabb-129">CommonParameters</span></span>
<span data-ttu-id="3fabb-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fabb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fabb-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fabb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fabb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3fabb-132">INPUTS</span></span>

### <span data-ttu-id="3fabb-133">System.object</span><span class="sxs-lookup"><span data-stu-id="3fabb-133">System.String</span></span>

## <span data-ttu-id="3fabb-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3fabb-134">OUTPUTS</span></span>

### <span data-ttu-id="3fabb-135">AuditingPolicyModel （.Sql） .Sql。</span><span class="sxs-lookup"><span data-stu-id="3fabb-135">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="3fabb-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3fabb-136">NOTES</span></span>

## <span data-ttu-id="3fabb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fabb-137">RELATED LINKS</span></span>

[<span data-ttu-id="3fabb-138">AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="3fabb-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="3fabb-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="3fabb-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="3fabb-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="3fabb-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


