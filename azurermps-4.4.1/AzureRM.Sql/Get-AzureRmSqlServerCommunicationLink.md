---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ed968db32505bcb3c581775d05235cc4c718dd67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451588"
---
# <span data-ttu-id="d4ac1-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d4ac1-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="d4ac1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ac1-103">取得資料庫伺服器間彈性資料庫事務的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4ac1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4ac1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4ac1-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ac1-106">**AzureRmSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL 資料庫中彈性資料庫交易取得伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="d4ac1-107">指定伺服器通訊連結的名稱，以查看該連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="d4ac1-108">示例</span><span class="sxs-lookup"><span data-stu-id="d4ac1-108">EXAMPLES</span></span>

### <span data-ttu-id="d4ac1-109">範例1：取得伺服器的所有通訊連結</span><span class="sxs-lookup"><span data-stu-id="d4ac1-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="d4ac1-110">這個命令會針對名為 ContosoServer17 的伺服器，取得彈性資料庫事務的所有伺服器與伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="d4ac1-111">範例2：取得伺服器的特定通訊連結</span><span class="sxs-lookup"><span data-stu-id="d4ac1-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="d4ac1-112">這個命令會取得名為 Link01 的伺服器到伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="d4ac1-113">參數</span><span class="sxs-lookup"><span data-stu-id="d4ac1-113">PARAMETERS</span></span>

### <span data-ttu-id="d4ac1-114">-LinkName</span><span class="sxs-lookup"><span data-stu-id="d4ac1-114">-LinkName</span></span>
<span data-ttu-id="d4ac1-115">指定此 Cmdlet 所取得之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-115">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d4ac1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ac1-116">-ResourceGroupName</span></span>
<span data-ttu-id="d4ac1-117">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-117">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="d4ac1-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d4ac1-118">-ServerName</span></span>
<span data-ttu-id="d4ac1-119">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-119">Specifies the name of a server.</span></span>
<span data-ttu-id="d4ac1-120">此伺服器包含此 Cmdlet 取得的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-120">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d4ac1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d4ac1-121">-Confirm</span></span>
<span data-ttu-id="d4ac1-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ac1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ac1-123">-WhatIf</span></span>
<span data-ttu-id="d4ac1-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ac1-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ac1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ac1-126">-DefaultProfile</span></span>
<span data-ttu-id="d4ac1-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4ac1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ac1-128">CommonParameters</span></span>
<span data-ttu-id="d4ac1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ac1-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4ac1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ac1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d4ac1-131">INPUTS</span></span>

## <span data-ttu-id="d4ac1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d4ac1-132">OUTPUTS</span></span>

### <span data-ttu-id="d4ac1-133">AzureSqlServerCommunicationLinkModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="d4ac1-133">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="d4ac1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d4ac1-134">NOTES</span></span>
* <span data-ttu-id="d4ac1-135">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="d4ac1-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="d4ac1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4ac1-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4ac1-137">新-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d4ac1-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="d4ac1-138">移除-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="d4ac1-138">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="d4ac1-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d4ac1-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
