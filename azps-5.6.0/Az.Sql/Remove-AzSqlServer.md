---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: b116a6ef09b3de4d3a11c1e9bdbcb831fc34af1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905766"
---
# <span data-ttu-id="e6d4e-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e6d4e-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="e6d4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d4e-103">移除 Azure SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="e6d4e-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6d4e-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6d4e-105">描述</span><span class="sxs-lookup"><span data-stu-id="e6d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="e6d4e-106">**Remove-AzSqlServer** Cmdlet 會移除 Azure SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="e6d4e-107">刪除作業是非同步，可能需要一些時間，因此在執行任何取決於伺服器完全刪除的額外作業之前，請確認作業已完成。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="e6d4e-108">例如，您需要建立使用相同名稱的新伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="e6d4e-109">例子</span><span class="sxs-lookup"><span data-stu-id="e6d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="e6d4e-110">範例 1：移除伺服器</span><span class="sxs-lookup"><span data-stu-id="e6d4e-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e6d4e-111">此命令會移除名為 Server01 的 Azure SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="e6d4e-112">參數</span><span class="sxs-lookup"><span data-stu-id="e6d4e-112">PARAMETERS</span></span>

### <span data-ttu-id="e6d4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d4e-113">-DefaultProfile</span></span>
<span data-ttu-id="e6d4e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e6d4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6d4e-115">-強制</span><span class="sxs-lookup"><span data-stu-id="e6d4e-115">-Force</span></span>
<span data-ttu-id="e6d4e-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6d4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6d4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6d4e-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e6d4e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6d4e-119">-ServerName</span></span>
<span data-ttu-id="e6d4e-120">指定要移除的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d4e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e6d4e-121">-Confirm</span></span>
<span data-ttu-id="e6d4e-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6d4e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6d4e-123">-WhatIf</span></span>
<span data-ttu-id="e6d4e-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6d4e-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6d4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d4e-126">CommonParameters</span></span>
<span data-ttu-id="e6d4e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6d4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d4e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6d4e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d4e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e6d4e-129">INPUTS</span></span>

### <span data-ttu-id="e6d4e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e6d4e-130">System.String</span></span>

## <span data-ttu-id="e6d4e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e6d4e-131">OUTPUTS</span></span>

### <span data-ttu-id="e6d4e-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="e6d4e-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e6d4e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e6d4e-133">NOTES</span></span>

## <span data-ttu-id="e6d4e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6d4e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e6d4e-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e6d4e-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="e6d4e-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e6d4e-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e6d4e-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e6d4e-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="e6d4e-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e6d4e-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


