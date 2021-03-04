---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913101"
---
# <span data-ttu-id="a8869-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8869-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="a8869-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8869-102">SYNOPSIS</span></span>
<span data-ttu-id="a8869-103">移除 SQL 資料庫伺服器系統復原組組。</span><span class="sxs-lookup"><span data-stu-id="a8869-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a8869-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8869-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8869-105">描述</span><span class="sxs-lookup"><span data-stu-id="a8869-105">DESCRIPTION</span></span>
<span data-ttu-id="a8869-106">**Remove-AzSqlServerDsterRecoveryConfiguration** Cmdlet 會移除 SQL 資料庫伺服器系統復原組式。</span><span class="sxs-lookup"><span data-stu-id="a8869-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a8869-107">例子</span><span class="sxs-lookup"><span data-stu-id="a8869-107">EXAMPLES</span></span>

## <span data-ttu-id="a8869-108">參數</span><span class="sxs-lookup"><span data-stu-id="a8869-108">PARAMETERS</span></span>

### <span data-ttu-id="a8869-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8869-109">-DefaultProfile</span></span>
<span data-ttu-id="a8869-110">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a8869-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8869-111">-強制</span><span class="sxs-lookup"><span data-stu-id="a8869-111">-Force</span></span>
<span data-ttu-id="a8869-112">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a8869-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8869-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8869-113">-ResourceGroupName</span></span>
<span data-ttu-id="a8869-114">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8869-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a8869-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8869-115">-ServerName</span></span>
<span data-ttu-id="a8869-116">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8869-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="a8869-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="a8869-117">-VirtualEndpointName</span></span>
<span data-ttu-id="a8869-118">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8869-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="a8869-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a8869-119">-Confirm</span></span>
<span data-ttu-id="a8869-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a8869-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8869-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8869-121">-WhatIf</span></span>
<span data-ttu-id="a8869-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8869-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8869-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8869-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8869-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8869-124">CommonParameters</span></span>
<span data-ttu-id="a8869-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8869-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8869-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8869-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8869-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a8869-127">INPUTS</span></span>

### <span data-ttu-id="a8869-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a8869-128">System.String</span></span>

## <span data-ttu-id="a8869-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a8869-129">OUTPUTS</span></span>

### <span data-ttu-id="a8869-130">Microsoft.Azure.Commands.Sql.ServerDazsterRecoveryConfiguration.Model.AzureSqlServerDsterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="a8869-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="a8869-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a8869-131">NOTES</span></span>

## <span data-ttu-id="a8869-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8869-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8869-133">Get-AzSqlServerD區sterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8869-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a8869-134">New-AzSqlServerDsterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8869-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a8869-135">Set-AzSqlServerD區sterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8869-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a8869-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a8869-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
