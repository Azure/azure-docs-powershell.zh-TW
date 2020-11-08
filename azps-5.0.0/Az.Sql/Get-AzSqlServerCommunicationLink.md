---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138432"
---
# <span data-ttu-id="809e9-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="809e9-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="809e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="809e9-102">SYNOPSIS</span></span>
<span data-ttu-id="809e9-103">取得資料庫伺服器間彈性資料庫事務的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="809e9-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="809e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="809e9-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="809e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="809e9-105">DESCRIPTION</span></span>
<span data-ttu-id="809e9-106">**AzSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL 資料庫中彈性資料庫交易取得伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="809e9-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="809e9-107">指定伺服器通訊連結的名稱，以查看該連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="809e9-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="809e9-108">示例</span><span class="sxs-lookup"><span data-stu-id="809e9-108">EXAMPLES</span></span>

### <span data-ttu-id="809e9-109">範例1：取得伺服器的所有通訊連結</span><span class="sxs-lookup"><span data-stu-id="809e9-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="809e9-110">這個命令會針對名為 ContosoServer17 的伺服器，取得彈性資料庫事務的所有伺服器與伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="809e9-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="809e9-111">範例2：取得伺服器的特定通訊連結</span><span class="sxs-lookup"><span data-stu-id="809e9-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="809e9-112">這個命令會取得名為 Link01 的伺服器到伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="809e9-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="809e9-113">範例3：使用篩選取得伺服器的所有通訊連結</span><span class="sxs-lookup"><span data-stu-id="809e9-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="809e9-114">這個命令會針對以「連結」開頭的伺服器（名為 ContosoServer17）取得彈性資料庫交易的所有伺服器到伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="809e9-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="809e9-115">參數</span><span class="sxs-lookup"><span data-stu-id="809e9-115">PARAMETERS</span></span>

### <span data-ttu-id="809e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809e9-116">-DefaultProfile</span></span>
<span data-ttu-id="809e9-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="809e9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="809e9-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="809e9-118">-LinkName</span></span>
<span data-ttu-id="809e9-119">指定此 Cmdlet 所取得之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="809e9-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="809e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="809e9-121">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="809e9-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="809e9-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="809e9-122">-ServerName</span></span>
<span data-ttu-id="809e9-123">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="809e9-123">Specifies the name of a server.</span></span>
<span data-ttu-id="809e9-124">此伺服器包含此 Cmdlet 取得的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="809e9-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="809e9-125">-確認</span><span class="sxs-lookup"><span data-stu-id="809e9-125">-Confirm</span></span>
<span data-ttu-id="809e9-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="809e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="809e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="809e9-127">-WhatIf</span></span>
<span data-ttu-id="809e9-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="809e9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="809e9-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="809e9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="809e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809e9-130">CommonParameters</span></span>
<span data-ttu-id="809e9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="809e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809e9-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="809e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809e9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="809e9-133">INPUTS</span></span>

### <span data-ttu-id="809e9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="809e9-134">System.String</span></span>

## <span data-ttu-id="809e9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="809e9-135">OUTPUTS</span></span>

### <span data-ttu-id="809e9-136">AzureSqlServerCommunicationLinkModel 中的 [ServerCommunicationLink]</span><span class="sxs-lookup"><span data-stu-id="809e9-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="809e9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="809e9-137">NOTES</span></span>
* <span data-ttu-id="809e9-138">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="809e9-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="809e9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="809e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="809e9-140">新-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="809e9-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="809e9-141">移除-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="809e9-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="809e9-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="809e9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
