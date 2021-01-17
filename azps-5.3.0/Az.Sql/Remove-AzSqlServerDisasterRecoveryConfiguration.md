---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435013"
---
# <span data-ttu-id="32d2b-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32d2b-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="32d2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="32d2b-103">移除 SQL 資料庫伺服器系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="32d2b-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="32d2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="32d2b-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32d2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="32d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="32d2b-106">**AzSqlServerDisasterRecoveryConfiguration** Cmdlet 會移除 SQL database server 系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="32d2b-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="32d2b-107">示例</span><span class="sxs-lookup"><span data-stu-id="32d2b-107">EXAMPLES</span></span>

## <span data-ttu-id="32d2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="32d2b-108">PARAMETERS</span></span>

### <span data-ttu-id="32d2b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d2b-109">-DefaultProfile</span></span>
<span data-ttu-id="32d2b-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="32d2b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32d2b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="32d2b-111">-Force</span></span>
<span data-ttu-id="32d2b-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="32d2b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32d2b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d2b-113">-ResourceGroupName</span></span>
<span data-ttu-id="32d2b-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32d2b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="32d2b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32d2b-115">-ServerName</span></span>
<span data-ttu-id="32d2b-116">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="32d2b-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="32d2b-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="32d2b-117">-VirtualEndpointName</span></span>
<span data-ttu-id="32d2b-118">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="32d2b-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="32d2b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="32d2b-119">-Confirm</span></span>
<span data-ttu-id="32d2b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32d2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32d2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32d2b-121">-WhatIf</span></span>
<span data-ttu-id="32d2b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32d2b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32d2b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32d2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32d2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d2b-124">CommonParameters</span></span>
<span data-ttu-id="32d2b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32d2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d2b-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32d2b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d2b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="32d2b-127">INPUTS</span></span>

### <span data-ttu-id="32d2b-128">System.object</span><span class="sxs-lookup"><span data-stu-id="32d2b-128">System.String</span></span>

## <span data-ttu-id="32d2b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="32d2b-129">OUTPUTS</span></span>

### <span data-ttu-id="32d2b-130">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="32d2b-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="32d2b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="32d2b-131">NOTES</span></span>

## <span data-ttu-id="32d2b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="32d2b-132">RELATED LINKS</span></span>

[<span data-ttu-id="32d2b-133">AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32d2b-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="32d2b-134">新-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32d2b-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="32d2b-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="32d2b-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="32d2b-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="32d2b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
