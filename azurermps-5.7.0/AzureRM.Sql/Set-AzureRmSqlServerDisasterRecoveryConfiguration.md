---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445976"
---
# <span data-ttu-id="47715-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="47715-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="47715-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47715-102">SYNOPSIS</span></span>
<span data-ttu-id="47715-103">修改資料庫伺服器的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="47715-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47715-104">句法</span><span class="sxs-lookup"><span data-stu-id="47715-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47715-105">說明</span><span class="sxs-lookup"><span data-stu-id="47715-105">DESCRIPTION</span></span>
<span data-ttu-id="47715-106">**AzureRmSqlServerDisasterRecoveryConfiguration** Cmdlet 會修改 SQL 資料庫伺服器的恢復設定。</span><span class="sxs-lookup"><span data-stu-id="47715-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="47715-107">示例</span><span class="sxs-lookup"><span data-stu-id="47715-107">EXAMPLES</span></span>

## <span data-ttu-id="47715-108">參數</span><span class="sxs-lookup"><span data-stu-id="47715-108">PARAMETERS</span></span>

### <span data-ttu-id="47715-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="47715-109">-AllowDataLoss</span></span>
<span data-ttu-id="47715-110">表示容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="47715-110">Indicates that the failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47715-111">-AsJob</span></span>
<span data-ttu-id="47715-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47715-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47715-113">-DefaultProfile</span></span>
<span data-ttu-id="47715-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="47715-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-115">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="47715-115">-Failover</span></span>
<span data-ttu-id="47715-116">表示此操作為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="47715-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47715-117">-ResourceGroupName</span></span>
<span data-ttu-id="47715-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47715-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47715-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47715-119">-ServerName</span></span>
<span data-ttu-id="47715-120">指定 SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="47715-120">Specifies the name of a SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47715-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="47715-121">-VirtualEndpointName</span></span>
<span data-ttu-id="47715-122">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="47715-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-123">-確認</span><span class="sxs-lookup"><span data-stu-id="47715-123">-Confirm</span></span>
<span data-ttu-id="47715-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47715-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47715-125">-WhatIf</span></span>
<span data-ttu-id="47715-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47715-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47715-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47715-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47715-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47715-128">CommonParameters</span></span>
<span data-ttu-id="47715-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47715-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47715-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47715-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47715-131">輸入</span><span class="sxs-lookup"><span data-stu-id="47715-131">INPUTS</span></span>

### <span data-ttu-id="47715-132">所有</span><span class="sxs-lookup"><span data-stu-id="47715-132">None</span></span>
<span data-ttu-id="47715-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="47715-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47715-134">輸出</span><span class="sxs-lookup"><span data-stu-id="47715-134">OUTPUTS</span></span>

## <span data-ttu-id="47715-135">筆記</span><span class="sxs-lookup"><span data-stu-id="47715-135">NOTES</span></span>

## <span data-ttu-id="47715-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="47715-136">RELATED LINKS</span></span>

[<span data-ttu-id="47715-137">AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="47715-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="47715-138">新-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="47715-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="47715-139">移除-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="47715-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="47715-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="47715-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
