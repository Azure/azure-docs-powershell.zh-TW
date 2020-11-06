---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 4f9abf17be9b90cb4650c6f38748702dc0955b9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448539"
---
# <span data-ttu-id="944b9-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="944b9-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="944b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="944b9-102">SYNOPSIS</span></span>
<span data-ttu-id="944b9-103">刪除兩個伺服器間彈性資料庫交易的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="944b9-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="944b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="944b9-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="944b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="944b9-105">DESCRIPTION</span></span>
<span data-ttu-id="944b9-106">**AzureRmSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL database 中彈性資料庫事務刪除伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="944b9-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="944b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="944b9-107">EXAMPLES</span></span>

### <span data-ttu-id="944b9-108">範例1：刪除通訊連結</span><span class="sxs-lookup"><span data-stu-id="944b9-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="944b9-109">這個命令會在 ContosoServer17 上刪除一個名為 Link01 的伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="944b9-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="944b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="944b9-110">PARAMETERS</span></span>

### <span data-ttu-id="944b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944b9-111">-DefaultProfile</span></span>
<span data-ttu-id="944b9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="944b9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="944b9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="944b9-113">-Force</span></span>
<span data-ttu-id="944b9-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="944b9-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="944b9-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="944b9-115">-LinkName</span></span>
<span data-ttu-id="944b9-116">指定此 Cmdlet 刪除之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="944b9-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="944b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="944b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="944b9-118">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="944b9-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="944b9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="944b9-119">-ServerName</span></span>
<span data-ttu-id="944b9-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="944b9-120">Specifies the name of a server.</span></span>
<span data-ttu-id="944b9-121">此伺服器包含此 Cmdlet 刪除的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="944b9-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="944b9-122">-確認</span><span class="sxs-lookup"><span data-stu-id="944b9-122">-Confirm</span></span>
<span data-ttu-id="944b9-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="944b9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="944b9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="944b9-124">-WhatIf</span></span>
<span data-ttu-id="944b9-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="944b9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="944b9-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="944b9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="944b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944b9-127">CommonParameters</span></span>
<span data-ttu-id="944b9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="944b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944b9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="944b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944b9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="944b9-130">INPUTS</span></span>

### <span data-ttu-id="944b9-131">所有</span><span class="sxs-lookup"><span data-stu-id="944b9-131">None</span></span>
<span data-ttu-id="944b9-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="944b9-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="944b9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="944b9-133">OUTPUTS</span></span>

### <span data-ttu-id="944b9-134">AzureSqlServerCommunicationLinkModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="944b9-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="944b9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="944b9-135">NOTES</span></span>
* <span data-ttu-id="944b9-136">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="944b9-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="944b9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="944b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="944b9-138">AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="944b9-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="944b9-139">新-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="944b9-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="944b9-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="944b9-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
