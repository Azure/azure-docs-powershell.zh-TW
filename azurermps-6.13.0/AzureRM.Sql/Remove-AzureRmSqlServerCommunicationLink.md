---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 3d2137aa1398e5bb3b8173b6ea927c4deb50d41f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626039"
---
# <span data-ttu-id="cb1a5-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="cb1a5-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="cb1a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1a5-103">刪除兩個伺服器間彈性資料庫交易的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb1a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb1a5-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb1a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb1a5-105">DESCRIPTION</span></span>
<span data-ttu-id="cb1a5-106">**AzureRmSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL database 中彈性資料庫事務刪除伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="cb1a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb1a5-107">EXAMPLES</span></span>

### <span data-ttu-id="cb1a5-108">範例1：刪除通訊連結</span><span class="sxs-lookup"><span data-stu-id="cb1a5-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="cb1a5-109">這個命令會在 ContosoServer17 上刪除一個名為 Link01 的伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="cb1a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb1a5-110">PARAMETERS</span></span>

### <span data-ttu-id="cb1a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb1a5-111">-DefaultProfile</span></span>
<span data-ttu-id="cb1a5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cb1a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb1a5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cb1a5-113">-Force</span></span>
<span data-ttu-id="cb1a5-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb1a5-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="cb1a5-115">-LinkName</span></span>
<span data-ttu-id="cb1a5-116">指定此 Cmdlet 刪除之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="cb1a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb1a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb1a5-118">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="cb1a5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb1a5-119">-ServerName</span></span>
<span data-ttu-id="cb1a5-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-120">Specifies the name of a server.</span></span>
<span data-ttu-id="cb1a5-121">此伺服器包含此 Cmdlet 刪除的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="cb1a5-122">-確認</span><span class="sxs-lookup"><span data-stu-id="cb1a5-122">-Confirm</span></span>
<span data-ttu-id="cb1a5-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb1a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb1a5-124">-WhatIf</span></span>
<span data-ttu-id="cb1a5-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb1a5-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb1a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1a5-127">CommonParameters</span></span>
<span data-ttu-id="cb1a5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1a5-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb1a5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1a5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cb1a5-130">INPUTS</span></span>

### <span data-ttu-id="cb1a5-131">System.object</span><span class="sxs-lookup"><span data-stu-id="cb1a5-131">System.String</span></span>

## <span data-ttu-id="cb1a5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cb1a5-132">OUTPUTS</span></span>

### <span data-ttu-id="cb1a5-133">AzureSqlServerCommunicationLinkModel 中的 [ServerCommunicationLink]</span><span class="sxs-lookup"><span data-stu-id="cb1a5-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="cb1a5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cb1a5-134">NOTES</span></span>
* <span data-ttu-id="cb1a5-135">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="cb1a5-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="cb1a5-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb1a5-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb1a5-137">AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="cb1a5-137">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="cb1a5-138">新-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="cb1a5-138">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="cb1a5-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cb1a5-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
