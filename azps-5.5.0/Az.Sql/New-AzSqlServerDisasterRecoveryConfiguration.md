---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128206"
---
# <span data-ttu-id="80bc3-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="80bc3-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="80bc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="80bc3-103">建立資料庫伺服器系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="80bc3-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="80bc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="80bc3-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80bc3-105">說明</span><span class="sxs-lookup"><span data-stu-id="80bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="80bc3-106">**AzSqlServerDisasterRecoveryConfiguration** Cmdlet 會建立 SQL database server 系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="80bc3-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="80bc3-107">示例</span><span class="sxs-lookup"><span data-stu-id="80bc3-107">EXAMPLES</span></span>

## <span data-ttu-id="80bc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="80bc3-108">PARAMETERS</span></span>

### <span data-ttu-id="80bc3-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80bc3-109">-AsJob</span></span>
<span data-ttu-id="80bc3-110">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80bc3-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80bc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bc3-111">-DefaultProfile</span></span>
<span data-ttu-id="80bc3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="80bc3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80bc3-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="80bc3-113">-FailoverPolicy</span></span>
<span data-ttu-id="80bc3-114">指定容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="80bc3-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="80bc3-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bc3-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="80bc3-116">指定合作夥伴資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80bc3-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bc3-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="80bc3-117">-PartnerServerName</span></span>
<span data-ttu-id="80bc3-118">指定合作夥伴伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="80bc3-118">Specifies the name of the partner server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bc3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80bc3-119">-ResourceGroupName</span></span>
<span data-ttu-id="80bc3-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80bc3-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="80bc3-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80bc3-121">-ServerName</span></span>
<span data-ttu-id="80bc3-122">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="80bc3-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="80bc3-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="80bc3-123">-VirtualEndpointName</span></span>
<span data-ttu-id="80bc3-124">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="80bc3-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bc3-125">-確認</span><span class="sxs-lookup"><span data-stu-id="80bc3-125">-Confirm</span></span>
<span data-ttu-id="80bc3-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80bc3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80bc3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80bc3-127">-WhatIf</span></span>
<span data-ttu-id="80bc3-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80bc3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80bc3-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80bc3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80bc3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bc3-130">CommonParameters</span></span>
<span data-ttu-id="80bc3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80bc3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bc3-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="80bc3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bc3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="80bc3-133">INPUTS</span></span>

### <span data-ttu-id="80bc3-134">System.object</span><span class="sxs-lookup"><span data-stu-id="80bc3-134">System.String</span></span>

## <span data-ttu-id="80bc3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="80bc3-135">OUTPUTS</span></span>

### <span data-ttu-id="80bc3-136">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="80bc3-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="80bc3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="80bc3-137">NOTES</span></span>

## <span data-ttu-id="80bc3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="80bc3-138">RELATED LINKS</span></span>

[<span data-ttu-id="80bc3-139">AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="80bc3-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="80bc3-140">移除-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="80bc3-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="80bc3-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="80bc3-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="80bc3-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="80bc3-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
