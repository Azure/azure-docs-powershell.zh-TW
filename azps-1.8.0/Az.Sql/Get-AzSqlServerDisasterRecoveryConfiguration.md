---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ac62ac0307422f0015fe578937a80a03e2a730d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620392"
---
# <span data-ttu-id="cb701-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb701-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="cb701-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb701-102">SYNOPSIS</span></span>
<span data-ttu-id="cb701-103">取得資料庫伺服器系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="cb701-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="cb701-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb701-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb701-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb701-105">DESCRIPTION</span></span>
<span data-ttu-id="cb701-106">**AzSqlServerDisasterRecoveryConfiguration** Cmdlet 會取得 SQL database server 系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="cb701-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="cb701-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb701-107">EXAMPLES</span></span>

## <span data-ttu-id="cb701-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb701-108">PARAMETERS</span></span>

### <span data-ttu-id="cb701-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb701-109">-DefaultProfile</span></span>
<span data-ttu-id="cb701-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cb701-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb701-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb701-111">-ResourceGroupName</span></span>
<span data-ttu-id="cb701-112">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb701-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cb701-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb701-113">-ServerName</span></span>
<span data-ttu-id="cb701-114">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb701-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="cb701-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="cb701-115">-VirtualEndpointName</span></span>
<span data-ttu-id="cb701-116">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb701-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="cb701-117">-確認</span><span class="sxs-lookup"><span data-stu-id="cb701-117">-Confirm</span></span>
<span data-ttu-id="cb701-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb701-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb701-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb701-119">-WhatIf</span></span>
<span data-ttu-id="cb701-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb701-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb701-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb701-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb701-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb701-122">CommonParameters</span></span>
<span data-ttu-id="cb701-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb701-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb701-124">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb701-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb701-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cb701-125">INPUTS</span></span>

### <span data-ttu-id="cb701-126">System.object</span><span class="sxs-lookup"><span data-stu-id="cb701-126">System.String</span></span>

## <span data-ttu-id="cb701-127">輸出</span><span class="sxs-lookup"><span data-stu-id="cb701-127">OUTPUTS</span></span>

### <span data-ttu-id="cb701-128">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="cb701-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="cb701-129">筆記</span><span class="sxs-lookup"><span data-stu-id="cb701-129">NOTES</span></span>

## <span data-ttu-id="cb701-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb701-130">RELATED LINKS</span></span>

[<span data-ttu-id="cb701-131">新-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb701-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="cb701-132">移除-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb701-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="cb701-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb701-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="cb701-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cb701-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
