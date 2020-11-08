---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970085"
---
# <span data-ttu-id="b5d74-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b5d74-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="b5d74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5d74-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d74-103">建立兩個 SQL 資料庫伺服器之間彈性資料庫交易的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="b5d74-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="b5d74-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5d74-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5d74-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5d74-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d74-106">**新的-AzSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL 資料庫中的兩個邏輯伺服器之間的彈性資料庫交易建立通訊連結。</span><span class="sxs-lookup"><span data-stu-id="b5d74-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="b5d74-107">彈性資料庫事務可以在其中一個成對伺服器中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b5d74-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="b5d74-108">您可以在伺服器上建立一個以上的連結。</span><span class="sxs-lookup"><span data-stu-id="b5d74-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="b5d74-109">因此，彈性資料庫事務可以跨越大量的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5d74-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="b5d74-110">示例</span><span class="sxs-lookup"><span data-stu-id="b5d74-110">EXAMPLES</span></span>

### <span data-ttu-id="b5d74-111">範例1：建立通訊連結</span><span class="sxs-lookup"><span data-stu-id="b5d74-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="b5d74-112">這個命令會在 ContosoServer17 和 ContosoServer02 之間建立名為 Link01 的連結。</span><span class="sxs-lookup"><span data-stu-id="b5d74-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="b5d74-113">參數</span><span class="sxs-lookup"><span data-stu-id="b5d74-113">PARAMETERS</span></span>

### <span data-ttu-id="b5d74-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5d74-114">-AsJob</span></span>
<span data-ttu-id="b5d74-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5d74-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5d74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d74-116">-DefaultProfile</span></span>
<span data-ttu-id="b5d74-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b5d74-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5d74-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="b5d74-118">-LinkName</span></span>
<span data-ttu-id="b5d74-119">指定此 Cmdlet 所建立之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5d74-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5d74-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="b5d74-120">-PartnerServer</span></span>
<span data-ttu-id="b5d74-121">指定參與此通訊連結之其他伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5d74-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="b5d74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d74-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5d74-123">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5d74-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="b5d74-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5d74-124">-ServerName</span></span>
<span data-ttu-id="b5d74-125">指定此 Cmdlet 設定通訊連結的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b5d74-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="b5d74-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b5d74-126">-Confirm</span></span>
<span data-ttu-id="b5d74-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5d74-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d74-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d74-128">-WhatIf</span></span>
<span data-ttu-id="b5d74-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5d74-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d74-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5d74-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d74-131">CommonParameters</span></span>
<span data-ttu-id="b5d74-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5d74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d74-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b5d74-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d74-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b5d74-134">INPUTS</span></span>

### <span data-ttu-id="b5d74-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b5d74-135">System.String</span></span>

## <span data-ttu-id="b5d74-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b5d74-136">OUTPUTS</span></span>

### <span data-ttu-id="b5d74-137">AzureSqlServerCommunicationLinkModel 中的 [ServerCommunicationLink]</span><span class="sxs-lookup"><span data-stu-id="b5d74-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="b5d74-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b5d74-138">NOTES</span></span>
* <span data-ttu-id="b5d74-139">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="b5d74-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b5d74-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5d74-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5d74-141">AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b5d74-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="b5d74-142">移除-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="b5d74-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="b5d74-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b5d74-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
