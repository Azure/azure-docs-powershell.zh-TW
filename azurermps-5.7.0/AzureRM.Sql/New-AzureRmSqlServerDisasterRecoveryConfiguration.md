---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450446"
---
# <span data-ttu-id="df5d7-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df5d7-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="df5d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="df5d7-103">建立資料庫伺服器系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="df5d7-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df5d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="df5d7-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df5d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="df5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="df5d7-106">**AzureRmSqlServerDisasterRecoveryConfiguration** Cmdlet 會建立 SQL database server 系統復原設定。</span><span class="sxs-lookup"><span data-stu-id="df5d7-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="df5d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="df5d7-107">EXAMPLES</span></span>

## <span data-ttu-id="df5d7-108">參數</span><span class="sxs-lookup"><span data-stu-id="df5d7-108">PARAMETERS</span></span>

### <span data-ttu-id="df5d7-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df5d7-109">-AsJob</span></span>
<span data-ttu-id="df5d7-110">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="df5d7-110">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="df5d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5d7-111">-DefaultProfile</span></span>
<span data-ttu-id="df5d7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df5d7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df5d7-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="df5d7-113">-FailoverPolicy</span></span>
<span data-ttu-id="df5d7-114">指定容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="df5d7-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5d7-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5d7-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="df5d7-116">指定合作夥伴資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df5d7-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="df5d7-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="df5d7-117">-PartnerServerName</span></span>
<span data-ttu-id="df5d7-118">指定合作夥伴伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="df5d7-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="df5d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="df5d7-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df5d7-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="df5d7-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df5d7-121">-ServerName</span></span>
<span data-ttu-id="df5d7-122">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="df5d7-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="df5d7-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="df5d7-123">-VirtualEndpointName</span></span>
<span data-ttu-id="df5d7-124">指定虛擬終點的名稱。</span><span class="sxs-lookup"><span data-stu-id="df5d7-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="df5d7-125">-確認</span><span class="sxs-lookup"><span data-stu-id="df5d7-125">-Confirm</span></span>
<span data-ttu-id="df5d7-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df5d7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5d7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5d7-127">-WhatIf</span></span>
<span data-ttu-id="df5d7-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df5d7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df5d7-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df5d7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df5d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5d7-130">CommonParameters</span></span>
<span data-ttu-id="df5d7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df5d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5d7-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df5d7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5d7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="df5d7-133">INPUTS</span></span>

### <span data-ttu-id="df5d7-134">所有</span><span class="sxs-lookup"><span data-stu-id="df5d7-134">None</span></span>
<span data-ttu-id="df5d7-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="df5d7-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df5d7-136">輸出</span><span class="sxs-lookup"><span data-stu-id="df5d7-136">OUTPUTS</span></span>

## <span data-ttu-id="df5d7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="df5d7-137">NOTES</span></span>

## <span data-ttu-id="df5d7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="df5d7-138">RELATED LINKS</span></span>

[<span data-ttu-id="df5d7-139">AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df5d7-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="df5d7-140">移除-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df5d7-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="df5d7-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df5d7-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="df5d7-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="df5d7-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
