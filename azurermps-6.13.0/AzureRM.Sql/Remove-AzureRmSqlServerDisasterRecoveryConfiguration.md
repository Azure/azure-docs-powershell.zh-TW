---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626040"
---
# <span data-ttu-id="2c26c-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c26c-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2c26c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c26c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c26c-103">移除 SQL 資料庫伺服器系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="2c26c-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c26c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c26c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c26c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c26c-105">DESCRIPTION</span></span>
<span data-ttu-id="2c26c-106">**AzureRmSqlServerDisasterRecoveryConfiguration** Cmdlet 會移除 SQL database server 系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="2c26c-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2c26c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c26c-107">EXAMPLES</span></span>

## <span data-ttu-id="2c26c-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c26c-108">PARAMETERS</span></span>

### <span data-ttu-id="2c26c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c26c-109">-DefaultProfile</span></span>
<span data-ttu-id="2c26c-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2c26c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c26c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2c26c-111">-Force</span></span>
<span data-ttu-id="2c26c-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2c26c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c26c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c26c-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c26c-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c26c-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2c26c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2c26c-115">-ServerName</span></span>
<span data-ttu-id="2c26c-116">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c26c-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="2c26c-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2c26c-117">-VirtualEndpointName</span></span>
<span data-ttu-id="2c26c-118">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c26c-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="2c26c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2c26c-119">-Confirm</span></span>
<span data-ttu-id="2c26c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c26c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c26c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c26c-121">-WhatIf</span></span>
<span data-ttu-id="2c26c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c26c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c26c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c26c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c26c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c26c-124">CommonParameters</span></span>
<span data-ttu-id="2c26c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c26c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c26c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c26c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c26c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2c26c-127">INPUTS</span></span>

### <span data-ttu-id="2c26c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2c26c-128">System.String</span></span>

## <span data-ttu-id="2c26c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2c26c-129">OUTPUTS</span></span>

### <span data-ttu-id="2c26c-130">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="2c26c-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="2c26c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2c26c-131">NOTES</span></span>

## <span data-ttu-id="2c26c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c26c-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c26c-133">AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c26c-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2c26c-134">新-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c26c-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2c26c-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c26c-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2c26c-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2c26c-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
