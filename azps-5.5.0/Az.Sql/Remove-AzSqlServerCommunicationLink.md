---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127399"
---
# <span data-ttu-id="6484c-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="6484c-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="6484c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6484c-102">SYNOPSIS</span></span>
<span data-ttu-id="6484c-103">刪除兩個伺服器間彈性資料庫交易的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="6484c-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="6484c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6484c-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6484c-105">說明</span><span class="sxs-lookup"><span data-stu-id="6484c-105">DESCRIPTION</span></span>
<span data-ttu-id="6484c-106">**AzSqlServerCommunicationLink** Cmdlet 會針對 Azure SQL database 中彈性資料庫事務刪除伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="6484c-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="6484c-107">示例</span><span class="sxs-lookup"><span data-stu-id="6484c-107">EXAMPLES</span></span>

### <span data-ttu-id="6484c-108">範例1：刪除通訊連結</span><span class="sxs-lookup"><span data-stu-id="6484c-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="6484c-109">這個命令會在 ContosoServer17 上刪除一個名為 Link01 的伺服器對伺服器通訊連結。</span><span class="sxs-lookup"><span data-stu-id="6484c-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="6484c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6484c-110">PARAMETERS</span></span>

### <span data-ttu-id="6484c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6484c-111">-DefaultProfile</span></span>
<span data-ttu-id="6484c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6484c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6484c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6484c-113">-Force</span></span>
<span data-ttu-id="6484c-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6484c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6484c-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="6484c-115">-LinkName</span></span>
<span data-ttu-id="6484c-116">指定此 Cmdlet 刪除之伺服器通訊連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="6484c-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="6484c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6484c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6484c-118">指定 *ServerName* 參數所指定之伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6484c-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="6484c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6484c-119">-ServerName</span></span>
<span data-ttu-id="6484c-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6484c-120">Specifies the name of a server.</span></span>
<span data-ttu-id="6484c-121">此伺服器包含此 Cmdlet 刪除的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="6484c-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="6484c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="6484c-122">-Confirm</span></span>
<span data-ttu-id="6484c-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6484c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6484c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6484c-124">-WhatIf</span></span>
<span data-ttu-id="6484c-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6484c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6484c-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6484c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6484c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6484c-127">CommonParameters</span></span>
<span data-ttu-id="6484c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6484c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6484c-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6484c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6484c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6484c-130">INPUTS</span></span>

### <span data-ttu-id="6484c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="6484c-131">System.String</span></span>

## <span data-ttu-id="6484c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6484c-132">OUTPUTS</span></span>

### <span data-ttu-id="6484c-133">AzureSqlServerCommunicationLinkModel 中的 [ServerCommunicationLink]</span><span class="sxs-lookup"><span data-stu-id="6484c-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="6484c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6484c-134">NOTES</span></span>
* <span data-ttu-id="6484c-135">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、database、mssql</span><span class="sxs-lookup"><span data-stu-id="6484c-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="6484c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6484c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6484c-137">AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="6484c-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="6484c-138">新-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="6484c-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="6484c-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6484c-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
