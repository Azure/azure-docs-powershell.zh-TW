---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ad00759bb2babb85c17ab9efe2d7e47025434607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909430"
---
# <span data-ttu-id="695a0-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="695a0-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="695a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="695a0-102">SYNOPSIS</span></span>
<span data-ttu-id="695a0-103">獲得資料庫伺服器系統復原組。</span><span class="sxs-lookup"><span data-stu-id="695a0-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="695a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="695a0-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="695a0-105">描述</span><span class="sxs-lookup"><span data-stu-id="695a0-105">DESCRIPTION</span></span>
<span data-ttu-id="695a0-106">**Get-AzSqlServerDsterRecoveryConfiguration** Cmdlet 會取得 SQL 資料庫伺服器系統復原組式。</span><span class="sxs-lookup"><span data-stu-id="695a0-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="695a0-107">例子</span><span class="sxs-lookup"><span data-stu-id="695a0-107">EXAMPLES</span></span>

## <span data-ttu-id="695a0-108">參數</span><span class="sxs-lookup"><span data-stu-id="695a0-108">PARAMETERS</span></span>

### <span data-ttu-id="695a0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695a0-109">-DefaultProfile</span></span>
<span data-ttu-id="695a0-110">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="695a0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="695a0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695a0-111">-ResourceGroupName</span></span>
<span data-ttu-id="695a0-112">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="695a0-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="695a0-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="695a0-113">-ServerName</span></span>
<span data-ttu-id="695a0-114">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="695a0-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="695a0-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="695a0-115">-VirtualEndpointName</span></span>
<span data-ttu-id="695a0-116">指定虛擬結束點的名稱。</span><span class="sxs-lookup"><span data-stu-id="695a0-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695a0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="695a0-117">-Confirm</span></span>
<span data-ttu-id="695a0-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="695a0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="695a0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="695a0-119">-WhatIf</span></span>
<span data-ttu-id="695a0-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="695a0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="695a0-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="695a0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="695a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695a0-122">CommonParameters</span></span>
<span data-ttu-id="695a0-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="695a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695a0-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="695a0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695a0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="695a0-125">INPUTS</span></span>

### <span data-ttu-id="695a0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="695a0-126">System.String</span></span>

## <span data-ttu-id="695a0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="695a0-127">OUTPUTS</span></span>

### <span data-ttu-id="695a0-128">Microsoft.Azure.Commands.Sql.ServerDazsterRecoveryConfiguration.Model.AzureSqlServerDsterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="695a0-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="695a0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="695a0-129">NOTES</span></span>

## <span data-ttu-id="695a0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="695a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="695a0-131">New-AzSqlServerDsterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="695a0-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="695a0-132">Remove-AzSqlServerDsterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="695a0-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="695a0-133">Set-AzSqlServerD區sterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="695a0-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="695a0-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="695a0-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

