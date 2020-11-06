---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448885"
---
# <span data-ttu-id="28e20-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="28e20-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="28e20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28e20-102">SYNOPSIS</span></span>
<span data-ttu-id="28e20-103">取得資料庫伺服器系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="28e20-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28e20-104">句法</span><span class="sxs-lookup"><span data-stu-id="28e20-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e20-105">說明</span><span class="sxs-lookup"><span data-stu-id="28e20-105">DESCRIPTION</span></span>
<span data-ttu-id="28e20-106">**AzureRmSqlServerDisasterRecoveryConfigurationActivity** Cmdlet 會取得 SQL database server 系統復原設定的活動。</span><span class="sxs-lookup"><span data-stu-id="28e20-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="28e20-107">示例</span><span class="sxs-lookup"><span data-stu-id="28e20-107">EXAMPLES</span></span>

## <span data-ttu-id="28e20-108">參數</span><span class="sxs-lookup"><span data-stu-id="28e20-108">PARAMETERS</span></span>

### <span data-ttu-id="28e20-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e20-109">-DefaultProfile</span></span>
<span data-ttu-id="28e20-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="28e20-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28e20-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="28e20-111">-OperationId</span></span>
<span data-ttu-id="28e20-112">指定操作 ID。</span><span class="sxs-lookup"><span data-stu-id="28e20-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28e20-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e20-113">-ResourceGroupName</span></span>
<span data-ttu-id="28e20-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28e20-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="28e20-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="28e20-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="28e20-116">指定伺服器系統的復原配置名稱。</span><span class="sxs-lookup"><span data-stu-id="28e20-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28e20-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28e20-117">-ServerName</span></span>
<span data-ttu-id="28e20-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="28e20-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="28e20-119">-確認</span><span class="sxs-lookup"><span data-stu-id="28e20-119">-Confirm</span></span>
<span data-ttu-id="28e20-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28e20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e20-121">-WhatIf</span></span>
<span data-ttu-id="28e20-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28e20-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e20-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e20-124">CommonParameters</span></span>
<span data-ttu-id="28e20-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28e20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e20-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28e20-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e20-127">輸入</span><span class="sxs-lookup"><span data-stu-id="28e20-127">INPUTS</span></span>

### <span data-ttu-id="28e20-128">System.object</span><span class="sxs-lookup"><span data-stu-id="28e20-128">System.String</span></span>

### <span data-ttu-id="28e20-129">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="28e20-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="28e20-130">輸出</span><span class="sxs-lookup"><span data-stu-id="28e20-130">OUTPUTS</span></span>

### <span data-ttu-id="28e20-131">AzureSqlServerDisasterRecoveryConfigurationActivityModel 中的 [ServerDisasterRecoveryConfiguration]</span><span class="sxs-lookup"><span data-stu-id="28e20-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="28e20-132">筆記</span><span class="sxs-lookup"><span data-stu-id="28e20-132">NOTES</span></span>

## <span data-ttu-id="28e20-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="28e20-133">RELATED LINKS</span></span>

[<span data-ttu-id="28e20-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="28e20-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
