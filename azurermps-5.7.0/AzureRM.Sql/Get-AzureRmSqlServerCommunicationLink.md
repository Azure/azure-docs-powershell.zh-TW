---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8240712b4ec6ef17dfff597bed4dc62d60be42b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623796"
---
# <span data-ttu-id="afae7-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="afae7-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="afae7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afae7-102">SYNOPSIS</span></span>
<span data-ttu-id="afae7-103">取得資料庫伺服器間彈性資料庫事務的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="afae7-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afae7-104">句法</span><span class="sxs-lookup"><span data-stu-id="afae7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afae7-105">說明</span><span class="sxs-lookup"><span data-stu-id="afae7-105">DESCRIPTION</span></span>
<span data-ttu-id="afae7-106">**AzureRmSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL 資料庫中彈性資料庫交易取得伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="afae7-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="afae7-107">指定伺服器通訊連結的名稱，以查看該連結的屬性。</span><span class="sxs-lookup"><span data-stu-id="afae7-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="afae7-108">示例</span><span class="sxs-lookup"><span data-stu-id="afae7-108">EXAMPLES</span></span>

### <span data-ttu-id="afae7-109">範例1：取得伺服器的所有通訊連結</span><span class="sxs-lookup"><span data-stu-id="afae7-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="afae7-110">這個命令會針對名為 ContosoServer17 的伺服器，取得彈性資料庫事務的所有伺服器與伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="afae7-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="afae7-111">範例2：取得伺服器的特定通訊連結</span><span class="sxs-lookup"><span data-stu-id="afae7-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="afae7-112">這個命令會取得名為 Link01 的伺服器到伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="afae7-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="afae7-113">參數</span><span class="sxs-lookup"><span data-stu-id="afae7-113">PARAMETERS</span></span>

### <span data-ttu-id="afae7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afae7-114">-DefaultProfile</span></span>
<span data-ttu-id="afae7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="afae7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afae7-116">-LinkName</span><span class="sxs-lookup"><span data-stu-id="afae7-116">-LinkName</span></span>
<span data-ttu-id="afae7-117">指定此 Cmdlet 所取得之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="afae7-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afae7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afae7-118">-ResourceGroupName</span></span>
<span data-ttu-id="afae7-119">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="afae7-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afae7-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="afae7-120">-ServerName</span></span>
<span data-ttu-id="afae7-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="afae7-121">Specifies the name of a server.</span></span>
<span data-ttu-id="afae7-122">此伺服器包含此 Cmdlet 取得的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="afae7-122">This server contains a communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afae7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="afae7-123">-Confirm</span></span>
<span data-ttu-id="afae7-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="afae7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afae7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afae7-125">-WhatIf</span></span>
<span data-ttu-id="afae7-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afae7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afae7-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afae7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afae7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afae7-128">CommonParameters</span></span>
<span data-ttu-id="afae7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afae7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afae7-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="afae7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afae7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="afae7-131">INPUTS</span></span>

### <span data-ttu-id="afae7-132">所有</span><span class="sxs-lookup"><span data-stu-id="afae7-132">None</span></span>
<span data-ttu-id="afae7-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="afae7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="afae7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="afae7-134">OUTPUTS</span></span>

### <span data-ttu-id="afae7-135">AzureSqlServerCommunicationLinkModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="afae7-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="afae7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="afae7-136">NOTES</span></span>
* <span data-ttu-id="afae7-137">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="afae7-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="afae7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="afae7-138">RELATED LINKS</span></span>

[<span data-ttu-id="afae7-139">新-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="afae7-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="afae7-140">移除-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="afae7-140">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="afae7-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="afae7-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
