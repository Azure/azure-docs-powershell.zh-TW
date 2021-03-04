---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 79d920f866991cae15e2da08d03e2eecd4d2e91e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906365"
---
# <span data-ttu-id="6ed5c-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="6ed5c-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="6ed5c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ed5c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed5c-103">為兩個 SQL Database 伺服器之間的彈性資料庫交易建立通訊連結。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="6ed5c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ed5c-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ed5c-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ed5c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ed5c-106">**New-AzSqlServerCommunicationLink** Cmdlet 會建立通訊連結，用於 Azure SQL Database 中兩個邏輯伺服器之間的固定資料庫交易。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="6ed5c-107">量值資料庫交易可以橫跨其中一個配對伺服器中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="6ed5c-108">您可以在伺服器上建立多個連結。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="6ed5c-109">因此，彈性資料庫交易可能會橫跨許多伺服器。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="6ed5c-110">例子</span><span class="sxs-lookup"><span data-stu-id="6ed5c-110">EXAMPLES</span></span>

### <span data-ttu-id="6ed5c-111">範例 1：建立通訊連結</span><span class="sxs-lookup"><span data-stu-id="6ed5c-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="6ed5c-112">此命令在 ContosoServer17 和 ContosoServer02 之間建立一個名為 Link01 的連結。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="6ed5c-113">參數</span><span class="sxs-lookup"><span data-stu-id="6ed5c-113">PARAMETERS</span></span>

### <span data-ttu-id="6ed5c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ed5c-114">-AsJob</span></span>
<span data-ttu-id="6ed5c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ed5c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ed5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed5c-116">-DefaultProfile</span></span>
<span data-ttu-id="6ed5c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6ed5c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ed5c-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="6ed5c-118">-LinkName</span></span>
<span data-ttu-id="6ed5c-119">指定此 Cmdlet 所建立的伺服器通訊連結名稱。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6ed5c-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="6ed5c-120">-PartnerServer</span></span>
<span data-ttu-id="6ed5c-121">指定參與此通訊連結的其他伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="6ed5c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed5c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ed5c-123">指定 *ServerName* 參數所指定伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="6ed5c-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ed5c-124">-ServerName</span></span>
<span data-ttu-id="6ed5c-125">指定此 Cmdlet 設定通訊連結的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="6ed5c-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6ed5c-126">-Confirm</span></span>
<span data-ttu-id="6ed5c-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed5c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed5c-128">-WhatIf</span></span>
<span data-ttu-id="6ed5c-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ed5c-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed5c-131">CommonParameters</span></span>
<span data-ttu-id="6ed5c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ed5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed5c-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ed5c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed5c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6ed5c-134">INPUTS</span></span>

### <span data-ttu-id="6ed5c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6ed5c-135">System.String</span></span>

## <span data-ttu-id="6ed5c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6ed5c-136">OUTPUTS</span></span>

### <span data-ttu-id="6ed5c-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="6ed5c-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="6ed5c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6ed5c-138">NOTES</span></span>
* <span data-ttu-id="6ed5c-139">關鍵字：azure、azurerm、arm、resource、management、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="6ed5c-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="6ed5c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ed5c-140">RELATED LINKS</span></span>

[<span data-ttu-id="6ed5c-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="6ed5c-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="6ed5c-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="6ed5c-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="6ed5c-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6ed5c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
