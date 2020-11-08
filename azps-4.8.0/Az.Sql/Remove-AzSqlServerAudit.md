---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129165"
---
# <span data-ttu-id="a70f2-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a70f2-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="a70f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a70f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a70f2-103">移除 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="a70f2-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="a70f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a70f2-104">SYNTAX</span></span>

### <span data-ttu-id="a70f2-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a70f2-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70f2-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a70f2-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70f2-107">說明</span><span class="sxs-lookup"><span data-stu-id="a70f2-107">DESCRIPTION</span></span>
<span data-ttu-id="a70f2-108">**AzSqlServerAudit** Cmdlet 會移除 Azure SQL server 的審核設定。</span><span class="sxs-lookup"><span data-stu-id="a70f2-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="a70f2-109">指定 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="a70f2-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="a70f2-110">示例</span><span class="sxs-lookup"><span data-stu-id="a70f2-110">EXAMPLES</span></span>

### <span data-ttu-id="a70f2-111">範例1：移除 Azure SQL server 的審核設定</span><span class="sxs-lookup"><span data-stu-id="a70f2-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="a70f2-112">範例2：在管道中移除 Azure SQL server 的審核設定</span><span class="sxs-lookup"><span data-stu-id="a70f2-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="a70f2-113">參數</span><span class="sxs-lookup"><span data-stu-id="a70f2-113">PARAMETERS</span></span>

### <span data-ttu-id="a70f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a70f2-114">-AsJob</span></span>
<span data-ttu-id="a70f2-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a70f2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a70f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70f2-116">-DefaultProfile</span></span>
<span data-ttu-id="a70f2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a70f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a70f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="a70f2-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a70f2-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70f2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a70f2-120">-ServerName</span></span>
<span data-ttu-id="a70f2-121">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="a70f2-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70f2-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="a70f2-122">-ServerObject</span></span>
<span data-ttu-id="a70f2-123">伺服器物件來管理其審核原則。</span><span class="sxs-lookup"><span data-stu-id="a70f2-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a70f2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a70f2-124">-Confirm</span></span>
<span data-ttu-id="a70f2-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a70f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70f2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70f2-126">-WhatIf</span></span>
<span data-ttu-id="a70f2-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a70f2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a70f2-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a70f2-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70f2-129">CommonParameters</span></span>
<span data-ttu-id="a70f2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a70f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70f2-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a70f2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70f2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a70f2-132">INPUTS</span></span>

### <span data-ttu-id="a70f2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="a70f2-133">System.String</span></span>

### <span data-ttu-id="a70f2-134">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="a70f2-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a70f2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a70f2-135">OUTPUTS</span></span>

### <span data-ttu-id="a70f2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a70f2-136">System.Boolean</span></span>

## <span data-ttu-id="a70f2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a70f2-137">NOTES</span></span>

## <span data-ttu-id="a70f2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a70f2-138">RELATED LINKS</span></span>
