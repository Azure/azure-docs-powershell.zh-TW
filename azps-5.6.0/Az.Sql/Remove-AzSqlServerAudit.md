---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: be2017c829a97196ad5cf2cef9d3dbd71144a325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913105"
---
# <span data-ttu-id="40813-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="40813-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="40813-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40813-102">SYNOPSIS</span></span>
<span data-ttu-id="40813-103">移除 Azure SQL 伺服器的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="40813-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="40813-104">語法</span><span class="sxs-lookup"><span data-stu-id="40813-104">SYNTAX</span></span>

### <span data-ttu-id="40813-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="40813-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40813-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40813-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40813-107">描述</span><span class="sxs-lookup"><span data-stu-id="40813-107">DESCRIPTION</span></span>
<span data-ttu-id="40813-108">**Remove-AzSqlServerAudit** Cmdlet 會移除 Azure SQL 伺服器的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="40813-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="40813-109">指定 *ResourceGroupName* 和 *ServerName* 參數以識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="40813-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="40813-110">例子</span><span class="sxs-lookup"><span data-stu-id="40813-110">EXAMPLES</span></span>

### <span data-ttu-id="40813-111">範例 1：移除 Azure SQL 伺服器的稽核設定</span><span class="sxs-lookup"><span data-stu-id="40813-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="40813-112">範例 2：透過管線移除 Azure SQL 伺服器的稽核設定</span><span class="sxs-lookup"><span data-stu-id="40813-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="40813-113">參數</span><span class="sxs-lookup"><span data-stu-id="40813-113">PARAMETERS</span></span>

### <span data-ttu-id="40813-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40813-114">-AsJob</span></span>
<span data-ttu-id="40813-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40813-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40813-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40813-116">-DefaultProfile</span></span>
<span data-ttu-id="40813-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40813-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40813-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40813-118">-ResourceGroupName</span></span>
<span data-ttu-id="40813-119">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40813-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="40813-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40813-120">-ServerName</span></span>
<span data-ttu-id="40813-121">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="40813-121">SQL server name.</span></span>

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

### <span data-ttu-id="40813-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="40813-122">-ServerObject</span></span>
<span data-ttu-id="40813-123">管理其稽核策略的伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="40813-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="40813-124">-確認</span><span class="sxs-lookup"><span data-stu-id="40813-124">-Confirm</span></span>
<span data-ttu-id="40813-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="40813-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40813-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40813-126">-WhatIf</span></span>
<span data-ttu-id="40813-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40813-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40813-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40813-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40813-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40813-129">CommonParameters</span></span>
<span data-ttu-id="40813-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40813-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40813-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40813-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40813-132">輸入</span><span class="sxs-lookup"><span data-stu-id="40813-132">INPUTS</span></span>

### <span data-ttu-id="40813-133">System.String</span><span class="sxs-lookup"><span data-stu-id="40813-133">System.String</span></span>

### <span data-ttu-id="40813-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="40813-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="40813-135">輸出</span><span class="sxs-lookup"><span data-stu-id="40813-135">OUTPUTS</span></span>

### <span data-ttu-id="40813-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40813-136">System.Boolean</span></span>

## <span data-ttu-id="40813-137">筆記</span><span class="sxs-lookup"><span data-stu-id="40813-137">NOTES</span></span>

## <span data-ttu-id="40813-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="40813-138">RELATED LINKS</span></span>
