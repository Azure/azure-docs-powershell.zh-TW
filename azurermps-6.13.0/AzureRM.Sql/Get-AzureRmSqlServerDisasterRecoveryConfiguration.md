---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 792d72c509df4c6b84f4ea86e597ddd8040a30d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454543"
---
# <span data-ttu-id="12a8c-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="12a8c-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="12a8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="12a8c-103">取得資料庫伺服器系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="12a8c-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="12a8c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12a8c-105">說明</span><span class="sxs-lookup"><span data-stu-id="12a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="12a8c-106">**AzureRmSqlServerDisasterRecoveryConfiguration** Cmdlet 會取得 SQL database server 系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="12a8c-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="12a8c-107">示例</span><span class="sxs-lookup"><span data-stu-id="12a8c-107">EXAMPLES</span></span>

## <span data-ttu-id="12a8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="12a8c-108">PARAMETERS</span></span>

### <span data-ttu-id="12a8c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a8c-109">-DefaultProfile</span></span>
<span data-ttu-id="12a8c-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="12a8c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12a8c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a8c-111">-ResourceGroupName</span></span>
<span data-ttu-id="12a8c-112">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12a8c-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="12a8c-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12a8c-113">-ServerName</span></span>
<span data-ttu-id="12a8c-114">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="12a8c-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="12a8c-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="12a8c-115">-VirtualEndpointName</span></span>
<span data-ttu-id="12a8c-116">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="12a8c-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="12a8c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="12a8c-117">-Confirm</span></span>
<span data-ttu-id="12a8c-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12a8c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12a8c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a8c-119">-WhatIf</span></span>
<span data-ttu-id="12a8c-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12a8c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a8c-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12a8c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12a8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a8c-122">CommonParameters</span></span>
<span data-ttu-id="12a8c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12a8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a8c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12a8c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a8c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="12a8c-125">INPUTS</span></span>

### <span data-ttu-id="12a8c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="12a8c-126">System.String</span></span>

## <span data-ttu-id="12a8c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="12a8c-127">OUTPUTS</span></span>

### <span data-ttu-id="12a8c-128">AzureSqlServerDisasterRecoveryConfigurationModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="12a8c-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="12a8c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="12a8c-129">NOTES</span></span>

## <span data-ttu-id="12a8c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="12a8c-130">RELATED LINKS</span></span>

[<span data-ttu-id="12a8c-131">新-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="12a8c-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="12a8c-132">移除-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="12a8c-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="12a8c-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="12a8c-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="12a8c-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="12a8c-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

