---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 20f0fe00486b6b81ec1600e518c42121f5369095
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909441"
---
# <span data-ttu-id="d69f4-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d69f4-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d69f4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d69f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d69f4-103">在資料庫伺服器之間，針對彈性資料庫交易獲得通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d69f4-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="d69f4-104">語法</span><span class="sxs-lookup"><span data-stu-id="d69f4-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d69f4-105">描述</span><span class="sxs-lookup"><span data-stu-id="d69f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d69f4-106">**Get-AzSqlServerCommunicationLink** Cmdlet 會取得 Azure SQL Database 中彈性資料庫交易的伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d69f4-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="d69f4-107">指定伺服器通訊連結的名稱，以查看該連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="d69f4-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="d69f4-108">例子</span><span class="sxs-lookup"><span data-stu-id="d69f4-108">EXAMPLES</span></span>

### <span data-ttu-id="d69f4-109">範例 1：取得伺服器的所有通訊連結</span><span class="sxs-lookup"><span data-stu-id="d69f4-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="d69f4-110">此命令會針對名為 ContosoServer17 的伺服器，獲得所有伺服器對伺服器通訊連結，以利於處理資料庫交易。</span><span class="sxs-lookup"><span data-stu-id="d69f4-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="d69f4-111">範例 2：取得伺服器的特定通訊連結</span><span class="sxs-lookup"><span data-stu-id="d69f4-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="d69f4-112">此命令會獲得名稱為 Link01 的伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d69f4-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="d69f4-113">範例 3：使用篩選取得伺服器的所有通訊連結</span><span class="sxs-lookup"><span data-stu-id="d69f4-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="d69f4-114">此命令會針對名稱為 ContosoServer17 的伺服器，以「連結」為起點，獲得所有伺服器對伺服器通訊連結，以利於處理資料庫交易。</span><span class="sxs-lookup"><span data-stu-id="d69f4-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="d69f4-115">參數</span><span class="sxs-lookup"><span data-stu-id="d69f4-115">PARAMETERS</span></span>

### <span data-ttu-id="d69f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69f4-116">-DefaultProfile</span></span>
<span data-ttu-id="d69f4-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d69f4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d69f4-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="d69f4-118">-LinkName</span></span>
<span data-ttu-id="d69f4-119">指定此 Cmdlet 獲得的伺服器通訊連結名稱。</span><span class="sxs-lookup"><span data-stu-id="d69f4-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d69f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="d69f4-121">指定 *ServerName* 參數所指定伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d69f4-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d69f4-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d69f4-122">-ServerName</span></span>
<span data-ttu-id="d69f4-123">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d69f4-123">Specifies the name of a server.</span></span>
<span data-ttu-id="d69f4-124">此伺服器包含此 Cmdlet 所獲取的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d69f4-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d69f4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d69f4-125">-Confirm</span></span>
<span data-ttu-id="d69f4-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d69f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69f4-127">-WhatIf</span></span>
<span data-ttu-id="d69f4-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d69f4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69f4-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d69f4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d69f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69f4-130">CommonParameters</span></span>
<span data-ttu-id="d69f4-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d69f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69f4-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d69f4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69f4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d69f4-133">INPUTS</span></span>

### <span data-ttu-id="d69f4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d69f4-134">System.String</span></span>

## <span data-ttu-id="d69f4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d69f4-135">OUTPUTS</span></span>

### <span data-ttu-id="d69f4-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d69f4-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d69f4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d69f4-137">NOTES</span></span>
* <span data-ttu-id="d69f4-138">關鍵字：azure、azurerm、arm、resource、management、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="d69f4-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d69f4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d69f4-139">RELATED LINKS</span></span>

[<span data-ttu-id="d69f4-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d69f4-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d69f4-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d69f4-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="d69f4-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d69f4-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
